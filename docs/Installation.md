## Installation Procedure

The\_Bitprim\_executables can be installed on Linux, macOS, FreeBSD, Windows and others. These binaries are pre-built for the most usual operating system/compiler combinations and hosted in an online repository. If there are no pre-built binaries for your platform, a build from source will be attempted.

So, for any platform, an installation can be performed in 2 simple steps:

1.Configure the Conan remote

```
conan remote add bitprim https://api.bintray.com/conan/bitprim/bitprim
```

2.Install the appropriate executable

```
# For Bitcoin Cash
conan install bitprim-node-exe/0.10.1@bitprim/stable -o currency=BCH 
# ... or (BCH is the default crypto)
conan install bitprim-node-exe/0.10.1@bitprim/stable 

# For Bitcoin Legacy
conan install bitprim-node-exe/0.10.1@bitprim/stable -o currency=BTC

# For Litecoin
conan install bitprim-node-exe/0.10.1@bitprim/stable -o currency=LTC
```

## Building from source Requirements

In case there are no pre-built binaries for your platform, it is necessary to build from source code. In such a scenario, the following requirements must be added to the previous ones:

* C++11 Conforming Compiler.
* [CMake](https://cmake.org/)
  building tool, version 3.4 or newer.

## Running the node

In order to run the full node, you have to initialize the database and then run the node:

1.Run the following to initialize the database:

`./bn -i`

2.Finally, run the node:

`./bn`

The above commands use the default configuration hardcoded in the executable. You can use a configuration file to customize the behavior of the node. In the [bitprim-config](https://github.com/bitprim/bitprim-config) repository you can find some example files.

3.Initialize the database using a configuration file:

`./bn -i -c <configuration file path>`

4.Run the node using a configuration file:

`./bn -c <configuration file path>`

