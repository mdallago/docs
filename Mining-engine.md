# Mining Engine

Since we've developed RPC support, we were able to create a whole new [mining](https://github.com/bitprim/bitprim-mining) engine for Bitprim, which is capable of mining Bitcoin and Litecoin, mainnet and testnet. 
This engine in a new module and it respects the Bitprim’s modular implementation, so it allows developers to create their own mining engine if they want to replace ours, and it will connect the Bitprim node without problems as long as it uses the same interface.
Bitprim database can maintain big tables and our mining engine makes use of this exploiting the big utxo table to maximize fees gained per block.

## Configuration

First download and install Bitprim as its explained on [this guide](https://github.com/bitprim/bitprim-build).
From the [configuration file](https://github.com/bitprim/bitprim-build#configuration-files), you will be able to configure Bitprim mining.

Under the `mining` section, you can edit several options:
* `cores`: "The number of cores dedicated to validation, defaults to 0 (physical cores)."
* `block_timeout_seconds`: The time limit for block receipt during initial block download, defaults to 5.
* `transaction_pool_refresh`: Refresh the transaction pool on reorganization and channel start, defaults to true.
* `use_testnet_rules`: Use testnet rules for determination of work required, defaults to false.
* `rpc_port`: "TCP port for the HTTP-JSON-RPC connection, default to 8332 (8332 mainnet, 18332 testnet).
* `real_consensus_enabled`: Enable real consensus mining.
* `real_consensus_endpoint`: The real consensus client endpoint (ip:port pair).
* `real_consensus_user`: The real consensus client auth user.
* `real_consensus_pass`: The real consensus client authorization pass.

Bitprim uses the same default ports as other Bitcoins clients
To connect your Mining Pool to Bitprim disable user auth, and use the rpc port defined on the configuration file.

Real Consensus is a feature of Bitprim mining, and it is explained [here](real-consensus.md)


