We are currently developing full RPC support, to be compatible with software that currently relies on other Bitcoin implementations.

Currently we are able to respond to the following messages:

* `getaddressbalance`
* `getaddresstxids`
* `getaddressdeltas`
* `getaddressutxos`
* `getblockhashes`
* `getaddressmempool`
* `getbestblockhash`
* `getblock`
* `getblockhash`
* `getblockchaininfo`
* `getblockheader`
* `getblockcount`
* `getblocktemplate`
* `getchaintips`
* `getdifficulty`
* `getinfo`
* `getmininginfo`
* `getrawtransaction`
* `getspentinfo`
* `validateaddress`
* `sendrawtransaction`
* `submitblock`

This allow us to successfully mine using our software.

