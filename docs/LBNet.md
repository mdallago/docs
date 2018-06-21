# Large Block Network

The Large Block Network (LBNet from now on) is a testing ground for an 8MB block bitcoin network. It's easy to modify a bitcoin client to be part of the lbnet, and it should be straightfoward, as it was launched using modified versions of the Bitprim and Bitcoin core nodes.

This guide contains instructions on how to connect to the LBNet.

We will create an environment that will allow us to synchronise the network in testnet, install a mining pool and mine over the network.

The installation and configuration of each part, is detailed below and includes, testnet nodes, pool, and miner

## Node Testnet Install

---

### Requirements:

The following packages will be needed

* Boost 1.58+
* libdb++ 4.8
* libzmq 4.1.4+
* libssl 1.0.2+
* libevent 2.0.21+
* git 

#### Ubuntu 16.04+

Installing Dependencies:

```
$ sudo apt-get install build-essential libtool autotools-dev automake pkg-config bsdmainutils
$ sudo apt-get install libzmq3-dev # libzmq
$ sudo apt-get install libboost-all-dev # Boost
$ sudo apt-get install libssl-dev # libssl
$ sudo apt-get install libevent-dev # libevent

$ sudo add-apt-repository ppa:bitcoin/bitcoin
$ sudo apt-get update
$ sudo apt-get install libdb4.8-dev libdb4.8++-dev # libdb

$ mkdir src
$ cd src
$ git clone https://github.com/bitprim/bitcoin/ -b bitcore-lbnet
$ cd bitcoin
$ ./autogen.sh
$ ./configure
$ make
$ make install
```

#### Other Distros

Install all dependencies without libdb++ 4.8 in your distro and follow these steps

```sh
$ mkdir src
$ cd src
$ git clone https://github.com/bitprim/bitcoin/ -b bitcore-lbnet
$ cd bitcoin
```

Create a file (we will call it  compile.sh) 

```sh
$ vi compile.sh
```
Now add following content:

```sh
#!/bin/bash
BITCOIN_ROOT=$(pwd)

# Pick some path to install BDB to, here we create a directory within the bitcoin directory
BDB_PREFIX="${BITCOIN_ROOT}/db4"
mkdir -p $BDB_PREFIX

# Fetch the source and verify that it is not tampered with
wget 'http://download.oracle.com/berkeley-db/db-4.8.30.NC.tar.gz'
echo '12edc0df75bf9abd7f82f821795bcee50f42cb2e5f76a6a281b85732798364ef  db-4.8.30.NC.tar.gz' | sha256sum -c
# -> db-4.8.30.NC.tar.gz: OK
tar -xzvf db-4.8.30.NC.tar.gz

# Build the library and install to our prefix
cd db-4.8.30.NC/build_unix/
#  Note: Do a static build so that it can be embedded into the executable, instead of having to find a .so at runtime
../dist/configure --enable-cxx --disable-shared --with-pic --prefix=$BDB_PREFIX
make install

# Configure Bitcoin Core to use our own-built instance of BDB
cd $BITCOIN_ROOT
./autogen.sh
./configure LDFLAGS="-L${BDB_PREFIX}/lib/" CPPFLAGS="-I${BDB_PREFIX}/include/" --with-boost=/usr/local/include/boost --with-boost-libdir=/usr/local/lib
```

Run the following instruccions:

```sh
$ chmod 755 compile.sh
$ ./compile
$ make
$ make install 
```

### Node Testnet Configuration

---

```sh
$ mkdir ~/.bitcoin
```
Use your favourite editor and edit following file ~/.bitcoin/bitcoin.conf

```sh
$ vi ~/.bitcoin/bitcoin.conf
```
Add the following content

```
testnet=1
txindex=1
addressindex=1
spentindex=1
reindex=1
zmqpubrawtx=tcp://127.0.0.1:28332
zmqpubhashblock=tcp://127.0.0.1:28332
rpcuser=rpcuser # Modify this
rpcpassword=rpcpass # Modify this
```
If you want leave the bitcoind running in background remember add "daemon=1" in bitcoin.conf


## Create a wallet

---

To create a new bitcoin wallet, run the following line

```sh
$ bitcoin-cli getnewaddress
mwTjQwRiny2ss741EAvzFqCfpnhYXai8Zu
$
```

## Pool Install
---

Install NOMP ( Node Open Mining Portal ) following the steps on this [Install guide](https://github.com/zone117x/node-open-mining-portal/) up to point "Coin Config"

After that we need to configure the pool for bitcoin lbnet


### Pool Configuration

```sh
$ cd nomp
$ cd pool_configs
```

Use your favourite editor and edit following file bitcoin.json

```sh
$ vi bitcoin.json
```
Add the following content

```
{
    "enabled": true,
    "coin": "bitcoin.json",

    "address": "<< YOUR WALLET ADDRESS >>",

    "rewardRecipients": {
    },

    "paymentProcessing": {
        "enabled": false,
        "paymentInterval": 20,
        "minimumPayment": 70,
        "daemon": {
            "host": "127.0.0.1",
            "port": 18332,
            "user": "rpcuser",
            "password": "rpcpass"
        }
    },

    "ports": {
        "4008": {
            "diff": 1
        },
        "4333": {
            "diff": 32,
            "varDiff": {
                "minDiff": 8,
                "maxDiff": 512,
                "targetTime": 15,
                "retargetTime": 90,
                "variancePercent": 30
            }
        },
        "4080": {
            "diff": 8192,
            "varDiff": {
                "minDiff": 8192,
                "maxDiff": 38400,
                "targetTime": 90,
                "retargetTime": 18,
                "variancePercent": 30
            }
        }
    },

    "daemons": [
        {
            "host": "127.0.0.1",
            "port": 18332,
            "user": "rpcuser",
            "password": "rpcpass"
        }
    ],

    "p2p": {
        "enabled": false,
        "host": "127.0.0.1",
        "port": 18333,
        "disableTransactions": true
    },

    "mposMode": {
        "enabled": false,
        "host": "127.0.0.1",
        "port": 3306,
        "user": "me",
        "password": "mypass",
        "database": "btc",
        "checkPassword": true,
        "autoCreateWorker": false
    }

}
```

Note that you need change the wallet address and the username and password of rpc defined earlier on the `Node Testnet Configuration` step.

Now you will be able to start nomp

```sh
$ cd ..
$ node init.js
```

We recommend leave app running inside a screen session.

If the command `node init.js` gives an error, it usually is because one of the following reasons:
* The redis-server is not running, so in a screen session start the redis server

```sh
$ redis-server start
```

* The `node` version is not compatible with `nomp`, to fix it run the next command before the `init.js`

```sh
$ nvm use 0.10.25
$ node init.js
```


## Miner Install

---

```sh
$ cd src
$ https://github.com/pooler/cpuminer.git
$ cd cpuminer
$ ./autogen.sh
$ ./configure CFLAGS="-O3"
$ make
$ make install
```

### Running Miner

```sh
$ minerd -o stratum+tcp://127.0.0.1:4008 -u << YOUR WALLET ADDRESS >> -a sha256d
```

At this point you have a node running in testnet, a mining pool running and the miner, please if you have any problem, send us a message

## Setup a Bitprim node

---

As an alternative you could run LBNet over the Bitprim client. First you should clone the [`Bitprim-build`](https://github.com/bitprim/bitprim-build/tree/lbnet) repository, and go the the LBnet branch.

```sh
git clone https://github.com/bitprim/bitprim-build.git --recursive -b lbnet

```

Now build the project following the instruccions stated in the the [`Bitprim-build`](https://github.com/bitprim/bitprim-build) Readme.

#### Run Bitprim lbnet
First execute the boostrap script. `bitprim-bootstrap-ibd-lbnet.sh` located in the `bin` folder. This will create the files needed by `Bitprim-node`, and will download the full chain in the background. 

Example:
```sh
$ sudo /opt/bitprim/bin/bitprim-bootstrap-ibd-lbnet.sh start
Creating Empty Database
22:29:15.904332 INFO [server] ================= startup  ==================
22:29:15.904365 WARNING [server] ================= startup  ==================
22:29:15.904408 ERROR [server] ================= startup  ==================
22:29:15.904429 FATAL [server] ================= startup  ==================
22:29:15.904446 INFO [server] Using config file: "/opt/bitprim/cfg/bitprim-node-lbnet-ibd.cfg"
22:29:15.904492 INFO [server] Please wait while initializing "/opt/bitprim/dbs/lbnet" directory...
22:29:21.492262 INFO [server] Completed initialization.
Starting Process
$
```
If necessary its possible to check status, or to stop the process by using `status` or `stop` parameters.

Example:
```sh
$ sudo /opt/bitprim/bin/bitprim-bootstrap-ibd-lbnet.sh stop
Stoping Process
Process is running ... wait
Process is running ... wait
Process is running ... wait
Stoping Done
```
**Note that the stop process may take a few minutes.**

#### Normal execution
Run the full node, using the `bitprim-node-lbnet-run.sh`.
```sh
$ sudo /opt/bitprim/bin/bitprim-node-lbnet-run.sh start
```

If necessary its possible to check status, or to stop the process by using `status` or `stop` parameters.

Example:
```sh
$ sudo /opt/bitprim/bin/bitprim-node-lbnet-run.sh stop
```

#### Request information
`Bitprim-explorer` can be used to request information using the `bitprim-bx-bitcoin-lbnet` for the desired network. 

Example:
```sh
$ /opt/bitprim/bin/bitprim-bx-lbnet.sh fetch-height 
```


