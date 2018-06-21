# Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`namespace `[`bitprim-py::bitprim`](#namespacebitprim-py_1_1bitprim) | 

# namespace `bitprim-py::bitprim` 

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public def `[`encode_hash`](#bitprim_8py_1a35a6363ee1ecccef9236b6d100989e75)`(hash)`            | Converts a bytearray into a readable format (hex string)
`public def `[`decode_hash`](#bitprim_8py_1a77eedeafd72bf91f59e51341e85154ae)`(hash_str)`            | Converts a string into a workable format (byte array)
`class `[`bitprim-py::bitprim::Binary`](#classbitprim-py_1_1bitprim_1_1Binary) | Represents a binary filter.
`class `[`bitprim-py::bitprim::Block`](#classbitprim-py_1_1bitprim_1_1Block) | Represent a full Bitcoin blockchain block.
`class `[`bitprim-py::bitprim::Chain`](#classbitprim-py_1_1bitprim_1_1Chain) | Represents the Bitcoin blockchain.
`class `[`bitprim-py::bitprim::Executor`](#classbitprim-py_1_1bitprim_1_1Executor) | Controls the execution of the Bitprim bitcoin node.
`class `[`bitprim-py::bitprim::Header`](#classbitprim-py_1_1bitprim_1_1Header) | Represents a Bitcoin block's header.
`class `[`bitprim-py::bitprim::History`](#classbitprim-py_1_1bitprim_1_1History) | [Output](#classbitprim-py_1_1bitprim_1_1Output) points, values, and spends for a payment address.
`class `[`bitprim-py::bitprim::Input`](#classbitprim-py_1_1bitprim_1_1Input) | Represents one of the inputs of a [Transaction](#classbitprim-py_1_1bitprim_1_1Transaction).
`class `[`bitprim-py::bitprim::MerkleBlock`](#classbitprim-py_1_1bitprim_1_1MerkleBlock) | Merkle tree representation of a transaction block.
`class `[`bitprim-py::bitprim::Output`](#classbitprim-py_1_1bitprim_1_1Output) | Represents one of the outputs of a [Transaction](#classbitprim-py_1_1bitprim_1_1Transaction).
`class `[`bitprim-py::bitprim::OutputPoint`](#classbitprim-py_1_1bitprim_1_1OutputPoint) | [Transaction](#classbitprim-py_1_1bitprim_1_1Transaction) hash and index pair representing one of the transaction outputs.
`class `[`bitprim-py::bitprim::P2p`](#classbitprim-py_1_1bitprim_1_1P2p) | Represents the Bitcoin `P2P` Networking API.
`class `[`bitprim-py::bitprim::PaymentAddress`](#classbitprim-py_1_1bitprim_1_1PaymentAddress) | Represents a Bitcoin wallet address.
`class `[`bitprim-py::bitprim::Point`](#classbitprim-py_1_1bitprim_1_1Point) | Represents one of the tx inputs.
`class `[`bitprim-py::bitprim::Script`](#classbitprim-py_1_1bitprim_1_1Script) | Represents a transaction script.
`class `[`bitprim-py::bitprim::Stealth`](#classbitprim-py_1_1bitprim_1_1Stealth) | [Stealth](#classbitprim-py_1_1bitprim_1_1Stealth) payment related data.
`class `[`bitprim-py::bitprim::StealthCompact`](#classbitprim-py_1_1bitprim_1_1StealthCompact) | Compressed representation of [Stealth](#classbitprim-py_1_1bitprim_1_1Stealth) payment related data.
`class `[`bitprim-py::bitprim::Transaction`](#classbitprim-py_1_1bitprim_1_1Transaction) | Represents a Bitcoin [Transaction](#classbitprim-py_1_1bitprim_1_1Transaction).
`class `[`bitprim-py::bitprim::Wallet`](#classbitprim-py_1_1bitprim_1_1Wallet) | [Wallet](#classbitprim-py_1_1bitprim_1_1Wallet) handling utilities.

## Members

#### `public def `[`encode_hash`](#bitprim_8py_1a35a6363ee1ecccef9236b6d100989e75)`(hash)` 

Converts a bytearray into a readable format (hex string)

#### Parameters
* `hash` (bytearray): Hash bytes 

#### Returns
(str) Hex string Example: "000000000019d6689c085ae165831e934ff763ae46a2a6c172b3f1b60a8ce26f"

#### `public def `[`decode_hash`](#bitprim_8py_1a77eedeafd72bf91f59e51341e85154ae)`(hash_str)` 

Converts a string into a workable format (byte array)

#### Parameters
* `hash_str` (str): hash hex string 

#### Returns
(bytearray): Byte array representing hash. Example "00 00 00 00 00 19 D6 68 ... E2 6F"

# class `bitprim-py::bitprim::Binary` 

Represents a binary filter.

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public def `[`construct`](#classbitprim-py_1_1bitprim_1_1Binary_1a9316644228cea96a0c795faef5a38ade)`()` | Create an empty binary object.
`public def `[`construct_string`](#classbitprim-py_1_1bitprim_1_1Binary_1a86c0b3de8e0dc2e5c84d2381ad03e85c)`(string_filter)` | Creates a binary filter from a binary string.
`public def `[`construct_blocks`](#classbitprim-py_1_1bitprim_1_1Binary_1a15b23af6128580697f431b8b1956634c)`(size,`[`blocks`](#classbitprim-py_1_1bitprim_1_1Binary_1a7c015d6228ba34e7474e2886ee6361f8)`)` | Creates a binary filter from an int array.
`public def `[`blocks`](#classbitprim-py_1_1bitprim_1_1Binary_1a7c015d6228ba34e7474e2886ee6361f8)`()` | Filter representation as uint array.
`public def `[`encoded`](#classbitprim-py_1_1bitprim_1_1Binary_1a87b87bdb3f1a568c20db4573655e9a61)`()` | Filter representation as binary string.

## Members

#### `public def `[`construct`](#classbitprim-py_1_1bitprim_1_1Binary_1a9316644228cea96a0c795faef5a38ade)`()` 

Create an empty binary object.

#### Returns
([Binary](#classbitprim-py_1_1bitprim_1_1Binary)) New instance

#### `public def `[`construct_string`](#classbitprim-py_1_1bitprim_1_1Binary_1a86c0b3de8e0dc2e5c84d2381ad03e85c)`(string_filter)` 

Creates a binary filter from a binary string.

#### Parameters
* `string_filter` [Binary](#classbitprim-py_1_1bitprim_1_1Binary) string. Example: '10111010101011011111000000001101' 

#### Returns
([Binary](#classbitprim-py_1_1bitprim_1_1Binary)) Instance representing the given filter string

#### `public def `[`construct_blocks`](#classbitprim-py_1_1bitprim_1_1Binary_1a15b23af6128580697f431b8b1956634c)`(size,`[`blocks`](#classbitprim-py_1_1bitprim_1_1Binary_1a7c015d6228ba34e7474e2886ee6361f8)`)` 

Creates a binary filter from an int array.

#### Parameters
* `size` (int) Filter length 

* `blocks` (int array) Filter representation. Example: '[186,173,240,13]' 

#### Returns
([Binary](#classbitprim-py_1_1bitprim_1_1Binary)) Instance representing the given filter

#### `public def `[`blocks`](#classbitprim-py_1_1bitprim_1_1Binary_1a7c015d6228ba34e7474e2886ee6361f8)`()` 

Filter representation as uint array.

#### Returns
(uint array)

#### `public def `[`encoded`](#classbitprim-py_1_1bitprim_1_1Binary_1a87b87bdb3f1a568c20db4573655e9a61)`()` 

Filter representation as binary string.

#### Returns
(str)

# class `bitprim-py::bitprim::Block` 

Represent a full Bitcoin blockchain block.

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public def `[`height`](#classbitprim-py_1_1bitprim_1_1Block_1adbee2f505eaed0757aa06581476061bf)`()` | The block's height in the chain.
`public def `[`header`](#classbitprim-py_1_1bitprim_1_1Block_1a66ff4a0260d856f0ba0501d83a37996e)`()` | The block's header.
`public def `[`transaction_count`](#classbitprim-py_1_1bitprim_1_1Block_1a7f586edd8ff2af4414d1f457466142ba)`()` | The total amount of transactions that the block contains.
`public def `[`hash`](#classbitprim-py_1_1bitprim_1_1Block_1a1b7c56cf57daa5abdba702996e088354)`()` | The block's hash as a 32 byte array.
`public def `[`serialized_size`](#classbitprim-py_1_1bitprim_1_1Block_1a0bb0ed4f08d877755b5f63ffb5a1c83e)`()` | [Block](#classbitprim-py_1_1bitprim_1_1Block) size in bytes.
`public def `[`fees`](#classbitprim-py_1_1bitprim_1_1Block_1a16259124f105d8f0713620748a7e0283)`()` | Miner fees included in the block's coinbase transaction.
`public def `[`claim`](#classbitprim-py_1_1bitprim_1_1Block_1af6123eaeb15dc6173aedb5249c76222a)`()` | Sum of coinbase outputs.
`public def `[`reward`](#classbitprim-py_1_1bitprim_1_1Block_1a2355ee175a47be556e227bc560ad91d9)`(`[`height`](#classbitprim-py_1_1bitprim_1_1Block_1adbee2f505eaed0757aa06581476061bf)`)` | Reward = Subsidy + Fees, for the block at the given height.
`public def `[`generate_merkle_root`](#classbitprim-py_1_1bitprim_1_1Block_1a9a2c4d24510492541117635a46bda8e4)`()` | The block's Merkle root, as a 32 byte array.
`public def `[`is_valid`](#classbitprim-py_1_1bitprim_1_1Block_1a32a1d3fce927c0368a9a17ee92f9e559)`()` | Return 1 if and only if the block has transactions and a valid header, 0 otherwise.
`public def `[`transaction_nth`](#classbitprim-py_1_1bitprim_1_1Block_1a83506a11e3c73dc177ae7641295e9b71)`(n)` | Given a position in the block, returns the corresponding transaction.
`public def `[`signature_operations`](#classbitprim-py_1_1bitprim_1_1Block_1a442b31f9cdd99017c4fe69d9fcc1708f)`()` | Amount of signature operations in the block.
`public def `[`signature_operations_bip16_active`](#classbitprim-py_1_1bitprim_1_1Block_1aa758b654d597a804582bd848088cdf5e)`(bip16_active)` | Amount of signature operations in the block.
`public def `[`total_inputs`](#classbitprim-py_1_1bitprim_1_1Block_1ae274945c0c5a93e97f0520ce6ab19ede)`(with_coinbase)` | Total amount of inputs in the block (consider all transactions).
`public def `[`is_extra_coinbases`](#classbitprim-py_1_1bitprim_1_1Block_1a0292edcc495d96184612853b4d4f85ac)`()` | Tell whether there is more than one coinbase transaction in the block.
`public def `[`is_final`](#classbitprim-py_1_1bitprim_1_1Block_1a00fe0c357648fe5ab621dce05838e406)`(`[`height`](#classbitprim-py_1_1bitprim_1_1Block_1adbee2f505eaed0757aa06581476061bf)`,block_time)` | Tell whether every transaction in the block is final or not.
`public def `[`is_distinct_transaction_set`](#classbitprim-py_1_1bitprim_1_1Block_1a1f4c4eca104136073014ed084f49f2eb)`()` | Tell whether all transactions in the block have a unique hash (i.e.
`public def `[`is_valid_coinbase_claim`](#classbitprim-py_1_1bitprim_1_1Block_1aa986d71754a4cf477d61ae34d6f37ca8)`(`[`height`](#classbitprim-py_1_1bitprim_1_1Block_1adbee2f505eaed0757aa06581476061bf)`)` | Given a block height, tell if its coinbase claim is not higher than the deserved reward.
`public def `[`is_valid_coinbase_script`](#classbitprim-py_1_1bitprim_1_1Block_1a5801ed77d131384d4f2e917e07f13c27)`(`[`height`](#classbitprim-py_1_1bitprim_1_1Block_1adbee2f505eaed0757aa06581476061bf)`)` | Returns 1 if and only if the coinbase script is valid.
`public def `[`is_valid_merkle_root`](#classbitprim-py_1_1bitprim_1_1Block_1a8b699ddd4ea235009db7197542f64e76)`()` | Tell if the generated Merkle root equals the header's Merkle root.

## Members

#### `public def `[`height`](#classbitprim-py_1_1bitprim_1_1Block_1adbee2f505eaed0757aa06581476061bf)`()` 

The block's height in the chain.

It identifies it univocally 
#### Returns
(int)

#### `public def `[`header`](#classbitprim-py_1_1bitprim_1_1Block_1a66ff4a0260d856f0ba0501d83a37996e)`()` 

The block's header.

#### Returns
([Header](#classbitprim-py_1_1bitprim_1_1Header))

#### `public def `[`transaction_count`](#classbitprim-py_1_1bitprim_1_1Block_1a7f586edd8ff2af4414d1f457466142ba)`()` 

The total amount of transactions that the block contains.

#### Returns
(unsigned int)

#### `public def `[`hash`](#classbitprim-py_1_1bitprim_1_1Block_1a1b7c56cf57daa5abdba702996e088354)`()` 

The block's hash as a 32 byte array.

#### Returns
(bytearray)

#### `public def `[`serialized_size`](#classbitprim-py_1_1bitprim_1_1Block_1a0bb0ed4f08d877755b5f63ffb5a1c83e)`()` 

[Block](#classbitprim-py_1_1bitprim_1_1Block) size in bytes.

#### Returns
(int)

#### `public def `[`fees`](#classbitprim-py_1_1bitprim_1_1Block_1a16259124f105d8f0713620748a7e0283)`()` 

Miner fees included in the block's coinbase transaction.

#### Returns
(unsigned int)

#### `public def `[`claim`](#classbitprim-py_1_1bitprim_1_1Block_1af6123eaeb15dc6173aedb5249c76222a)`()` 

Sum of coinbase outputs.

#### Returns
(unsigned int)

#### `public def `[`reward`](#classbitprim-py_1_1bitprim_1_1Block_1a2355ee175a47be556e227bc560ad91d9)`(`[`height`](#classbitprim-py_1_1bitprim_1_1Block_1adbee2f505eaed0757aa06581476061bf)`)` 

Reward = Subsidy + Fees, for the block at the given height.

#### Parameters
* `height` (unsigned int) [Block](#classbitprim-py_1_1bitprim_1_1Block) height in the chain. Identifies it univocally 

#### Returns
(unsigned int)

#### `public def `[`generate_merkle_root`](#classbitprim-py_1_1bitprim_1_1Block_1a9a2c4d24510492541117635a46bda8e4)`()` 

The block's Merkle root, as a 32 byte array.

#### Returns
(byte array)

#### `public def `[`is_valid`](#classbitprim-py_1_1bitprim_1_1Block_1a32a1d3fce927c0368a9a17ee92f9e559)`()` 

Return 1 if and only if the block has transactions and a valid header, 0 otherwise.

#### Returns
(int) TODO Why not a bool?

#### `public def `[`transaction_nth`](#classbitprim-py_1_1bitprim_1_1Block_1a83506a11e3c73dc177ae7641295e9b71)`(n)` 

Given a position in the block, returns the corresponding transaction.

#### Parameters
* `n` (unsigned int): [Transaction](#classbitprim-py_1_1bitprim_1_1Transaction) index inside the block (starting at zero) 

#### Returns
([Transaction](#classbitprim-py_1_1bitprim_1_1Transaction))

#### `public def `[`signature_operations`](#classbitprim-py_1_1bitprim_1_1Block_1a442b31f9cdd99017c4fe69d9fcc1708f)`()` 

Amount of signature operations in the block.

Returns max_int in case of overflow. 
#### Returns
(unsigned int)

#### `public def `[`signature_operations_bip16_active`](#classbitprim-py_1_1bitprim_1_1Block_1aa758b654d597a804582bd848088cdf5e)`(bip16_active)` 

Amount of signature operations in the block.

Returns max_int in case of overflow. 
#### Parameters
* `bip16_active` (int): should be '1' if and only if bip16 is activated at this point.

#### `public def `[`total_inputs`](#classbitprim-py_1_1bitprim_1_1Block_1ae274945c0c5a93e97f0520ce6ab19ede)`(with_coinbase)` 

Total amount of inputs in the block (consider all transactions).

#### Parameters
* `with_coinbase` (int): should be '1' if and only if the block contains a coinbase transaction, '0' otherwise. 

#### Returns
(unsigned int)

#### `public def `[`is_extra_coinbases`](#classbitprim-py_1_1bitprim_1_1Block_1a0292edcc495d96184612853b4d4f85ac)`()` 

Tell whether there is more than one coinbase transaction in the block.

#### Returns
(int) 1 if and only if there is another coinbase other than the first transaction, 0 otherwise.

#### `public def `[`is_final`](#classbitprim-py_1_1bitprim_1_1Block_1a00fe0c357648fe5ab621dce05838e406)`(`[`height`](#classbitprim-py_1_1bitprim_1_1Block_1adbee2f505eaed0757aa06581476061bf)`,block_time)` 

Tell whether every transaction in the block is final or not.

#### Parameters
* `height` (unsigned int): [Block](#classbitprim-py_1_1bitprim_1_1Block) height in the chain. Identifies it univocally. 

#### Returns
(int) 1 if every transaction in the block is final, 0 otherwise.

#### `public def `[`is_distinct_transaction_set`](#classbitprim-py_1_1bitprim_1_1Block_1a1f4c4eca104136073014ed084f49f2eb)`()` 

Tell whether all transactions in the block have a unique hash (i.e.

no duplicates) 
#### Returns
(int): 1 if there are no two transactions with the same hash in the block, 0 otherwise

#### `public def `[`is_valid_coinbase_claim`](#classbitprim-py_1_1bitprim_1_1Block_1aa986d71754a4cf477d61ae34d6f37ca8)`(`[`height`](#classbitprim-py_1_1bitprim_1_1Block_1adbee2f505eaed0757aa06581476061bf)`)` 

Given a block height, tell if its coinbase claim is not higher than the deserved reward.

#### Parameters
* `height` (unsigned int): [Block](#classbitprim-py_1_1bitprim_1_1Block) height in the chain. Identifies it univocally. 

#### Returns
(int) 1 if coinbase claim is not higher than the deserved reward.

#### `public def `[`is_valid_coinbase_script`](#classbitprim-py_1_1bitprim_1_1Block_1a5801ed77d131384d4f2e917e07f13c27)`(`[`height`](#classbitprim-py_1_1bitprim_1_1Block_1adbee2f505eaed0757aa06581476061bf)`)` 

Returns 1 if and only if the coinbase script is valid.

#### Returns
(int)

#### `public def `[`is_valid_merkle_root`](#classbitprim-py_1_1bitprim_1_1Block_1a8b699ddd4ea235009db7197542f64e76)`()` 

Tell if the generated Merkle root equals the header's Merkle root.

#### Returns
(int) 1 if and only if the generated Merkle root is equal to the [Header](#classbitprim-py_1_1bitprim_1_1Header)'s Merkle root

# class `bitprim-py::bitprim::Chain` 

Represents the Bitcoin blockchain.

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public  `[`history_fetch_handler_`](#classbitprim-py_1_1bitprim_1_1Chain_1affd953b04003452fafe5a3a559409ca2) | Internal callback which is called by the native fetch_history function and marshalls parameters to the managed callback.
`public  `[`fetch_block_header_handler_`](#classbitprim-py_1_1bitprim_1_1Chain_1a89897722d7aed04f04ae393852c16204) | Internal callback which is called by the native fetch_block_header function and marshalls parameters to the managed callback.
`public def `[`fetch_last_height`](#classbitprim-py_1_1bitprim_1_1Chain_1ac61495c0b64988230423073f3b03ff07)`(handler)` | Gets the height of the highest block in the local copy of the blockchain.
`public def `[`fetch_history`](#classbitprim-py_1_1bitprim_1_1Chain_1a965cf6db03e48540bb14d3b3edaa8bcc)`(address,limit,from_height,handler)` | Get a list of output points, values, and spends for a given payment address.
`public def `[`fetch_stealth`](#classbitprim-py_1_1bitprim_1_1Chain_1af176a2ccfcfb1f50830367a19c35a794)`(binary_filter_str,from_height,handler)` | Get metadata on potential payment transactions by stealth filter.
`public def `[`fetch_block_height`](#classbitprim-py_1_1bitprim_1_1Chain_1afdf1cef6c699bdfbf2e9d84e4301ac31)`(hash,handler)` | Given a block hash, it queries the chain for the block height.
`public def `[`fetch_block_header_by_height`](#classbitprim-py_1_1bitprim_1_1Chain_1aaebc8d01e70714a76baf7f18254d17a1)`(height,handler)` | Get the block header from the specified height in the chain.
`public def `[`fetch_block_header_by_hash`](#classbitprim-py_1_1bitprim_1_1Chain_1a906414b6f4be27e8f4cdea304e693c60)`(hash,handler)` | Get the block header from the specified block hash.
`public def `[`fetch_block_by_height`](#classbitprim-py_1_1bitprim_1_1Chain_1a0194a90c0647ecf28f5561fec03795fe)`(height,handler)` | Gets a block from the specified height in the chain.
`public def `[`fetch_block_by_hash`](#classbitprim-py_1_1bitprim_1_1Chain_1ada2a30b95551270e866128b9faf78e91)`(hash,handler)` | Gets a block from the specified hash.
`public def `[`fetch_merkle_block_by_height`](#classbitprim-py_1_1bitprim_1_1Chain_1a8736e68dd88164e25c20a342f71d51fb)`(height,handler)` | Given a block height in the chain, it retrieves the block's associated Merkle block.
`public def `[`fetch_merkle_block_by_hash`](#classbitprim-py_1_1bitprim_1_1Chain_1a34fe828b455288f6b0e4394309827823)`(hash,handler)` | Given a block hash, it retrieves the block's associated Merkle block.
`public def `[`fetch_transaction`](#classbitprim-py_1_1bitprim_1_1Chain_1aa3a1843a9773e0356f583279842e0937)`(hashn,require_confirmed,handler)` | Get a transaction by its hash.
`public def `[`fetch_transaction_position`](#classbitprim-py_1_1bitprim_1_1Chain_1a3ccaf20e10f6c95349c58a548213e12d)`(hashn,require_confirmed,handler)` | Given a transaction hash, it fetches the height and position inside the block.
`public def `[`validate_tx`](#classbitprim-py_1_1bitprim_1_1Chain_1a34527842538c37c393577c62ad0827a5)`(transaction,handler)` | Determine if a transaction is valid for submission to the blockchain.
`public def `[`fetch_spend`](#classbitprim-py_1_1bitprim_1_1Chain_1a03e03c44ed6ff0049d091b2cf9e1b10d)`(output_point,handler)` | Fetch the transaction input which spends the indicated output.
`public def `[`subscribe_blockchain`](#classbitprim-py_1_1bitprim_1_1Chain_1a5f64a4f2a1e978265468fff03f6a8979)`(handler)` | 
`public def `[`unsubscribe`](#classbitprim-py_1_1bitprim_1_1Chain_1a89c0f67530a7e6c420b72d0d93cc9ba0)`()` | 

## Members

#### `public  `[`history_fetch_handler_`](#classbitprim-py_1_1bitprim_1_1Chain_1affd953b04003452fafe5a3a559409ca2) 

Internal callback which is called by the native fetch_history function and marshalls parameters to the managed callback.

#### `public  `[`fetch_block_header_handler_`](#classbitprim-py_1_1bitprim_1_1Chain_1a89897722d7aed04f04ae393852c16204) 

Internal callback which is called by the native fetch_block_header function and marshalls parameters to the managed callback.

#### `public def `[`fetch_last_height`](#classbitprim-py_1_1bitprim_1_1Chain_1ac61495c0b64988230423073f3b03ff07)`(handler)` 

Gets the height of the highest block in the local copy of the blockchain.

This number will grow as the node synchronizes with the blockchain. This is an asynchronous method; a callback must be provided to receive the result

Args: handler (Callable (error, block_height)): Will be executed when the chain is queried.

* error (int): Error code. 0 if and only if successful.

* block_height (unsigned int): Height of the highest block in the chain.

#### `public def `[`fetch_history`](#classbitprim-py_1_1bitprim_1_1Chain_1a965cf6db03e48540bb14d3b3edaa8bcc)`(address,limit,from_height,handler)` 

Get a list of output points, values, and spends for a given payment address.

This is an asynchronous method; a callback must be provided to receive the result

Args: address ([PaymentAddress](#classbitprim-py_1_1bitprim_1_1PaymentAddress)): [Wallet](#classbitprim-py_1_1bitprim_1_1Wallet) to search. limit (unsigned int): Max amount of results to fetch. from_height (unsigned int): Starting height to search for transactions. handler (Callable (error, list)): Will be executed when the chain is queried.

* error (int): Error code. 0 if and only if successful.

* list (HistoryList): A list with every element found.

#### `public def `[`fetch_stealth`](#classbitprim-py_1_1bitprim_1_1Chain_1af176a2ccfcfb1f50830367a19c35a794)`(binary_filter_str,from_height,handler)` 

Get metadata on potential payment transactions by stealth filter.

Given a filter and a height in the chain, it queries the chain for transactions matching the given filter. Args: binary_filter_str (string): Must be at least 8 bits in length. example "10101010" from_height (unsigned int): Starting height in the chain to search for transactions. handler (Callable (error, list)): Will be executed when the chain is queried.

* error (int): Error code. 0 if and only if successful.

* list (StealthList): list with every transaction matching the given filter.

#### `public def `[`fetch_block_height`](#classbitprim-py_1_1bitprim_1_1Chain_1afdf1cef6c699bdfbf2e9d84e4301ac31)`(hash,handler)` 

Given a block hash, it queries the chain for the block height.

Args: hash (bytearray): 32 bytes of the block hash. handler (Callable (error, block_height)): Will be executed after the chain is cued.

* error (int): Error code. 0 if and only if successful.

* block_height (unsigned int): height of the block in the chain.

#### `public def `[`fetch_block_header_by_height`](#classbitprim-py_1_1bitprim_1_1Chain_1aaebc8d01e70714a76baf7f18254d17a1)`(height,handler)` 

Get the block header from the specified height in the chain.

Args: height (unsigned int): [Block](#classbitprim-py_1_1bitprim_1_1Block) height in the chain. handler (Callable (error, block_header)): Will be executed after the chain is queried.

* error (int): Error code. 0 if successful.

* block_header ([Header](#classbitprim-py_1_1bitprim_1_1Header)): The found block's header.

#### `public def `[`fetch_block_header_by_hash`](#classbitprim-py_1_1bitprim_1_1Chain_1a906414b6f4be27e8f4cdea304e693c60)`(hash,handler)` 

Get the block header from the specified block hash.

Args: hash (bytearray): 32 bytes of the block hash. handler (Callable (error, block_header)): Will be executed after the chain is queried.

* error (int): Error code. 0 if successful.

* block_header ([Header](#classbitprim-py_1_1bitprim_1_1Header)): The found block's header.

#### `public def `[`fetch_block_by_height`](#classbitprim-py_1_1bitprim_1_1Chain_1a0194a90c0647ecf28f5561fec03795fe)`(height,handler)` 

Gets a block from the specified height in the chain.

Args: height (unsigned int): [Block](#classbitprim-py_1_1bitprim_1_1Block) height in the chain. handler (Callable (error, block)): Will be executed after the chain is queried.

* error (int): Error code. 0 if successful.

* block ([Block](#classbitprim-py_1_1bitprim_1_1Block)): [Block](#classbitprim-py_1_1bitprim_1_1Block) at the given height in the chain.

#### `public def `[`fetch_block_by_hash`](#classbitprim-py_1_1bitprim_1_1Chain_1ada2a30b95551270e866128b9faf78e91)`(hash,handler)` 

Gets a block from the specified hash.

Args: hash (bytearray): 32 bytes of the block hash. handler (Callable (error, block)): Will be executed after the chain is queried.

* error (int): Error code. 0 if successful.

* block ([Block](#classbitprim-py_1_1bitprim_1_1Block)): [Block](#classbitprim-py_1_1bitprim_1_1Block) found with the specified hash.

#### `public def `[`fetch_merkle_block_by_height`](#classbitprim-py_1_1bitprim_1_1Chain_1a8736e68dd88164e25c20a342f71d51fb)`(height,handler)` 

Given a block height in the chain, it retrieves the block's associated Merkle block.

Args: height (unsigned int): [Block](#classbitprim-py_1_1bitprim_1_1Block) height in the chain. handler (Callable (error, merkle_block, block_height)): Will be executed when the chain is queried.

* error (int): Error code. 0 if successful.

* merkle_block ([MerkleBlock](#classbitprim-py_1_1bitprim_1_1MerkleBlock)): The requested block's Merkle block.

* block_height (unsigned int): The block's height in the chain.

#### `public def `[`fetch_merkle_block_by_hash`](#classbitprim-py_1_1bitprim_1_1Chain_1a34fe828b455288f6b0e4394309827823)`(hash,handler)` 

Given a block hash, it retrieves the block's associated Merkle block.

Args: hash (bytearray): 32 bytes of the block hash. handler (Callable (error, merkle_block, block_height)): Will be executed when the chain is queried.

* error (int): Error code. 0 if successful.

* merkle_block ([MerkleBlock](#classbitprim-py_1_1bitprim_1_1MerkleBlock)): The requested block's Merkle block.

* block_height (unsigned int): The block's height in the chain.

#### `public def `[`fetch_transaction`](#classbitprim-py_1_1bitprim_1_1Chain_1aa3a1843a9773e0356f583279842e0937)`(hashn,require_confirmed,handler)` 

Get a transaction by its hash.

Args: hashn (bytearray): 32 bytes of the transaction hash. require_confirmed (int): If transaction should be in a block. 0 if not. handler (Callable (error, transaction, block_height, tx_index)): Will be executed when the chain is queried.

* error (int): Error code. 0 if successful.

* transaction ([Transaction](#classbitprim-py_1_1bitprim_1_1Transaction)): [Transaction](#classbitprim-py_1_1bitprim_1_1Transaction) found.

* block_height (unsigned int): height in the chain of the block containing the transaction.

* tx_index (unsigned int): index of the transaction inside the block (starting at zero).

#### `public def `[`fetch_transaction_position`](#classbitprim-py_1_1bitprim_1_1Chain_1a3ccaf20e10f6c95349c58a548213e12d)`(hashn,require_confirmed,handler)` 

Given a transaction hash, it fetches the height and position inside the block.

Args: hash (bytearray): 32 bytes of the transaction hash. require_confirmed (int): 1 if and only if transaction should be in a block, 0 otherwise. handler (Callable (error, block_height, tx_index)): Will be executed after the chain is queried.

* error (int): Error code. 0 if successful.

* block_height (unsigned int): Height of the block containing the transaction.

* tx_index (unsigned int): [Transaction](#classbitprim-py_1_1bitprim_1_1Transaction) index inside the block (starting at zero).

#### `public def `[`validate_tx`](#classbitprim-py_1_1bitprim_1_1Chain_1a34527842538c37c393577c62ad0827a5)`(transaction,handler)` 

Determine if a transaction is valid for submission to the blockchain.

Args: transaction ([Transaction](#classbitprim-py_1_1bitprim_1_1Transaction)): transaction to be checked. handler (Callable (error, message)): Will be executed after the chain is queried.

* error (int): error code. 0 if successful.

* message (str): string describing the result of the query. Example: 'The transaction is valid'

#### `public def `[`fetch_spend`](#classbitprim-py_1_1bitprim_1_1Chain_1a03e03c44ed6ff0049d091b2cf9e1b10d)`(output_point,handler)` 

Fetch the transaction input which spends the indicated output.

The `fetch_spend_handler` callback will be executed after querying the chain. Args: output_point ([OutputPoint](#classbitprim-py_1_1bitprim_1_1OutputPoint)): tx hash and index pair. handler (Callable (error, input_point)): Will be executed when the chain is queried.

* error (int): Error code. 0 if successful.

* input_point ([Point](#classbitprim-py_1_1bitprim_1_1Point)): Tx hash and index pair where the output was spent.

#### `public def `[`subscribe_blockchain`](#classbitprim-py_1_1bitprim_1_1Chain_1a5f64a4f2a1e978265468fff03f6a8979)`(handler)` 

#### `public def `[`unsubscribe`](#classbitprim-py_1_1bitprim_1_1Chain_1a89c0f67530a7e6c420b72d0d93cc9ba0)`()` 

# class `bitprim-py::bitprim::Executor` 

Controls the execution of the Bitprim bitcoin node.

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public def `[`__init__`](#classbitprim-py_1_1bitprim_1_1Executor_1a72c2f23cb1edf83547118813f6e93eae)`(path,sout,serr)` | Node executor constructor.
`public def `[`init_chain`](#classbitprim-py_1_1bitprim_1_1Executor_1a7c32502c052194f5135ac02896935f57)`()` | Initializes blockchain local copy.
`public def `[`run`](#classbitprim-py_1_1bitprim_1_1Executor_1ae5e0072a42604d141baf924fc4c58e6c)`()` | Starts running the node; blockchain starts synchronizing (downloading).
`public def `[`run_wait`](#classbitprim-py_1_1bitprim_1_1Executor_1a8113286b620ec22753af007ddeae073b)`()` | Starts running the node; blockchain start synchronizing (downloading).
`public def `[`stop`](#classbitprim-py_1_1bitprim_1_1Executor_1a4f60688eaed3452c1f8b54d1ed925a55)`()` | Stops the node; that includes all activies, such as synchronization and networking precondition: self._running.
`public def `[`stopped`](#classbitprim-py_1_1bitprim_1_1Executor_1aa0cb066e377ffd93c907eaf90be34382)`()` | To know if the node is stopped.
`public def `[`chain`](#classbitprim-py_1_1bitprim_1_1Executor_1ae5d4f74596113f6aa1b63034240885f1)`()` | Return the chain object representation.
`public def `[`p2p`](#classbitprim-py_1_1bitprim_1_1Executor_1aba4d20326e54e244c389f5f0149d65c3)`()` | Return the p2p object representation.
`public def `[`__enter__`](#classbitprim-py_1_1bitprim_1_1Executor_1aef4dd157e70a41c03b6ec61d1a5c3dd4)`()` | Implements acquisition part of the RAII idiom (acquires the executor object)
`public def `[`__exit__`](#classbitprim-py_1_1bitprim_1_1Executor_1a987258e17974de21c21553aed017456b)`(exc_type,exc_value,traceback)` | Implements the release part of the RAII idiom (releases the executor object)

## Members

#### `public def `[`__init__`](#classbitprim-py_1_1bitprim_1_1Executor_1a72c2f23cb1edf83547118813f6e93eae)`(path,sout,serr)` 

Node executor constructor.

#### Parameters
* `path` (string): Absolute path to node configuration file. 

* `sout` (file handle): File handle for redirecting standard output. If None, output goes to the a log file in the current directory. 

* `serr` (file handle): File handle for redirecting standard error output. If None, output goes to log file in the current directory.

#### `public def `[`init_chain`](#classbitprim-py_1_1bitprim_1_1Executor_1a7c32502c052194f5135ac02896935f57)`()` 

Initializes blockchain local copy.

#### Returns
(bool) true if and only if successful.

#### `public def `[`run`](#classbitprim-py_1_1bitprim_1_1Executor_1ae5e0072a42604d141baf924fc4c58e6c)`()` 

Starts running the node; blockchain starts synchronizing (downloading).

Returns right away (doesn't wait for init process to end) 
#### Returns
(bool) true if and only if successful.

#### `public def `[`run_wait`](#classbitprim-py_1_1bitprim_1_1Executor_1a8113286b620ec22753af007ddeae073b)`()` 

Starts running the node; blockchain start synchronizing (downloading).

Call blocks until init process is completed or fails. 
#### Returns
(bool) true if and only if successful.

#### `public def `[`stop`](#classbitprim-py_1_1bitprim_1_1Executor_1a4f60688eaed3452c1f8b54d1ed925a55)`()` 

Stops the node; that includes all activies, such as synchronization and networking precondition: self._running.

#### Returns
(bool) true if and only if successful

#### `public def `[`stopped`](#classbitprim-py_1_1bitprim_1_1Executor_1aa0cb066e377ffd93c907eaf90be34382)`()` 

To know if the node is stopped.

#### Returns
(bool) true if the node is stopped

#### `public def `[`chain`](#classbitprim-py_1_1bitprim_1_1Executor_1ae5d4f74596113f6aa1b63034240885f1)`()` 

Return the chain object representation.

#### Returns
([Chain](#classbitprim-py_1_1bitprim_1_1Chain))

#### `public def `[`p2p`](#classbitprim-py_1_1bitprim_1_1Executor_1aba4d20326e54e244c389f5f0149d65c3)`()` 

Return the p2p object representation.

#### Returns
([P2p](#classbitprim-py_1_1bitprim_1_1P2p))

#### `public def `[`__enter__`](#classbitprim-py_1_1bitprim_1_1Executor_1aef4dd157e70a41c03b6ec61d1a5c3dd4)`()` 

Implements acquisition part of the RAII idiom (acquires the executor object)

#### Returns
([Executor](#classbitprim-py_1_1bitprim_1_1Executor)) a newly acquired instance ready to use

#### `public def `[`__exit__`](#classbitprim-py_1_1bitprim_1_1Executor_1a987258e17974de21c21553aed017456b)`(exc_type,exc_value,traceback)` 

Implements the release part of the RAII idiom (releases the executor object)

#### Parameters
* `exc_type` Ignored 

* `exc_value` Ignored 

* `traceback` Ignored

# class `bitprim-py::bitprim::Header` 

Represents a Bitcoin block's header.

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public def `[`height`](#classbitprim-py_1_1bitprim_1_1Header_1ad3fe6079bf8dd360481a8f4a1a83a48e)`()` | [Block](#classbitprim-py_1_1bitprim_1_1Block) height in the chain.
`public def `[`version`](#classbitprim-py_1_1bitprim_1_1Header_1adef8d2dd843f47fb7d360095a50eb924)`()` | [Header](#classbitprim-py_1_1bitprim_1_1Header) protocol version.
`public def `[`set_version`](#classbitprim-py_1_1bitprim_1_1Header_1a82f67cf031b79cb2f1db5683a1776f24)`(`[`version`](#classbitprim-py_1_1bitprim_1_1Header_1adef8d2dd843f47fb7d360095a50eb924)`)` | Set version.
`public def `[`previous_block_hash`](#classbitprim-py_1_1bitprim_1_1Header_1ad83d031d2a01ce270f83ada967cc80fb)`()` | 32 bytes hash of the previous block in the chain.
`public def `[`merkle`](#classbitprim-py_1_1bitprim_1_1Header_1acc826caa5c5668f4e4343c291c8e22bb)`()` | Merkle root in 32 byte array format.
`public def `[`hash`](#classbitprim-py_1_1bitprim_1_1Header_1ad22ece8e1effb91727cd387be35b84c3)`()` | [Block](#classbitprim-py_1_1bitprim_1_1Block) hash in 32 byte array format.
`public def `[`timestamp`](#classbitprim-py_1_1bitprim_1_1Header_1a6c1e6f3893a2baf66cf195cbcf3b088d)`()` | [Block](#classbitprim-py_1_1bitprim_1_1Block) timestamp in UNIX Epoch (seconds since January 1st 1970) Assume UTC 0.
`public def `[`set_timestamp`](#classbitprim-py_1_1bitprim_1_1Header_1a9fa47d19f94503612e0188184b49c451)`(`[`timestamp`](#classbitprim-py_1_1bitprim_1_1Header_1a6c1e6f3893a2baf66cf195cbcf3b088d)`)` | Set header timestamp.
`public def `[`bits`](#classbitprim-py_1_1bitprim_1_1Header_1aaec0b170366dd10bec3732d43a41f8fa)`()` | Difficulty threshold.
`public def `[`set_bits`](#classbitprim-py_1_1bitprim_1_1Header_1a7f373da41c2c472e1eaba4cfe06cbf7c)`(`[`bits`](#classbitprim-py_1_1bitprim_1_1Header_1aaec0b170366dd10bec3732d43a41f8fa)`)` | Set header bits.
`public def `[`nonce`](#classbitprim-py_1_1bitprim_1_1Header_1ad18f1cc735e0e1b18cc4e5638f74363d)`()` | The nonce that allowed this block to be added to the blockchain.
`public def `[`set_nonce`](#classbitprim-py_1_1bitprim_1_1Header_1a50e3efb83494717264730251b752f789)`(`[`nonce`](#classbitprim-py_1_1bitprim_1_1Header_1ad18f1cc735e0e1b18cc4e5638f74363d)`)` | Set header nonce.

## Members

#### `public def `[`height`](#classbitprim-py_1_1bitprim_1_1Header_1ad3fe6079bf8dd360481a8f4a1a83a48e)`()` 

[Block](#classbitprim-py_1_1bitprim_1_1Block) height in the chain.

#### Returns
(unsigned int)

#### `public def `[`version`](#classbitprim-py_1_1bitprim_1_1Header_1adef8d2dd843f47fb7d360095a50eb924)`()` 

[Header](#classbitprim-py_1_1bitprim_1_1Header) protocol version.

#### Returns
(unsigned int)

#### `public def `[`set_version`](#classbitprim-py_1_1bitprim_1_1Header_1a82f67cf031b79cb2f1db5683a1776f24)`(`[`version`](#classbitprim-py_1_1bitprim_1_1Header_1adef8d2dd843f47fb7d360095a50eb924)`)` 

Set version.

#### Parameters
* `version` New version value

#### `public def `[`previous_block_hash`](#classbitprim-py_1_1bitprim_1_1Header_1ad83d031d2a01ce270f83ada967cc80fb)`()` 

32 bytes hash of the previous block in the chain.

#### Returns
(bytearray)

#### `public def `[`merkle`](#classbitprim-py_1_1bitprim_1_1Header_1acc826caa5c5668f4e4343c291c8e22bb)`()` 

Merkle root in 32 byte array format.

#### Returns
(bytearray)

#### `public def `[`hash`](#classbitprim-py_1_1bitprim_1_1Header_1ad22ece8e1effb91727cd387be35b84c3)`()` 

[Block](#classbitprim-py_1_1bitprim_1_1Block) hash in 32 byte array format.

#### Returns
(bytearray

#### `public def `[`timestamp`](#classbitprim-py_1_1bitprim_1_1Header_1a6c1e6f3893a2baf66cf195cbcf3b088d)`()` 

[Block](#classbitprim-py_1_1bitprim_1_1Block) timestamp in UNIX Epoch (seconds since January 1st 1970) Assume UTC 0.

#### Returns
(unsigned int)

#### `public def `[`set_timestamp`](#classbitprim-py_1_1bitprim_1_1Header_1a9fa47d19f94503612e0188184b49c451)`(`[`timestamp`](#classbitprim-py_1_1bitprim_1_1Header_1a6c1e6f3893a2baf66cf195cbcf3b088d)`)` 

Set header timestamp.

#### Parameters
* `timestamp` New header timestamp value

#### `public def `[`bits`](#classbitprim-py_1_1bitprim_1_1Header_1aaec0b170366dd10bec3732d43a41f8fa)`()` 

Difficulty threshold.

#### Returns
(unsigned int)

#### `public def `[`set_bits`](#classbitprim-py_1_1bitprim_1_1Header_1a7f373da41c2c472e1eaba4cfe06cbf7c)`(`[`bits`](#classbitprim-py_1_1bitprim_1_1Header_1aaec0b170366dd10bec3732d43a41f8fa)`)` 

Set header bits.

#### Parameters
* `bits` New header bits value

#### `public def `[`nonce`](#classbitprim-py_1_1bitprim_1_1Header_1ad18f1cc735e0e1b18cc4e5638f74363d)`()` 

The nonce that allowed this block to be added to the blockchain.

#### Returns
(unsigned int)

#### `public def `[`set_nonce`](#classbitprim-py_1_1bitprim_1_1Header_1a50e3efb83494717264730251b752f789)`(`[`nonce`](#classbitprim-py_1_1bitprim_1_1Header_1ad18f1cc735e0e1b18cc4e5638f74363d)`)` 

Set header nonce.

#### Parameters
* `nonce` New header nonce value

# class `bitprim-py::bitprim::History` 

[Output](#classbitprim-py_1_1bitprim_1_1Output) points, values, and spends for a payment address.

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public def `[`point_kind`](#classbitprim-py_1_1bitprim_1_1History_1ad238b84935d85af45317a4c40b407044)`()` | Used for differentiation.
`public def `[`point`](#classbitprim-py_1_1bitprim_1_1History_1a1641137742fea1930eb579efa771a39b)`()` | The point that identifies the [History](#classbitprim-py_1_1bitprim_1_1History) instance.
`public def `[`height`](#classbitprim-py_1_1bitprim_1_1History_1ad4c4d4d355c109413520392b9da29f9e)`()` | Height of the block containing the [Point](#classbitprim-py_1_1bitprim_1_1Point).
`public def `[`value_or_previous_checksum`](#classbitprim-py_1_1bitprim_1_1History_1aa524f25be3735504843a427030bf3663)`()` | Varies depending of point_kind.

## Members

#### `public def `[`point_kind`](#classbitprim-py_1_1bitprim_1_1History_1ad238b84935d85af45317a4c40b407044)`()` 

Used for differentiation.

'0' output '1' spend 
#### Returns
(unsigned int)

#### `public def `[`point`](#classbitprim-py_1_1bitprim_1_1History_1a1641137742fea1930eb579efa771a39b)`()` 

The point that identifies the [History](#classbitprim-py_1_1bitprim_1_1History) instance.

#### Returns
([Point](#classbitprim-py_1_1bitprim_1_1Point))

#### `public def `[`height`](#classbitprim-py_1_1bitprim_1_1History_1ad4c4d4d355c109413520392b9da29f9e)`()` 

Height of the block containing the [Point](#classbitprim-py_1_1bitprim_1_1Point).

#### Returns
(unsigned int)

#### `public def `[`value_or_previous_checksum`](#classbitprim-py_1_1bitprim_1_1History_1aa524f25be3735504843a427030bf3663)`()` 

Varies depending of point_kind.

value: if output, then satoshi value of output. previous_checksum: if spend, then checksum hash of previous output_point. 
#### Returns
(unsigned int)

# class `bitprim-py::bitprim::Input` 

Represents one of the inputs of a [Transaction](#classbitprim-py_1_1bitprim_1_1Transaction).

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public def `[`is_valid`](#classbitprim-py_1_1bitprim_1_1Input_1ad31d4fd3352cdb164bc8cd7f597b2245)`()` | Returns 0 if and only if previous outputs or script are invalid.
`public def `[`is_final`](#classbitprim-py_1_1bitprim_1_1Input_1a358c573c56fbf98c8026a0e6377e7203)`()` | Returns 1 if and only if sequence is equal to max_sequence.
`public def `[`serialized_size`](#classbitprim-py_1_1bitprim_1_1Input_1a4ae1e6fd2bc06dee3c8892d375831687)`()` | Size in bytes.
`public def `[`sequence`](#classbitprim-py_1_1bitprim_1_1Input_1a0dcf9a7c5e43e648a9ac2524cc641ea6)`()` | Sequence number of inputs.
`public def `[`signature_operations`](#classbitprim-py_1_1bitprim_1_1Input_1add34303f9c31390fc6bfca9c37c4813e)`(bip16_active)` | Total amount of sigops in the script.
`public def `[`script`](#classbitprim-py_1_1bitprim_1_1Input_1a3791f42e9d7bae367d1a24ab739edc0d)`()` | The input's script.
`public def `[`previous_output`](#classbitprim-py_1_1bitprim_1_1Input_1acbc3904f5c0a3c38a087d533e906ed66)`()` | Returns the previous output, with its transaction hash and index.

## Members

#### `public def `[`is_valid`](#classbitprim-py_1_1bitprim_1_1Input_1ad31d4fd3352cdb164bc8cd7f597b2245)`()` 

Returns 0 if and only if previous outputs or script are invalid.

#### Returns
(int)

#### `public def `[`is_final`](#classbitprim-py_1_1bitprim_1_1Input_1a358c573c56fbf98c8026a0e6377e7203)`()` 

Returns 1 if and only if sequence is equal to max_sequence.

#### Returns
int

#### `public def `[`serialized_size`](#classbitprim-py_1_1bitprim_1_1Input_1a4ae1e6fd2bc06dee3c8892d375831687)`()` 

Size in bytes.

#### Returns
(unsigned int)

#### `public def `[`sequence`](#classbitprim-py_1_1bitprim_1_1Input_1a0dcf9a7c5e43e648a9ac2524cc641ea6)`()` 

Sequence number of inputs.

If it equals max_sequence, txs is final 
#### Returns
(unsigned int)

#### `public def `[`signature_operations`](#classbitprim-py_1_1bitprim_1_1Input_1add34303f9c31390fc6bfca9c37c4813e)`(bip16_active)` 

Total amount of sigops in the script.

#### Parameters
* `bip16_active` (int): 1 if and only if bip 16 is active. 0 if not. 

#### Returns
(unsigned int)

#### `public def `[`script`](#classbitprim-py_1_1bitprim_1_1Input_1a3791f42e9d7bae367d1a24ab739edc0d)`()` 

The input's script.

#### Returns
([Script](#classbitprim-py_1_1bitprim_1_1Script))

#### `public def `[`previous_output`](#classbitprim-py_1_1bitprim_1_1Input_1acbc3904f5c0a3c38a087d533e906ed66)`()` 

Returns the previous output, with its transaction hash and index.

#### Returns
([OutputPoint](#classbitprim-py_1_1bitprim_1_1OutputPoint))

# class `bitprim-py::bitprim::MerkleBlock` 

Merkle tree representation of a transaction block.

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public def `[`height`](#classbitprim-py_1_1bitprim_1_1MerkleBlock_1abfc566beda5c199193ec2be8e421ffc2)`()` | Height of the block in the chain.
`public def `[`header`](#classbitprim-py_1_1bitprim_1_1MerkleBlock_1afdc8d1a7f34d22b6de787aa659a18418)`()` | The block's header.
`public def `[`is_valid`](#classbitprim-py_1_1bitprim_1_1MerkleBlock_1a5d192339bee7659d9d7e11a12a3adaad)`()` | Returns true if and only if it the block contains txs hashes, and header is valid.
`public def `[`hash_count`](#classbitprim-py_1_1bitprim_1_1MerkleBlock_1aa79c9306522448016e065715e3f0684d)`()` | [Transaction](#classbitprim-py_1_1bitprim_1_1Transaction) hashes list element count.
`public def `[`serialized_size`](#classbitprim-py_1_1bitprim_1_1MerkleBlock_1aee85571af3517d3a9985c11596b2d02c)`(version)` | [Block](#classbitprim-py_1_1bitprim_1_1Block) size in bytes.
`public def `[`total_transaction_count`](#classbitprim-py_1_1bitprim_1_1MerkleBlock_1a74e7756dc8cef287f922f08077419309)`()` | Amount of transactions inside the block.
`public def `[`reset`](#classbitprim-py_1_1bitprim_1_1MerkleBlock_1a327461611bfb0fbd67c75c180eceb3df)`()` | Delete all the data inside the block.

## Members

#### `public def `[`height`](#classbitprim-py_1_1bitprim_1_1MerkleBlock_1abfc566beda5c199193ec2be8e421ffc2)`()` 

Height of the block in the chain.

#### Returns
(unsigned int)

#### `public def `[`header`](#classbitprim-py_1_1bitprim_1_1MerkleBlock_1afdc8d1a7f34d22b6de787aa659a18418)`()` 

The block's header.

#### Returns
([Header](#classbitprim-py_1_1bitprim_1_1Header))

#### `public def `[`is_valid`](#classbitprim-py_1_1bitprim_1_1MerkleBlock_1a5d192339bee7659d9d7e11a12a3adaad)`()` 

Returns true if and only if it the block contains txs hashes, and header is valid.

#### Returns
(int)

#### `public def `[`hash_count`](#classbitprim-py_1_1bitprim_1_1MerkleBlock_1aa79c9306522448016e065715e3f0684d)`()` 

[Transaction](#classbitprim-py_1_1bitprim_1_1Transaction) hashes list element count.

#### Returns
(unsigned int)

#### `public def `[`serialized_size`](#classbitprim-py_1_1bitprim_1_1MerkleBlock_1aee85571af3517d3a9985c11596b2d02c)`(version)` 

[Block](#classbitprim-py_1_1bitprim_1_1Block) size in bytes.

#### Parameters
* `version` (unsigned int): block protocol version. 

#### Returns
(unsigned int)

#### `public def `[`total_transaction_count`](#classbitprim-py_1_1bitprim_1_1MerkleBlock_1a74e7756dc8cef287f922f08077419309)`()` 

Amount of transactions inside the block.

#### Returns
(unsigned int)

#### `public def `[`reset`](#classbitprim-py_1_1bitprim_1_1MerkleBlock_1a327461611bfb0fbd67c75c180eceb3df)`()` 

Delete all the data inside the block.

# class `bitprim-py::bitprim::Output` 

Represents one of the outputs of a [Transaction](#classbitprim-py_1_1bitprim_1_1Transaction).

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public def `[`is_valid`](#classbitprim-py_1_1bitprim_1_1Output_1ad00852dc52696e41210132d0b8640c62)`()` | Returns 0 if and only if output is not found.
`public def `[`serialized_size`](#classbitprim-py_1_1bitprim_1_1Output_1a7cb3c94232de8c027b592813f3f23e53)`(wire)` | [Block](#classbitprim-py_1_1bitprim_1_1Block) size in bytes.
`public def `[`value`](#classbitprim-py_1_1bitprim_1_1Output_1afe291758c2d3df8773a180b3314b6026)`()` | [Output](#classbitprim-py_1_1bitprim_1_1Output) value in Satoshis.
`public def `[`signature_operations`](#classbitprim-py_1_1bitprim_1_1Output_1ae15adadbf1f3d77a20d07520ab773414)`()` | Amount of signature operations in script.
`public def `[`script`](#classbitprim-py_1_1bitprim_1_1Output_1af932383bc4ff5906d53bb50ce19edd59)`()` | [Script](#classbitprim-py_1_1bitprim_1_1Script): returns the output script.

## Members

#### `public def `[`is_valid`](#classbitprim-py_1_1bitprim_1_1Output_1ad00852dc52696e41210132d0b8640c62)`()` 

Returns 0 if and only if output is not found.

#### Returns
(int)

#### `public def `[`serialized_size`](#classbitprim-py_1_1bitprim_1_1Output_1a7cb3c94232de8c027b592813f3f23e53)`(wire)` 

[Block](#classbitprim-py_1_1bitprim_1_1Block) size in bytes.

#### Parameters
* `wire` (bool): if true, size will include size of 'uint32' for storing spender height 

#### Returns
(unsigned int)

#### `public def `[`value`](#classbitprim-py_1_1bitprim_1_1Output_1afe291758c2d3df8773a180b3314b6026)`()` 

[Output](#classbitprim-py_1_1bitprim_1_1Output) value in Satoshis.

#### Returns
(unsigned int)

#### `public def `[`signature_operations`](#classbitprim-py_1_1bitprim_1_1Output_1ae15adadbf1f3d77a20d07520ab773414)`()` 

Amount of signature operations in script.

#### Returns
(unsigned int)

#### `public def `[`script`](#classbitprim-py_1_1bitprim_1_1Output_1af932383bc4ff5906d53bb50ce19edd59)`()` 

[Script](#classbitprim-py_1_1bitprim_1_1Script): returns the output script.

"""

# class `bitprim-py::bitprim::OutputPoint` 

[Transaction](#classbitprim-py_1_1bitprim_1_1Transaction) hash and index pair representing one of the transaction outputs.

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public def `[`hash`](#classbitprim-py_1_1bitprim_1_1OutputPoint_1a05dbf08bfe327b6921c973dc3d892cae)`()` | [Transaction](#classbitprim-py_1_1bitprim_1_1Transaction) hash in 32 byte array format.
`public def `[`index`](#classbitprim-py_1_1bitprim_1_1OutputPoint_1aa5b25737824a2e3cc4c740938a26860d)`()` | Position of the output in the transaction (starting at zero)
`public def `[`construct`](#classbitprim-py_1_1bitprim_1_1OutputPoint_1a4d0c7f4cc0ca831aee9ead6894b28d3f)`()` | Creates an empty output point.
`public def `[`construct_from_hash_index`](#classbitprim-py_1_1bitprim_1_1OutputPoint_1a00b134c01738b03ee4127e621f037414)`(hashn,`[`index`](#classbitprim-py_1_1bitprim_1_1OutputPoint_1aa5b25737824a2e3cc4c740938a26860d)`)` | Creates an [OutputPoint](#classbitprim-py_1_1bitprim_1_1OutputPoint) from a transaction hash and index pair.

## Members

#### `public def `[`hash`](#classbitprim-py_1_1bitprim_1_1OutputPoint_1a05dbf08bfe327b6921c973dc3d892cae)`()` 

[Transaction](#classbitprim-py_1_1bitprim_1_1Transaction) hash in 32 byte array format.

#### Returns
(bytearray)

#### `public def `[`index`](#classbitprim-py_1_1bitprim_1_1OutputPoint_1aa5b25737824a2e3cc4c740938a26860d)`()` 

Position of the output in the transaction (starting at zero)

#### Returns
(unsigned int)

#### `public def `[`construct`](#classbitprim-py_1_1bitprim_1_1OutputPoint_1a4d0c7f4cc0ca831aee9ead6894b28d3f)`()` 

Creates an empty output point.

#### Returns
([OutputPoint](#classbitprim-py_1_1bitprim_1_1OutputPoint))

#### `public def `[`construct_from_hash_index`](#classbitprim-py_1_1bitprim_1_1OutputPoint_1a00b134c01738b03ee4127e621f037414)`(hashn,`[`index`](#classbitprim-py_1_1bitprim_1_1OutputPoint_1aa5b25737824a2e3cc4c740938a26860d)`)` 

Creates an [OutputPoint](#classbitprim-py_1_1bitprim_1_1OutputPoint) from a transaction hash and index pair.

#### Parameters
* `hashn` (bytearray): [Transaction](#classbitprim-py_1_1bitprim_1_1Transaction) hash in 32 byte array format 

* `index` (unsigned int): position of the output in the transaction. 

#### Returns
(Outputpoint)

# class `bitprim-py::bitprim::P2p` 

Represents the Bitcoin `P2P` Networking API.

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public def `[`address_count`](#classbitprim-py_1_1bitprim_1_1P2p_1a7d87a3623ae7dc935cb664733da2e6cd)`()` | 
`public def `[`stop`](#classbitprim-py_1_1bitprim_1_1P2p_1a26d9a1501654d0ed1e5afeefda3de941)`()` | 
`public def `[`close`](#classbitprim-py_1_1bitprim_1_1P2p_1a57adb23c0c20f510f6eb4f3f09be2d39)`()` | 
`public def `[`stopped`](#classbitprim-py_1_1bitprim_1_1P2p_1afb2ce808ea6759718922020d46f043c8)`()` | 

## Members

#### `public def `[`address_count`](#classbitprim-py_1_1bitprim_1_1P2p_1a7d87a3623ae7dc935cb664733da2e6cd)`()` 

#### `public def `[`stop`](#classbitprim-py_1_1bitprim_1_1P2p_1a26d9a1501654d0ed1e5afeefda3de941)`()` 

#### `public def `[`close`](#classbitprim-py_1_1bitprim_1_1P2p_1a57adb23c0c20f510f6eb4f3f09be2d39)`()` 

#### `public def `[`stopped`](#classbitprim-py_1_1bitprim_1_1P2p_1afb2ce808ea6759718922020d46f043c8)`()` 

# class `bitprim-py::bitprim::PaymentAddress` 

Represents a Bitcoin wallet address.

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public def `[`encoded`](#classbitprim-py_1_1bitprim_1_1PaymentAddress_1af1cdc7005a7ef4d8675ed0d058cc8501)`()` | Address in readable format (hex string)
`public def `[`version`](#classbitprim-py_1_1bitprim_1_1PaymentAddress_1a3ab562255f10b971828f4469e93fed27)`()` | Address version.
`public def `[`construct_from_string`](#classbitprim-py_1_1bitprim_1_1PaymentAddress_1ad36c727ed2a22d9319cce02f90a6edf9)`(address)` | Creates the Payment Address based on the received string.

## Members

#### `public def `[`encoded`](#classbitprim-py_1_1bitprim_1_1PaymentAddress_1af1cdc7005a7ef4d8675ed0d058cc8501)`()` 

Address in readable format (hex string)

#### Returns
(str)

#### `public def `[`version`](#classbitprim-py_1_1bitprim_1_1PaymentAddress_1a3ab562255f10b971828f4469e93fed27)`()` 

Address version.

#### Returns
(unsigned int)

#### `public def `[`construct_from_string`](#classbitprim-py_1_1bitprim_1_1PaymentAddress_1ad36c727ed2a22d9319cce02f90a6edf9)`(address)` 

Creates the Payment Address based on the received string.

#### Parameters
* `address` (str) A base58 address. Example: '1MLVpZC2CTFHheox8SCEnAbW5NBdewRTdR'

# class `bitprim-py::bitprim::Point` 

Represents one of the tx inputs.

It's a transaction hash and index pair.

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public def `[`hash`](#classbitprim-py_1_1bitprim_1_1Point_1a769b69a1c88d48a005cf3ee5bc3fc0be)`()` | [Transaction](#classbitprim-py_1_1bitprim_1_1Transaction) hash in 32 byte array format.
`public def `[`is_valid`](#classbitprim-py_1_1bitprim_1_1Point_1ae9fe3003137cd984294baf00d326d860)`()` | returns true if its not null.
`public def `[`index`](#classbitprim-py_1_1bitprim_1_1Point_1a4ea1423a10b705f0da514602984d0cfc)`()` | [Input](#classbitprim-py_1_1bitprim_1_1Input) position in the transaction (starting at zero)
`public def `[`checksum`](#classbitprim-py_1_1bitprim_1_1Point_1aa7d8499e11091e3d6814d449f984d151)`()` | This is used with output_point identification within a set of history rows of the same address.

## Members

#### `public def `[`hash`](#classbitprim-py_1_1bitprim_1_1Point_1a769b69a1c88d48a005cf3ee5bc3fc0be)`()` 

[Transaction](#classbitprim-py_1_1bitprim_1_1Transaction) hash in 32 byte array format.

#### Returns
(byte array)

#### `public def `[`is_valid`](#classbitprim-py_1_1bitprim_1_1Point_1ae9fe3003137cd984294baf00d326d860)`()` 

returns true if its not null.

Returns: bool

#### `public def `[`index`](#classbitprim-py_1_1bitprim_1_1Point_1a4ea1423a10b705f0da514602984d0cfc)`()` 

[Input](#classbitprim-py_1_1bitprim_1_1Input) position in the transaction (starting at zero)

#### Returns
(unsigned int)

#### `public def `[`checksum`](#classbitprim-py_1_1bitprim_1_1Point_1aa7d8499e11091e3d6814d449f984d151)`()` 

This is used with output_point identification within a set of history rows of the same address.

Collision will result in miscorrelation of points by client callers. This is NOT a bitcoin checksum. 
#### Returns
(unsigned int)

# class `bitprim-py::bitprim::Script` 

Represents a transaction script.

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public def `[`is_valid`](#classbitprim-py_1_1bitprim_1_1Script_1a9b6ec4344c4c0e2f8449137924525ecd)`()` | All script bytes are valid under some circumstance (e.g.
`public def `[`is_valid_operations`](#classbitprim-py_1_1bitprim_1_1Script_1af761eba7a960265c8b93a2c3f1e17412)`()` | [Script](#classbitprim-py_1_1bitprim_1_1Script) validity is independent of individual operation validity.
`public def `[`satoshi_content_size`](#classbitprim-py_1_1bitprim_1_1Script_1aa7656ca492d8372873d61ab80176addd)`()` | Size in bytes.
`public def `[`serialized_size`](#classbitprim-py_1_1bitprim_1_1Script_1a6c72828fc7e8ab8fd2c73a9df3add14d)`(prefix)` | Size in bytes.
`public def `[`to_string`](#classbitprim-py_1_1bitprim_1_1Script_1ae83d84e607644b7703ce44eeacf6dd3a)`(active_forks)` | Translate operations in the script to string.
`public def `[`sigops`](#classbitprim-py_1_1bitprim_1_1Script_1a5879bfb8f103ce5c9276c98a1432b27d)`(embedded)` | Amount of signature operations in the script.
`public def `[`embedded_sigops`](#classbitprim-py_1_1bitprim_1_1Script_1a6da1a8dba7ce44d5a8261ef9c8474cb7)`(prevout_script)` | Count the sigops in the embedded script using BIP16 rules.

## Members

#### `public def `[`is_valid`](#classbitprim-py_1_1bitprim_1_1Script_1a9b6ec4344c4c0e2f8449137924525ecd)`()` 

All script bytes are valid under some circumstance (e.g.

coinbase). 
#### Returns
(int) 0 if and only if prefix and byte count do not match.

#### `public def `[`is_valid_operations`](#classbitprim-py_1_1bitprim_1_1Script_1af761eba7a960265c8b93a2c3f1e17412)`()` 

[Script](#classbitprim-py_1_1bitprim_1_1Script) validity is independent of individual operation validity.

Ops are considered invalid if there is a trailing invalid/default op or if a push op has a size mismatch 
#### Returns
(int)

#### `public def `[`satoshi_content_size`](#classbitprim-py_1_1bitprim_1_1Script_1aa7656ca492d8372873d61ab80176addd)`()` 

Size in bytes.

#### Returns
(unsigned int)

#### `public def `[`serialized_size`](#classbitprim-py_1_1bitprim_1_1Script_1a6c72828fc7e8ab8fd2c73a9df3add14d)`(prefix)` 

Size in bytes.

If prefix is 1 size, includes a var int size 
#### Parameters
* `prefix` (int): include prefix size in the final result 

#### Returns
(unsigned int)

#### `public def `[`to_string`](#classbitprim-py_1_1bitprim_1_1Script_1ae83d84e607644b7703ce44eeacf6dd3a)`(active_forks)` 

Translate operations in the script to string.

#### Parameters
* `active_forks` (unsigned int): Tells which rule is active 

#### Returns
(str)

#### `public def `[`sigops`](#classbitprim-py_1_1bitprim_1_1Script_1a5879bfb8f103ce5c9276c98a1432b27d)`(embedded)` 

Amount of signature operations in the script.

#### Parameters
* `embedded` (bool): Tells whether this is an embedded script 

#### Returns
(unsigned int)

#### `public def `[`embedded_sigops`](#classbitprim-py_1_1bitprim_1_1Script_1a6da1a8dba7ce44d5a8261ef9c8474cb7)`(prevout_script)` 

Count the sigops in the embedded script using BIP16 rules.

#### Returns
(unsigned int)

# class `bitprim-py::bitprim::Stealth` 

[Stealth](#classbitprim-py_1_1bitprim_1_1Stealth) payment related data.

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public def `[`ephemeral_public_key_hash`](#classbitprim-py_1_1bitprim_1_1Stealth_1a40bf96bf4766af27b611bbb7fb3ca532)`()` | 33 bytes.
`public def `[`transaction_hash`](#classbitprim-py_1_1bitprim_1_1Stealth_1a2a969744c067849b58f69f0369824eff)`()` | [Transaction](#classbitprim-py_1_1bitprim_1_1Transaction) hash in 32 bytes format.
`public def `[`public_key_hash`](#classbitprim-py_1_1bitprim_1_1Stealth_1ad85500f41aebba4296898f1d0ad0412c)`()` | Public key hash in 20 byte array format.

## Members

#### `public def `[`ephemeral_public_key_hash`](#classbitprim-py_1_1bitprim_1_1Stealth_1a40bf96bf4766af27b611bbb7fb3ca532)`()` 

33 bytes.

Includes the sign byte (0x02) 
#### Returns
(bytearray)

#### `public def `[`transaction_hash`](#classbitprim-py_1_1bitprim_1_1Stealth_1a2a969744c067849b58f69f0369824eff)`()` 

[Transaction](#classbitprim-py_1_1bitprim_1_1Transaction) hash in 32 bytes format.

#### Returns
(bytearray)

#### `public def `[`public_key_hash`](#classbitprim-py_1_1bitprim_1_1Stealth_1ad85500f41aebba4296898f1d0ad0412c)`()` 

Public key hash in 20 byte array format.

#### Returns
(bytearray)

# class `bitprim-py::bitprim::StealthCompact` 

Compressed representation of [Stealth](#classbitprim-py_1_1bitprim_1_1Stealth) payment related data.

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public def `[`ephemeral_public_key_hash`](#classbitprim-py_1_1bitprim_1_1StealthCompact_1a50276fa81cbdbdc6d9c5c61c08c3b466)`()` | Ephemeral public key hash in 32 byte array format.
`public def `[`transaction_hash`](#classbitprim-py_1_1bitprim_1_1StealthCompact_1a77d9f757e9e6c9d4fa1dbcc1c00cfede)`()` | [Transaction](#classbitprim-py_1_1bitprim_1_1Transaction) hash in 32 byte array format.
`public def `[`public_key_hash`](#classbitprim-py_1_1bitprim_1_1StealthCompact_1a91abc6e2a28913ee1e61ce76f21787e6)`()` | Public key hash in 20 byte array format.

## Members

#### `public def `[`ephemeral_public_key_hash`](#classbitprim-py_1_1bitprim_1_1StealthCompact_1a50276fa81cbdbdc6d9c5c61c08c3b466)`()` 

Ephemeral public key hash in 32 byte array format.

Does not include the sign byte (0x02) 
#### Returns
(byte array)

#### `public def `[`transaction_hash`](#classbitprim-py_1_1bitprim_1_1StealthCompact_1a77d9f757e9e6c9d4fa1dbcc1c00cfede)`()` 

[Transaction](#classbitprim-py_1_1bitprim_1_1Transaction) hash in 32 byte array format.

#### Returns
(byte array)

#### `public def `[`public_key_hash`](#classbitprim-py_1_1bitprim_1_1StealthCompact_1a91abc6e2a28913ee1e61ce76f21787e6)`()` 

Public key hash in 20 byte array format.

#### Returns
(byte array)

# class `bitprim-py::bitprim::Transaction` 

Represents a Bitcoin [Transaction](#classbitprim-py_1_1bitprim_1_1Transaction).

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public def `[`version`](#classbitprim-py_1_1bitprim_1_1Transaction_1aa0645d1ed364603e366414e4e70e19e2)`()` | [Transaction](#classbitprim-py_1_1bitprim_1_1Transaction) protocol version.
`public def `[`set_version`](#classbitprim-py_1_1bitprim_1_1Transaction_1aa4877d45df18da894d8975b666570c03)`(`[`version`](#classbitprim-py_1_1bitprim_1_1Transaction_1aa0645d1ed364603e366414e4e70e19e2)`)` | Set new transaction version value.
`public def `[`hash`](#classbitprim-py_1_1bitprim_1_1Transaction_1a4bc40f5d9a176b9e58b88026b0715638)`()` | bytearray: 32 bytes transaction hash.
`public def `[`hash_sighash_type`](#classbitprim-py_1_1bitprim_1_1Transaction_1ad34d97d680ec9d6ba824325f07388bd8)`(sighash_type)` | 32 bytes transaction hash + 4 bytes signature hash type
`public def `[`locktime`](#classbitprim-py_1_1bitprim_1_1Transaction_1a0bb1fb350c14fef36a221d1d8d8c6b67)`()` | [Transaction](#classbitprim-py_1_1bitprim_1_1Transaction) locktime.
`public def `[`serialized_size`](#classbitprim-py_1_1bitprim_1_1Transaction_1a1f861e77dbc67de37c6667cc69a5893f)`(wire)` | [Transaction](#classbitprim-py_1_1bitprim_1_1Transaction) size in bytes.
`public def `[`fees`](#classbitprim-py_1_1bitprim_1_1Transaction_1a39560a3fe997f308d6d8e5993f2fe804)`()` | Fees to pay to the winning miner.
`public def `[`signature_operations`](#classbitprim-py_1_1bitprim_1_1Transaction_1afdc08c10aa1f6d5fa0e97900435229d2)`()` | Amount of signature operations in the transaction.
`public def `[`signature_operations_bip16_active`](#classbitprim-py_1_1bitprim_1_1Transaction_1afb639b53fa7f54c76685b09e0e301d72)`(bip16_active)` | Amount of signature operations in the transaction.
`public def `[`total_input_value`](#classbitprim-py_1_1bitprim_1_1Transaction_1a6ace5d080d3fdacf2ae464e9a6132728)`()` | Sum of every input value in the transaction.
`public def `[`total_output_value`](#classbitprim-py_1_1bitprim_1_1Transaction_1afb97ebed6e1f5e54f1f998ee7ca03da5)`()` | Sum of every output value in the transaction.
`public def `[`is_coinbase`](#classbitprim-py_1_1bitprim_1_1Transaction_1ad4789711bb2628a48d99d5e0942b85ff)`()` | Return 1 if and only if transaction is coinbase, 0 otherwise.
`public def `[`is_null_non_coinbase`](#classbitprim-py_1_1bitprim_1_1Transaction_1a212bcb41f5af02e5a321507238b7c67e)`()` | Return 1 if and only if the transaction is not coinbase and has a null previous output, 0 otherwise.
`public def `[`is_oversized_coinbase`](#classbitprim-py_1_1bitprim_1_1Transaction_1ab0e7d9c00716cedf8d0c7a36fd57710a)`()` | Returns 1 if the transaction is coinbase and has an invalid script size on its first input.
`public def `[`is_mature`](#classbitprim-py_1_1bitprim_1_1Transaction_1a252aeca7f71d8132b537d6aa50e03af6)`(target_height)` | Returns 1 if and only if at least one of the inputs is not mature, 0 otherwise.
`public def `[`is_overspent`](#classbitprim-py_1_1bitprim_1_1Transaction_1ac5572cc62c77734450b73e14b9ff0a1e)`()` | Returns 1 if transaction is not a coinbase, and the sum of its outputs is higher than the sum of its inputs, 0 otherwise.
`public def `[`is_double_spend`](#classbitprim-py_1_1bitprim_1_1Transaction_1a477e1e68292a50ade80ab598ec645e59)`(include_unconfirmed)` | Returns 1 if at least one of the previous outputs was already spent, 0 otherwise.
`public def `[`is_missing_previous_outputs`](#classbitprim-py_1_1bitprim_1_1Transaction_1ad3cc78bfe0ba993fe1eafab6905b5f70)`()` | Returns 1 if and only if at least one of the previous outputs is invalid, 0 otherwise.
`public def `[`is_final`](#classbitprim-py_1_1bitprim_1_1Transaction_1a8d846e71bd65b0bae933037709321e59)`(block_height,block_time)` | Returns 1 if and only if the transaction is final, 0 otherwise.
`public def `[`is_locktime_conflict`](#classbitprim-py_1_1bitprim_1_1Transaction_1a4b6c074b3d02e78eb4c21260b8bc23cf)`()` | Returns 1 if and only if the transaction is locked and every input is final, 0 otherwise.
`public def `[`outputs`](#classbitprim-py_1_1bitprim_1_1Transaction_1af95578f147dee2cfc6b31b17422ba45f)`()` | Returns a list with all of this transaction's outputs.
`public def `[`inputs`](#classbitprim-py_1_1bitprim_1_1Transaction_1a853bc44a3722b45b4c289e3e49335267)`()` | Returns a list with all of this transaction's inputs.
`public def `[`to_data`](#classbitprim-py_1_1bitprim_1_1Transaction_1adce773eb03ed3dc5439bf47cf64a9b92)`(wired)` | 

## Members

#### `public def `[`version`](#classbitprim-py_1_1bitprim_1_1Transaction_1aa0645d1ed364603e366414e4e70e19e2)`()` 

[Transaction](#classbitprim-py_1_1bitprim_1_1Transaction) protocol version.

#### Returns
(unsigned int)

#### `public def `[`set_version`](#classbitprim-py_1_1bitprim_1_1Transaction_1aa4877d45df18da894d8975b666570c03)`(`[`version`](#classbitprim-py_1_1bitprim_1_1Transaction_1aa0645d1ed364603e366414e4e70e19e2)`)` 

Set new transaction version value.

#### Parameters
* `version` New transaction version value

#### `public def `[`hash`](#classbitprim-py_1_1bitprim_1_1Transaction_1a4bc40f5d9a176b9e58b88026b0715638)`()` 

bytearray: 32 bytes transaction hash.

#### `public def `[`hash_sighash_type`](#classbitprim-py_1_1bitprim_1_1Transaction_1ad34d97d680ec9d6ba824325f07388bd8)`(sighash_type)` 

32 bytes transaction hash + 4 bytes signature hash type

#### Parameters
* `sighash_type` (unsigned int): signature hash type 

#### Returns
(byte array)

#### `public def `[`locktime`](#classbitprim-py_1_1bitprim_1_1Transaction_1a0bb1fb350c14fef36a221d1d8d8c6b67)`()` 

[Transaction](#classbitprim-py_1_1bitprim_1_1Transaction) locktime.

#### Returns
(unsigned int)

#### `public def `[`serialized_size`](#classbitprim-py_1_1bitprim_1_1Transaction_1a1f861e77dbc67de37c6667cc69a5893f)`(wire)` 

[Transaction](#classbitprim-py_1_1bitprim_1_1Transaction) size in bytes.

#### Parameters
* `wire` (bool): if true, size will include size of 'uint32' for storing spender output height 

#### Returns
(unsigned int)

#### `public def `[`fees`](#classbitprim-py_1_1bitprim_1_1Transaction_1a39560a3fe997f308d6d8e5993f2fe804)`()` 

Fees to pay to the winning miner.

Difference between sum of inputs and outputs 
#### Returns
(unsigned int)

#### `public def `[`signature_operations`](#classbitprim-py_1_1bitprim_1_1Transaction_1afdc08c10aa1f6d5fa0e97900435229d2)`()` 

Amount of signature operations in the transaction.

#### Returns
(unsigned int) max_int in case of overflow

#### `public def `[`signature_operations_bip16_active`](#classbitprim-py_1_1bitprim_1_1Transaction_1afb639b53fa7f54c76685b09e0e301d72)`(bip16_active)` 

Amount of signature operations in the transaction.

#### Parameters
* `bip16_active` (int): 1 if and only if bip 16 is active, 0 otherwise 

#### Returns
(unsigned int) max_int in case of overflow.

#### `public def `[`total_input_value`](#classbitprim-py_1_1bitprim_1_1Transaction_1a6ace5d080d3fdacf2ae464e9a6132728)`()` 

Sum of every input value in the transaction.

#### Returns
(unsigned int) max_int in case of overflow

#### `public def `[`total_output_value`](#classbitprim-py_1_1bitprim_1_1Transaction_1afb97ebed6e1f5e54f1f998ee7ca03da5)`()` 

Sum of every output value in the transaction.

#### Returns
(unsigned int) max_int in case of overflow

#### `public def `[`is_coinbase`](#classbitprim-py_1_1bitprim_1_1Transaction_1ad4789711bb2628a48d99d5e0942b85ff)`()` 

Return 1 if and only if transaction is coinbase, 0 otherwise.

#### Returns
(int)

#### `public def `[`is_null_non_coinbase`](#classbitprim-py_1_1bitprim_1_1Transaction_1a212bcb41f5af02e5a321507238b7c67e)`()` 

Return 1 if and only if the transaction is not coinbase and has a null previous output, 0 otherwise.

#### Returns
(int)

#### `public def `[`is_oversized_coinbase`](#classbitprim-py_1_1bitprim_1_1Transaction_1ab0e7d9c00716cedf8d0c7a36fd57710a)`()` 

Returns 1 if the transaction is coinbase and has an invalid script size on its first input.

#### Returns
(int)

#### `public def `[`is_mature`](#classbitprim-py_1_1bitprim_1_1Transaction_1a252aeca7f71d8132b537d6aa50e03af6)`(target_height)` 

Returns 1 if and only if at least one of the inputs is not mature, 0 otherwise.

#### Returns
(int)

#### `public def `[`is_overspent`](#classbitprim-py_1_1bitprim_1_1Transaction_1ac5572cc62c77734450b73e14b9ff0a1e)`()` 

Returns 1 if transaction is not a coinbase, and the sum of its outputs is higher than the sum of its inputs, 0 otherwise.

#### Returns
(int)

#### `public def `[`is_double_spend`](#classbitprim-py_1_1bitprim_1_1Transaction_1a477e1e68292a50ade80ab598ec645e59)`(include_unconfirmed)` 

Returns 1 if at least one of the previous outputs was already spent, 0 otherwise.

#### Returns
(int)

#### `public def `[`is_missing_previous_outputs`](#classbitprim-py_1_1bitprim_1_1Transaction_1ad3cc78bfe0ba993fe1eafab6905b5f70)`()` 

Returns 1 if and only if at least one of the previous outputs is invalid, 0 otherwise.

#### Returns
(int)

#### `public def `[`is_final`](#classbitprim-py_1_1bitprim_1_1Transaction_1a8d846e71bd65b0bae933037709321e59)`(block_height,block_time)` 

Returns 1 if and only if the transaction is final, 0 otherwise.

#### Returns
(int)

#### `public def `[`is_locktime_conflict`](#classbitprim-py_1_1bitprim_1_1Transaction_1a4b6c074b3d02e78eb4c21260b8bc23cf)`()` 

Returns 1 if and only if the transaction is locked and every input is final, 0 otherwise.

#### Returns
(int)

#### `public def `[`outputs`](#classbitprim-py_1_1bitprim_1_1Transaction_1af95578f147dee2cfc6b31b17422ba45f)`()` 

Returns a list with all of this transaction's outputs.

#### Returns
(OutputList)

#### `public def `[`inputs`](#classbitprim-py_1_1bitprim_1_1Transaction_1a853bc44a3722b45b4c289e3e49335267)`()` 

Returns a list with all of this transaction's inputs.

#### Returns
(InputList)

#### `public def `[`to_data`](#classbitprim-py_1_1bitprim_1_1Transaction_1adce773eb03ed3dc5439bf47cf64a9b92)`(wired)` 

# class `bitprim-py::bitprim::Wallet` 

[Wallet](#classbitprim-py_1_1bitprim_1_1Wallet) handling utilities.

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public def `[`mnemonics_to_seed`](#classbitprim-py_1_1bitprim_1_1Wallet_1ac66aadd0dc07bc22a938152b2aeacf58)`(cls,mnemonics)` | Convert mnemonics to a seed.

## Members

#### `public def `[`mnemonics_to_seed`](#classbitprim-py_1_1bitprim_1_1Wallet_1ac66aadd0dc07bc22a938152b2aeacf58)`(cls,mnemonics)` 

Convert mnemonics to a seed.

#### Parameters
* `mnemonics` A list of strings representing the mnemonics 

#### Returns
A new seed

Generated by [Moxygen](https://sourcey.com/moxygen)