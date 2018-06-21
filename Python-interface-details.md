# Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`namespace `[`bitprim`](#namespacebitprim) | 

# namespace `bitprim` 

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public def `[`encode_hash`](#bitprim_8py_1a0592acb88150dfcb800e7fa1975cf8ce)`(hash)`            | str: Converts a bytearray into a readable format.
`public def `[`decode_hash`](#bitprim_8py_1ae9d85d5c0bd672672fc12eb12144c092)`(hash_str)`            | bytearray: Converts a string into a workable format. 
`class `[`bitprim::Binary`](#classbitprim_1_1Binary) | Represents a binary filter.
`class `[`bitprim::Block`](#classbitprim_1_1Block) | Represent a full Bitcoin block.
`class `[`bitprim::BlockList`](#classbitprim_1_1BlockList) | 
`class `[`bitprim::Chain`](#classbitprim_1_1Chain) | Represents the Bitcoin blockchain.
`class `[`bitprim::Executor`](#classbitprim_1_1Executor) | Controls the execution of the Bitprim bitcoin node.
`class `[`bitprim::Header`](#classbitprim_1_1Header) | Represent the Header of a Bitcoin Block.
`class `[`bitprim::History`](#classbitprim_1_1History) | Output points, values, and spends for a payment address
`class `[`bitprim::HistoryList`](#classbitprim_1_1HistoryList) | 
`class `[`bitprim::Input`](#classbitprim_1_1Input) | Represents one of the inputs of a Transaction.
`class `[`bitprim::InputList`](#classbitprim_1_1InputList) | 
`class `[`bitprim::MerkleBlock`](#classbitprim_1_1MerkleBlock) | 
`class `[`bitprim::Output`](#classbitprim_1_1Output) | Represents one of the outputs of a Transaction.
`class `[`bitprim::OutputList`](#classbitprim_1_1OutputList) | 
`class `[`bitprim::OutputPoint`](#classbitprim_1_1OutputPoint) | Transaction hash and index representing one of the transaction outputs.
`class `[`bitprim::PaymentAddress`](#classbitprim_1_1PaymentAddress) | Represents a Bitcoin wallet address.
`class `[`bitprim::Point`](#classbitprim_1_1Point) | Represents one of the txs input.
`class `[`bitprim::Script`](#classbitprim_1_1Script) | Represents transaction scripts.
`class `[`bitprim::Stealth`](#classbitprim_1_1Stealth) | 
`class `[`bitprim::StealthCompact`](#classbitprim_1_1StealthCompact) | 
`class `[`bitprim::StealthCompactList`](#classbitprim_1_1StealthCompactList) | 
`class `[`bitprim::StealthList`](#classbitprim_1_1StealthList) | 
`class `[`bitprim::Transaction`](#classbitprim_1_1Transaction) | Represents a Bitcoin Transaction.
`class `[`bitprim::TransactionList`](#classbitprim_1_1TransactionList) | 
`class `[`bitprim::Wallet`](#classbitprim_1_1Wallet) | 

## Members

#### `public def `[`encode_hash`](#bitprim_8py_1a0592acb88150dfcb800e7fa1975cf8ce)`(hash)` 

str: Converts a bytearray into a readable format.
example return: "000000000019d6689c085ae165831e934ff763ae46a2a6c172b3f1b60a8ce26f"

Args:
    hash (bytearray): bytes of the hash.

#### `public def `[`decode_hash`](#bitprim_8py_1ae9d85d5c0bd672672fc12eb12144c092)`(hash_str)` 

bytearray: Converts a string into a workable format. 

Args:
    hash_str (str): string with hash. example "000000000019d6689c085ae165831e934ff763ae46a2a6c172b3f1b60a8ce26f"

# class `bitprim::Binary` 

Represents a binary filter.

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public def `[`__init__`](#classbitprim_1_1Binary_1a1daf6fc8346857c44134d1b162888e00)`(self,ptr)` | 
`public def `[`construct`](#classbitprim_1_1Binary_1a248318057ecc3f432d2f3d4514ee7018)`(self)` | Binary: create an empty binary object.
`public def `[`construct_string`](#classbitprim_1_1Binary_1af6393c61459c6e883bd103ffa30ce765)`(self,string_filter)` | Binary: construct a binary filter form string.
`public def `[`construct_blocks`](#classbitprim_1_1Binary_1a74fbcd4afc9837b23ef1a91ea2a7589c)`(self,size,`[`blocks`](#classbitprim_1_1Binary_1a59e18ba201b98aeb46acff7cdeddadb8)`)` | Binary: construct binary filter from an array of int.
`public def `[`blocks`](#classbitprim_1_1Binary_1a59e18ba201b98aeb46acff7cdeddadb8)`(self)` | Array [unsigned int]: returns the filter as an array of uint.
`public def `[`encoded`](#classbitprim_1_1Binary_1a357615d3078c30ad799f6a4f057a8d0d)`(self)` | str: returns the filter in a binary string.

## Members

#### `public def `[`__init__`](#classbitprim_1_1Binary_1a1daf6fc8346857c44134d1b162888e00)`(self,ptr)` 

#### `public def `[`construct`](#classbitprim_1_1Binary_1a248318057ecc3f432d2f3d4514ee7018)`(self)` 

Binary: create an empty binary object.

#### `public def `[`construct_string`](#classbitprim_1_1Binary_1af6393c61459c6e883bd103ffa30ce765)`(self,string_filter)` 

Binary: construct a binary filter form string.

Args:
    string_filter (str): binary string. Example: '10111010101011011111000000001101'

#### `public def `[`construct_blocks`](#classbitprim_1_1Binary_1a74fbcd4afc9837b23ef1a91ea2a7589c)`(self,size,`[`blocks`](#classbitprim_1_1Binary_1a59e18ba201b98aeb46acff7cdeddadb8)`)` 

Binary: construct binary filter from an array of int.

Args:
    size (unsigned int): lenght of the filter.
    blocks (array[unsigned int]): Every int represents a byte of the filter. Example: '[186,173,240,13]'

#### `public def `[`blocks`](#classbitprim_1_1Binary_1a59e18ba201b98aeb46acff7cdeddadb8)`(self)` 

Array [unsigned int]: returns the filter as an array of uint.

#### `public def `[`encoded`](#classbitprim_1_1Binary_1a357615d3078c30ad799f6a4f057a8d0d)`(self)` 

str: returns the filter in a binary string.

# class `bitprim::Block` 

Represent a full Bitcoin block.

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public def `[`__init__`](#classbitprim_1_1Block_1a44545a7845b4018443876653dfec399b)`(self,pointer,`[`height`](#classbitprim_1_1Block_1a7d8e2c22055d9d5247969f709d2b574b)`)` | 
`public def `[`__del__`](#classbitprim_1_1Block_1abe0b5010b709246f4c6782994e9425c8)`(self)` | 
`public def `[`height`](#classbitprim_1_1Block_1a7d8e2c22055d9d5247969f709d2b574b)`(self)` | unsigned int: Height of the block in the chain.
`public def `[`header`](#classbitprim_1_1Block_1afcfdf6c352e1e7050d28c3feab1e1ac2)`(self)` | Header: block header object.
`public def `[`transaction_count`](#classbitprim_1_1Block_1af3d919e7ed870a65fd5478c2a9429e01)`(self)` | unsigned int: amount of transaction in the block.
`public def `[`hash`](#classbitprim_1_1Block_1abb559d43d05b2c1348cb1ead5c9cda41)`(self)` | bytearray: 32 bytes of the block hash.
`public def `[`serialized_size`](#classbitprim_1_1Block_1ab3436c618568d6e09084fa4e9523671f)`(self)` | unsigned int: size of the block in bytes.
`public def `[`fees`](#classbitprim_1_1Block_1a1ef7f0aa734ec9e299e24f7fffc0808e)`(self)` | unsigned int: amount of fees included in coinbase.
`public def `[`claim`](#classbitprim_1_1Block_1a907b7a24b60a5c02de03a24f4b3044b3)`(self)` | unsigned int: value of the outputs in the coinbase.
`public def `[`reward`](#classbitprim_1_1Block_1a1d018419f3b6159090f411edac2a509f)`(self,`[`height`](#classbitprim_1_1Block_1a7d8e2c22055d9d5247969f709d2b574b)`)` | unsigned int: value of the fees plus the reward for a block at the given height.
`public def `[`generate_merkle_root`](#classbitprim_1_1Block_1ac0f6c0124f4783ffc9e35c4a845551a4)`(self)` | bytearray: 32 bytes of the merkle root, for the generated merkle tree.
`public def `[`is_valid`](#classbitprim_1_1Block_1ab89a94a544e21b2ba10090bcd134d0f4)`(self)` | int: block has transactions and a valid Header. 1 if its valid.
`public def `[`transaction_nth`](#classbitprim_1_1Block_1a5667be645fb35e99672f6edd4eb79f71)`(self,n)` | Transaction: given a position in the block, returns the corresponding transaction.
`public def `[`signature_operations`](#classbitprim_1_1Block_1ab7e7eb80570a7e1592260ace29b8172f)`(self)` | unsigned int: amount of signature operations in the block.
`public def `[`signature_operations_bip16_active`](#classbitprim_1_1Block_1a529bf227db8e885caedfb01ba96b30f4)`(self,bip16_active)` | unsigned int: amount of signature operations in the block.
`public def `[`total_inputs`](#classbitprim_1_1Block_1aecf9d6861b5804bf4e8a531da92e5469)`(self,with_coinbase)` | unsigned int: amount of inputs in every transaction in the block.
`public def `[`is_extra_coinbases`](#classbitprim_1_1Block_1a9ae78d94a280b7d2f6d4e61378e148b9)`(self)` | int: returns '1' if there is another coinbase other than the first transaction.
`public def `[`is_final`](#classbitprim_1_1Block_1acbeaad19916285fcb598284e0560bc99)`(self,`[`height`](#classbitprim_1_1Block_1a7d8e2c22055d9d5247969f709d2b574b)`)` | int: returns '1' if every transaction in the block is final.
`public def `[`is_distinct_transaction_set`](#classbitprim_1_1Block_1a2f858494ee1ddb0f455efc2289422f22)`(self)` | int: returns '1' if there are not two transactions with the same hash.
`public def `[`is_valid_coinbase_claim`](#classbitprim_1_1Block_1a5e844d3b70bc66bcac3cf4108d9a4c14)`(self,`[`height`](#classbitprim_1_1Block_1a7d8e2c22055d9d5247969f709d2b574b)`)` | int: returns '1' if coinbase claim is not higher than the deserved reward.
`public def `[`is_valid_coinbase_script`](#classbitprim_1_1Block_1a0b1d70c44c0f94090f5f3dc2b2730fc2)`(self,`[`height`](#classbitprim_1_1Block_1a7d8e2c22055d9d5247969f709d2b574b)`)` | int: returns '1' if coinbase script is valid.
`public def `[`is_valid_merkle_root`](#classbitprim_1_1Block_1a53e999a14dc396d90606155c384a9848)`(self)` | int: returns '1' if the generated merkle root is equal to the Header merkle root.

## Members

#### `public def `[`__init__`](#classbitprim_1_1Block_1a44545a7845b4018443876653dfec399b)`(self,pointer,`[`height`](#classbitprim_1_1Block_1a7d8e2c22055d9d5247969f709d2b574b)`)` 

#### `public def `[`__del__`](#classbitprim_1_1Block_1abe0b5010b709246f4c6782994e9425c8)`(self)` 

#### `public def `[`height`](#classbitprim_1_1Block_1a7d8e2c22055d9d5247969f709d2b574b)`(self)` 

unsigned int: Height of the block in the chain.

#### `public def `[`header`](#classbitprim_1_1Block_1afcfdf6c352e1e7050d28c3feab1e1ac2)`(self)` 

Header: block header object.

#### `public def `[`transaction_count`](#classbitprim_1_1Block_1af3d919e7ed870a65fd5478c2a9429e01)`(self)` 

unsigned int: amount of transaction in the block.

#### `public def `[`hash`](#classbitprim_1_1Block_1abb559d43d05b2c1348cb1ead5c9cda41)`(self)` 

bytearray: 32 bytes of the block hash.

#### `public def `[`serialized_size`](#classbitprim_1_1Block_1ab3436c618568d6e09084fa4e9523671f)`(self)` 

unsigned int: size of the block in bytes.

#### `public def `[`fees`](#classbitprim_1_1Block_1a1ef7f0aa734ec9e299e24f7fffc0808e)`(self)` 

unsigned int: amount of fees included in coinbase.

#### `public def `[`claim`](#classbitprim_1_1Block_1a907b7a24b60a5c02de03a24f4b3044b3)`(self)` 

unsigned int: value of the outputs in the coinbase.

#### `public def `[`reward`](#classbitprim_1_1Block_1a1d018419f3b6159090f411edac2a509f)`(self,`[`height`](#classbitprim_1_1Block_1a7d8e2c22055d9d5247969f709d2b574b)`)` 

unsigned int: value of the fees plus the reward for a block at the given height.

Args:
    height (unsigned int): height of the block in the chain.

#### `public def `[`generate_merkle_root`](#classbitprim_1_1Block_1ac0f6c0124f4783ffc9e35c4a845551a4)`(self)` 

bytearray: 32 bytes of the merkle root, for the generated merkle tree.

#### `public def `[`is_valid`](#classbitprim_1_1Block_1ab89a94a544e21b2ba10090bcd134d0f4)`(self)` 

int: block has transactions and a valid Header. 1 if its valid.

#### `public def `[`transaction_nth`](#classbitprim_1_1Block_1a5667be645fb35e99672f6edd4eb79f71)`(self,n)` 

Transaction: given a position in the block, returns the corresponding transaction.

Args: 
    n (unsigned int): index of the transaction in the block.

#### `public def `[`signature_operations`](#classbitprim_1_1Block_1ab7e7eb80570a7e1592260ace29b8172f)`(self)` 

unsigned int: amount of signature operations in the block.
Returns max_int in case of overflow.

#### `public def `[`signature_operations_bip16_active`](#classbitprim_1_1Block_1a529bf227db8e885caedfb01ba96b30f4)`(self,bip16_active)` 

unsigned int: amount of signature operations in the block.
Returns max_int in case of overflow.

Args:
    bip16_active(int): if bip16 is activated at this point. Should be '1' if its active.

#### `public def `[`total_inputs`](#classbitprim_1_1Block_1aecf9d6861b5804bf4e8a531da92e5469)`(self,with_coinbase)` 

unsigned int: amount of inputs in every transaction in the block.

Args:
    with_coinbase (int): should be '1' if block contains a coinbase transaction. '0' otherwise.

#### `public def `[`is_extra_coinbases`](#classbitprim_1_1Block_1a9ae78d94a280b7d2f6d4e61378e148b9)`(self)` 

int: returns '1' if there is another coinbase other than the first transaction.

#### `public def `[`is_final`](#classbitprim_1_1Block_1acbeaad19916285fcb598284e0560bc99)`(self,`[`height`](#classbitprim_1_1Block_1a7d8e2c22055d9d5247969f709d2b574b)`)` 

int: returns '1' if every transaction in the block is final.

Args:
    height (unsigned int): height of the block in the chain.

#### `public def `[`is_distinct_transaction_set`](#classbitprim_1_1Block_1a2f858494ee1ddb0f455efc2289422f22)`(self)` 

int: returns '1' if there are not two transactions with the same hash.

#### `public def `[`is_valid_coinbase_claim`](#classbitprim_1_1Block_1a5e844d3b70bc66bcac3cf4108d9a4c14)`(self,`[`height`](#classbitprim_1_1Block_1a7d8e2c22055d9d5247969f709d2b574b)`)` 

int: returns '1' if coinbase claim is not higher than the deserved reward.

Args:
    height (unsigned int): height of the block in the chain.

#### `public def `[`is_valid_coinbase_script`](#classbitprim_1_1Block_1a0b1d70c44c0f94090f5f3dc2b2730fc2)`(self,`[`height`](#classbitprim_1_1Block_1a7d8e2c22055d9d5247969f709d2b574b)`)` 

int: returns '1' if coinbase script is valid.

#### `public def `[`is_valid_merkle_root`](#classbitprim_1_1Block_1a53e999a14dc396d90606155c384a9848)`(self)` 

int: returns '1' if the generated merkle root is equal to the Header merkle root.

# class `bitprim::BlockList` 

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public def `[`__init__`](#classbitprim_1_1BlockList_1af0275513907dd01841efb2707040f947)`(self,ptr)` | 
`public def `[`__del__`](#classbitprim_1_1BlockList_1a2b0db7ee43138ad3ac6dede1e576d379)`(self)` | 
`public def `[`construct_default`](#classbitprim_1_1BlockList_1a294964864e12b86ea650841c384e80c4)`(self)` | 
`public def `[`push_back`](#classbitprim_1_1BlockList_1a0da9e5cf1747039d4538fcc9876d75a8)`(self,block)` | 
`public def `[`list_count`](#classbitprim_1_1BlockList_1a3696b14ba1271ae45e3be336266f89c3)`(self)` | 
`public def `[`__getitem__`](#classbitprim_1_1BlockList_1ad4d132428d9d3f6156fc4848720f640a)`(self,key)` | 

## Members

#### `public def `[`__init__`](#classbitprim_1_1BlockList_1af0275513907dd01841efb2707040f947)`(self,ptr)` 

#### `public def `[`__del__`](#classbitprim_1_1BlockList_1a2b0db7ee43138ad3ac6dede1e576d379)`(self)` 

#### `public def `[`construct_default`](#classbitprim_1_1BlockList_1a294964864e12b86ea650841c384e80c4)`(self)` 

#### `public def `[`push_back`](#classbitprim_1_1BlockList_1a0da9e5cf1747039d4538fcc9876d75a8)`(self,block)` 

#### `public def `[`list_count`](#classbitprim_1_1BlockList_1a3696b14ba1271ae45e3be336266f89c3)`(self)` 

#### `public def `[`__getitem__`](#classbitprim_1_1BlockList_1ad4d132428d9d3f6156fc4848720f640a)`(self,key)` 

# class `bitprim::Chain` 

Represents the Bitcoin blockchain.

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public  `[`history_fetch_handler_`](#classbitprim_1_1Chain_1aa966de86303a5df511cdbd20fba36027) | 
`public  `[`fetch_block_header_handler_`](#classbitprim_1_1Chain_1ae2925200c9e3213b288672c130ca5d7c) | 
`public def `[`__init__`](#classbitprim_1_1Chain_1a91d2e01fb06a95e28761bc33580be399)`(self,chain)` | 
`public def `[`fetch_last_height`](#classbitprim_1_1Chain_1a3b2aaba82203b00addff05747f630443)`(self,handler)` | Gets the height of the highest block in the chain. 
`public def `[`fetch_history`](#classbitprim_1_1Chain_1a8654c1cd107ce5455a3bf202a65ee6ac)`(self,address,limit,from_height,handler)` | Get list of output points, values, and spends for a payment address.
`public def `[`fetch_stealth`](#classbitprim_1_1Chain_1a1b87b8c0f9320c2c2e344297dee65b0f)`(self,binary_filter_str,from_height,handler)` | Get metadata on potential payment transactions by stealth filter. 
`public def `[`fetch_block_height`](#classbitprim_1_1Chain_1a99c62752f73e9b7ef8402863a04ad4a9)`(self,hash,handler)` | Given a block hash, it cues the chain for the block height. 
`public def `[`fetch_block_header_by_height`](#classbitprim_1_1Chain_1a094aa543335f147e7b6e48ad010ca070)`(self,height,handler)` | Get the block header from the specified height in the chain.
`public def `[`fetch_block_header_by_hash`](#classbitprim_1_1Chain_1aad170dbb1d2c7978414221a609856720)`(self,hash,handler)` | Get the block header from the specified block hash.
`public def `[`fetch_block_by_height`](#classbitprim_1_1Chain_1a284806f124ea0f94efdac5fa679993ad)`(self,height,handler)` | Gets a block from the specified height in the chain.
`public def `[`fetch_block_by_hash`](#classbitprim_1_1Chain_1a6d223f504ce3452988ffc2f84b27b2a4)`(self,hash,handler)` | Gets a block from the specified hash.
`public def `[`fetch_merkle_block_by_height`](#classbitprim_1_1Chain_1ae445ca8c6d5baaa009d08c98634246aa)`(self,height,handler)` | Given a block height in the chain, it retrieves a merkle block. 
`public def `[`fetch_merkle_block_by_hash`](#classbitprim_1_1Chain_1a7e4efae5160fe3615e608ec41e71f758)`(self,hash,handler)` | Given a block hash, it retrieves a merkle block. 
`public def `[`fetch_transaction`](#classbitprim_1_1Chain_1a1d85163b2ba7b815f0bfa997c3dbd442)`(self,hashn,require_confirmed,handler)` | Get a transaction by its hash. 
`public def `[`fetch_output`](#classbitprim_1_1Chain_1a72218a16849f5a0c8054be336658caf1)`(self,hashn,index,require_confirmed,handler)` | Get a transaction output by its transaction hash and index inside the transaction. 
`public def `[`fetch_transaction_position`](#classbitprim_1_1Chain_1a5024c70760381fc3eada646bba4a5c8e)`(self,hashn,require_confirmed,handler)` | Given a transaction hash it fetches the height and position inside the block.
`public def `[`validate_tx`](#classbitprim_1_1Chain_1a376f1a70435c94ee95d27dad2c66c6aa)`(self,transaction,handler)` | Determine if a transaction is valid for submission to the blockchain.
`public def `[`fetch_spend`](#classbitprim_1_1Chain_1ae1bd60745bb42815e14901925e6e6558)`(self,output_point,handler)` | Fetch the transaction input which spends the indicated output. The `fetch_spend_handler` will be executed after cueing the chain. 

## Members

#### `public  `[`history_fetch_handler_`](#classbitprim_1_1Chain_1aa966de86303a5df511cdbd20fba36027) 

#### `public  `[`fetch_block_header_handler_`](#classbitprim_1_1Chain_1ae2925200c9e3213b288672c130ca5d7c) 

#### `public def `[`__init__`](#classbitprim_1_1Chain_1a91d2e01fb06a95e28761bc33580be399)`(self,chain)` 

#### `public def `[`fetch_last_height`](#classbitprim_1_1Chain_1a3b2aaba82203b00addff05747f630443)`(self,handler)` 

Gets the height of the highest block in the chain. 

Args:
    handler (Callable (error, block_height)): Will be executed when the chain is cued. 

* error (int): error code. 0 if successfull.
* block_height (unsigned int): height of the highest block in the chain.

#### `public def `[`fetch_history`](#classbitprim_1_1Chain_1a8654c1cd107ce5455a3bf202a65ee6ac)`(self,address,limit,from_height,handler)` 

Get list of output points, values, and spends for a payment address.

Args:
    address (PaymentAddress): wallet to search.
    limit (unsigned int): max amount of results to fetch.
    from_height (unsigned int): minimum height to search for transactions.
    handler (Callable (error, list)): Will be executed when the chain is cued. 

* error (int): error code. 0 if successfull.
* list (HistoryList): list with every element found.

#### `public def `[`fetch_stealth`](#classbitprim_1_1Chain_1a1b87b8c0f9320c2c2e344297dee65b0f)`(self,binary_filter_str,from_height,handler)` 

Get metadata on potential payment transactions by stealth filter. 
Given a filter and a height in the chain it cues the chain for transactions matching the provided filter.

Args:
    binary_filter_str (string): Must be at least 8 bits in lenght. example "10101010"
    from_height (unsigned int): minimum height in the chain where to look for transactions.
    handler (Callable (error, list)): Will be executed after the chain is cued.

* error (int): error code. 0 if successfull.
* list (StealthList): list with every transaction matching the given filter.

#### `public def `[`fetch_block_height`](#classbitprim_1_1Chain_1a99c62752f73e9b7ef8402863a04ad4a9)`(self,hash,handler)` 

Given a block hash, it cues the chain for the block height. 

Args:
    hash (bytearray): 32 bytes of the block hash.
    handler (Callable (error, block_height)): Will be executed after the chain is cued. 

* error (int): error code. 0 if successfull.
* block_height (unsigned int): height of the block in the chain.

#### `public def `[`fetch_block_header_by_height`](#classbitprim_1_1Chain_1a094aa543335f147e7b6e48ad010ca070)`(self,height,handler)` 

Get the block header from the specified height in the chain.

Args:
    height (unsigned int): block height in the chain.
    handler (Callable (error, block_header)): Will be executed after the chain is cued. 

* error (int): error code. 0 if successfull.
* block_header (Header): header of the block found.

#### `public def `[`fetch_block_header_by_hash`](#classbitprim_1_1Chain_1aad170dbb1d2c7978414221a609856720)`(self,hash,handler)` 

Get the block header from the specified block hash.

Args:
    hash (bytearray): 32 bytes of the block hash.
    handler (Callable (error, block_header)): Will be executed after the chain is cued. 

* error (int): error code. 0 if successfull.
* block_header (Header): header of the block found.

#### `public def `[`fetch_block_by_height`](#classbitprim_1_1Chain_1a284806f124ea0f94efdac5fa679993ad)`(self,height,handler)` 

Gets a block from the specified height in the chain.

Args:
    height (unsigned int): block height in the chain.
    handler (Callable (error, block)): Will be executed after the chain is cued. 

* error (int): error code. 0 if successfull.
* block (Block): block at the defined height in the chain.

#### `public def `[`fetch_block_by_hash`](#classbitprim_1_1Chain_1a6d223f504ce3452988ffc2f84b27b2a4)`(self,hash,handler)` 

Gets a block from the specified hash.

Args:
    hash (bytearray): 32 bytes of the block hash.
    handler (Callable (error, block)): Will be executed after the chain is cued. 

* error (int): error code. 0 if successfull.
* block (Block): block found with the specified hash.

#### `public def `[`fetch_merkle_block_by_height`](#classbitprim_1_1Chain_1ae445ca8c6d5baaa009d08c98634246aa)`(self,height,handler)` 

Given a block height in the chain, it retrieves a merkle block. 

Args:
    height (unsigned int): block height in the chain.
    handler (Callable (error, merkle_block, block_height)): Will be executed when the chain is cued. 

* error (int): error code. 0 if successfull.
* merkle_block (MerkleBlock): merkle block of the block found at the specified height.
* block_height (unsigned int): height of the block in the chain.

#### `public def `[`fetch_merkle_block_by_hash`](#classbitprim_1_1Chain_1a7e4efae5160fe3615e608ec41e71f758)`(self,hash,handler)` 

Given a block hash, it retrieves a merkle block. 

Args:
    hash (bytearray): 32 bytes of the block hash.
    handler (Callable (error, merkle_block, block_height)): Will be executed when the chain is cued. 

* error (int): error code. 0 if successfull.
* merkle_block (MerkleBlock): merkle block of the block found with the given hash.
* block_height (unsigned int): height of the block in the chain.

#### `public def `[`fetch_transaction`](#classbitprim_1_1Chain_1a1d85163b2ba7b815f0bfa997c3dbd442)`(self,hashn,require_confirmed,handler)` 

Get a transaction by its hash. 

Args:
    hashn (bytearray): 32 bytes of the transaction hash.
    require_confirmed (int): if transaction should be in a block. 0 if not.
    handler (Callable (error, transaction, block_height, tx_index)): Will be executed when the chain is cued. 

* error (int): error code. 0 if successfull.
* transaction (Transaction): Transaction found.
* block_height (unsigned int): height in the chain of the block containing the transaction.
* tx_index (unsigned int): index of the transaction inside the block.

#### `public def `[`fetch_output`](#classbitprim_1_1Chain_1a72218a16849f5a0c8054be336658caf1)`(self,hashn,index,require_confirmed,handler)` 

Get a transaction output by its transaction hash and index inside the transaction. 

Args:
    hashn (bytearray): 32 bytes of the transaction hash.
    index (unsigned int): index of the output in the transaction.
    require_confirmed (int): if transaction should be in a block. 0 if not.
    handler (Callable (error, output)): Will be executed when the chain is cued. 

* error (int): error code. 0 if successfull.
* output (Output): output found.

#### `public def `[`fetch_transaction_position`](#classbitprim_1_1Chain_1a5024c70760381fc3eada646bba4a5c8e)`(self,hashn,require_confirmed,handler)` 

Given a transaction hash it fetches the height and position inside the block.

Args:
    hash (bytearray): 32 bytes of the transaction hash.
    require_confirmed (int): if transaction should be in a block. 0 if not.
    handler (Callable (error, block_height, tx_index)): Will be executed after the chain is cued. 

* error (int): error code. 0 if successfull.
* block_height (unsigned int): height of the block containing the transaction.
* tx_index (unsigned int): index in the block of the transaction.

#### `public def `[`validate_tx`](#classbitprim_1_1Chain_1a376f1a70435c94ee95d27dad2c66c6aa)`(self,transaction,handler)` 

Determine if a transaction is valid for submission to the blockchain.

Args:
    transaction (Transaction): transaction to be checked.
    handler (Callable (error, message)): Will be executed after the chain is cued. 

* error (int): error code. 0 if successfull.
* message (str): string describing the result of the cue. example: 'The transaction is valid'

#### `public def `[`fetch_spend`](#classbitprim_1_1Chain_1ae1bd60745bb42815e14901925e6e6558)`(self,output_point,handler)` 

Fetch the transaction input which spends the indicated output. The `fetch_spend_handler` will be executed after cueing the chain. 

Args:
    output_point (OutputPoint): tx hash and index pair.
    handler (Callable (error, input_point)): Will be executed when the chain is cued.

* error (int): error code. 0 if successfull.
* input_point (Point): Tx hash nad index pair where the output was spent.

# class `bitprim::Executor` 

Controls the execution of the Bitprim bitcoin node.

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public def `[`__init__`](#classbitprim_1_1Executor_1af03d07adc2f2ffdac5b3255ee8b69967)`(self,path,sout,serr)` | 
`public def `[`__del__`](#classbitprim_1_1Executor_1a0be33b77505fd6836f22b2177b98a941)`(self)` | 
`public def `[`init_chain`](#classbitprim_1_1Executor_1a963a48bff1fa656636909d41c44ba1dd)`(self)` | bool: Initialization of the blockchain. 
`public def `[`run`](#classbitprim_1_1Executor_1adc2614f1b1a53246eb5c99f57bf50d77)`(self)` | bool: Starts running the node, initializing blockchain download.
`public def `[`run_wait`](#classbitprim_1_1Executor_1a9e6c0c3764214ce25872821141461792)`(self)` | bool: Starts running the node, initializing blockchain download. 
`public def `[`stop`](#classbitprim_1_1Executor_1a8c3abf988c9b8db664548ac9442331d1)`(self)` | bool: it stops the node.
`public def `[`chain`](#classbitprim_1_1Executor_1a6287206dcd5c0d0c87a20f48cf3f5632)`(self)` | Chain: Object containing the blockchain.
`public def `[`__enter__`](#classbitprim_1_1Executor_1ad18cf685fae0e24f51b869b069ec3527)`(self)` | 
`public def `[`__exit__`](#classbitprim_1_1Executor_1a4e694437fd6b419d279c979a0fa8e1de)`(self,exc_type,exc_value,traceback)` | 

## Members

#### `public def `[`__init__`](#classbitprim_1_1Executor_1af03d07adc2f2ffdac5b3255ee8b69967)`(self,path,sout,serr)` 

#### `public def `[`__del__`](#classbitprim_1_1Executor_1a0be33b77505fd6836f22b2177b98a941)`(self)` 

#### `public def `[`init_chain`](#classbitprim_1_1Executor_1a963a48bff1fa656636909d41c44ba1dd)`(self)` 

bool: Initialization of the blockchain. 
Returns 'TRUE' if successfull.

#### `public def `[`run`](#classbitprim_1_1Executor_1adc2614f1b1a53246eb5c99f57bf50d77)`(self)` 

bool: Starts running the node, initializing blockchain download.
Returns 'TRUE' if successful.

#### `public def `[`run_wait`](#classbitprim_1_1Executor_1a9e6c0c3764214ce25872821141461792)`(self)` 

bool: Starts running the node, initializing blockchain download. 
It listen to wait signals.
Returns 'TRUE' if successful.

#### `public def `[`stop`](#classbitprim_1_1Executor_1a8c3abf988c9b8db664548ac9442331d1)`(self)` 

bool: it stops the node.
precondition: self._running.
Returns 'TRUE' if successfull

#### `public def `[`chain`](#classbitprim_1_1Executor_1a6287206dcd5c0d0c87a20f48cf3f5632)`(self)` 

Chain: Object containing the blockchain.

#### `public def `[`__enter__`](#classbitprim_1_1Executor_1ad18cf685fae0e24f51b869b069ec3527)`(self)` 

#### `public def `[`__exit__`](#classbitprim_1_1Executor_1a4e694437fd6b419d279c979a0fa8e1de)`(self,exc_type,exc_value,traceback)` 

# class `bitprim::Header` 

Represent the Header of a Bitcoin Block.

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public def `[`__init__`](#classbitprim_1_1Header_1ab1054610e909b96de1bb2dd8028a765a)`(self,pointer,`[`height`](#classbitprim_1_1Header_1a38f5a0200aa5d54e3bdd9d9cc1a136e5)`,auto_destroy)` | Construction of the Header class object.
`public def `[`__del__`](#classbitprim_1_1Header_1a4b2baea19d3f69d1657398b393829900)`(self)` | 
`public def `[`height`](#classbitprim_1_1Header_1a38f5a0200aa5d54e3bdd9d9cc1a136e5)`(self)` | unsigned int: Height of the block in the chain.
`public def `[`version`](#classbitprim_1_1Header_1a3f3b70f4c986cb07dffe85b5afba040c)`(self)` | unsigned int: protocol version of the header.
`public def `[`set_version`](#classbitprim_1_1Header_1a609e51d54c44345e0ec5dbfb191bc8ce)`(self,`[`version`](#classbitprim_1_1Header_1a3f3b70f4c986cb07dffe85b5afba040c)`)` | 
`public def `[`previous_block_hash`](#classbitprim_1_1Header_1a6f69d5f8a25ca54e0c5f62b907d3d11b)`(self)` | bytearray: 32 bytes hash of the previous block in the chain.
`public def `[`merkle`](#classbitprim_1_1Header_1acb8f6ae7da9ce9fc322cf368cb990dea)`(self)` | bytearray: 32 bytes merkle root.
`public def `[`hash`](#classbitprim_1_1Header_1ab5e63722faa35d7a4842f91b252db8cf)`(self)` | bytearray: 32 bytes block hash.
`public def `[`timestamp`](#classbitprim_1_1Header_1a376f62f26bbb764768bbd877ec0501e4)`(self)` | unsigned int: block timestamp.
`public def `[`set_timestamp`](#classbitprim_1_1Header_1ae47b3d4b8916e020f0f904ac030ba42b)`(self,`[`timestamp`](#classbitprim_1_1Header_1a376f62f26bbb764768bbd877ec0501e4)`)` | 
`public def `[`bits`](#classbitprim_1_1Header_1a9d9b68fb70720ef9ebf16f9bd8d3db41)`(self)` | unsigned int: value of bits. Difficulty threshold.
`public def `[`set_bits`](#classbitprim_1_1Header_1a239f8d73f8d4039bef0880082d877320)`(self,`[`bits`](#classbitprim_1_1Header_1a9d9b68fb70720ef9ebf16f9bd8d3db41)`)` | 
`public def `[`nonce`](#classbitprim_1_1Header_1ac071c7567cb2ab2942baed4044b0c07d)`(self)` | unsigned int: the nonce that allowed this block to added to the blockchain.
`public def `[`set_nonce`](#classbitprim_1_1Header_1aa6db7b91c6d5eb191334973dea3856f0)`(self,`[`nonce`](#classbitprim_1_1Header_1ac071c7567cb2ab2942baed4044b0c07d)`)` | 

## Members

#### `public def `[`__init__`](#classbitprim_1_1Header_1ab1054610e909b96de1bb2dd8028a765a)`(self,pointer,`[`height`](#classbitprim_1_1Header_1a38f5a0200aa5d54e3bdd9d9cc1a136e5)`,auto_destroy)` 

Construction of the Header class object.

Args:
    pointer (Object): pointer to c implementation.
    height (unsigned int): Height of the block in the chain.
    auto_destroy (bool): the object will be deleted when out of scope..

#### `public def `[`__del__`](#classbitprim_1_1Header_1a4b2baea19d3f69d1657398b393829900)`(self)` 

#### `public def `[`height`](#classbitprim_1_1Header_1a38f5a0200aa5d54e3bdd9d9cc1a136e5)`(self)` 

unsigned int: Height of the block in the chain.

#### `public def `[`version`](#classbitprim_1_1Header_1a3f3b70f4c986cb07dffe85b5afba040c)`(self)` 

unsigned int: protocol version of the header.

#### `public def `[`set_version`](#classbitprim_1_1Header_1a609e51d54c44345e0ec5dbfb191bc8ce)`(self,`[`version`](#classbitprim_1_1Header_1a3f3b70f4c986cb07dffe85b5afba040c)`)` 

#### `public def `[`previous_block_hash`](#classbitprim_1_1Header_1a6f69d5f8a25ca54e0c5f62b907d3d11b)`(self)` 

bytearray: 32 bytes hash of the previous block in the chain.

#### `public def `[`merkle`](#classbitprim_1_1Header_1acb8f6ae7da9ce9fc322cf368cb990dea)`(self)` 

bytearray: 32 bytes merkle root.

#### `public def `[`hash`](#classbitprim_1_1Header_1ab5e63722faa35d7a4842f91b252db8cf)`(self)` 

bytearray: 32 bytes block hash.

#### `public def `[`timestamp`](#classbitprim_1_1Header_1a376f62f26bbb764768bbd877ec0501e4)`(self)` 

unsigned int: block timestamp.

#### `public def `[`set_timestamp`](#classbitprim_1_1Header_1ae47b3d4b8916e020f0f904ac030ba42b)`(self,`[`timestamp`](#classbitprim_1_1Header_1a376f62f26bbb764768bbd877ec0501e4)`)` 

#### `public def `[`bits`](#classbitprim_1_1Header_1a9d9b68fb70720ef9ebf16f9bd8d3db41)`(self)` 

unsigned int: value of bits. Difficulty threshold.

#### `public def `[`set_bits`](#classbitprim_1_1Header_1a239f8d73f8d4039bef0880082d877320)`(self,`[`bits`](#classbitprim_1_1Header_1a9d9b68fb70720ef9ebf16f9bd8d3db41)`)` 

#### `public def `[`nonce`](#classbitprim_1_1Header_1ac071c7567cb2ab2942baed4044b0c07d)`(self)` 

unsigned int: the nonce that allowed this block to added to the blockchain.

#### `public def `[`set_nonce`](#classbitprim_1_1Header_1aa6db7b91c6d5eb191334973dea3856f0)`(self,`[`nonce`](#classbitprim_1_1Header_1ac071c7567cb2ab2942baed4044b0c07d)`)` 

# class `bitprim::History` 

Output points, values, and spends for a payment address

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public def `[`__init__`](#classbitprim_1_1History_1a73191eb84c2e5bdf08b8040a3879dde5)`(self,ptr)` | 
`public def `[`point_kind`](#classbitprim_1_1History_1a9ec5efba6a4cc6b1909e293d3e412613)`(self)` | unsigned int: Used for differentiation.
`public def `[`point`](#classbitprim_1_1History_1a851ad89d09c17a1f6da17a9b020a209e)`(self)` | Point: point that identifies History.
`public def `[`height`](#classbitprim_1_1History_1adde220878b3bc05ebc000b12d4013a10)`(self)` | unsigned int: Height of the block containing the Point.
`public def `[`value_or_previous_checksum`](#classbitprim_1_1History_1a836dc64f95577b4e430133f3346bbaee)`(self)` | unsigned int: varies depending of point_kind.

## Members

#### `public def `[`__init__`](#classbitprim_1_1History_1a73191eb84c2e5bdf08b8040a3879dde5)`(self,ptr)` 

#### `public def `[`point_kind`](#classbitprim_1_1History_1a9ec5efba6a4cc6b1909e293d3e412613)`(self)` 

unsigned int: Used for differentiation.
    '0' output
    '1' spend

#### `public def `[`point`](#classbitprim_1_1History_1a851ad89d09c17a1f6da17a9b020a209e)`(self)` 

Point: point that identifies History.

#### `public def `[`height`](#classbitprim_1_1History_1adde220878b3bc05ebc000b12d4013a10)`(self)` 

unsigned int: Height of the block containing the Point.

#### `public def `[`value_or_previous_checksum`](#classbitprim_1_1History_1a836dc64f95577b4e430133f3346bbaee)`(self)` 

unsigned int: varies depending of point_kind.

value: if output, then satoshi value of output.

previous_checksum: if spend, then checksum hash of previous output_point.

# class `bitprim::HistoryList` 

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public  `[`constructed`](#classbitprim_1_1HistoryList_1a0a940029b8c0820b1f64f7123fce997a) | 
`public def `[`__init__`](#classbitprim_1_1HistoryList_1a52db717ce2e113abe759524175991cfb)`(self,ptr)` | 
`public def `[`__del__`](#classbitprim_1_1HistoryList_1a78658958bcfe9062ffe7fad75df4a284)`(self)` | 
`public def `[`count`](#classbitprim_1_1HistoryList_1a121077ffd2e0c1787234489ca2b065e2)`(self)` | 
`public def `[`nth`](#classbitprim_1_1HistoryList_1a78e90bb2ca57368f01dfbcaae0ab5155)`(self,n)` | 
`public def `[`__getitem__`](#classbitprim_1_1HistoryList_1a41a6ea5aeac370e6a51e40497e95947b)`(self,key)` | 

## Members

#### `public  `[`constructed`](#classbitprim_1_1HistoryList_1a0a940029b8c0820b1f64f7123fce997a) 

#### `public def `[`__init__`](#classbitprim_1_1HistoryList_1a52db717ce2e113abe759524175991cfb)`(self,ptr)` 

#### `public def `[`__del__`](#classbitprim_1_1HistoryList_1a78658958bcfe9062ffe7fad75df4a284)`(self)` 

#### `public def `[`count`](#classbitprim_1_1HistoryList_1a121077ffd2e0c1787234489ca2b065e2)`(self)` 

#### `public def `[`nth`](#classbitprim_1_1HistoryList_1a78e90bb2ca57368f01dfbcaae0ab5155)`(self,n)` 

#### `public def `[`__getitem__`](#classbitprim_1_1HistoryList_1a41a6ea5aeac370e6a51e40497e95947b)`(self,key)` 

# class `bitprim::Input` 

Represents one of the inputs of a Transaction.

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public def `[`__init__`](#classbitprim_1_1Input_1ae13083fb6e70555b91861147ebff6329)`(self,ptr)` | 
`public def `[`__del__`](#classbitprim_1_1Input_1aab52e334cbe944496a112bb726b21530)`(self)` | 
`public def `[`is_valid`](#classbitprim_1_1Input_1ae29f9ee24d1a123f1dcce44393de606c)`(self)` | int: returns '0' if previous outputs or script are invalid.
`public def `[`is_final`](#classbitprim_1_1Input_1a76fccbec6192bf842745f7acb26adb85)`(self)` | int: returns '1' if sequence is equal to max_sequence.
`public def `[`serialized_size`](#classbitprim_1_1Input_1a0341dd46f71dd163a7e61fed469e9d15)`(self)` | unsigned int: size in bytes.
`public def `[`sequence`](#classbitprim_1_1Input_1a6116ec3110b937e98c12d4af036d14da)`(self)` | unsigned int: sequence number of inputs. if it equals max_sequence, txs is final.
`public def `[`signature_operations`](#classbitprim_1_1Input_1a29cff0c9139870bdc33225a935e461dd)`(self,bip16_active)` | unsigned int: amount of sigops in the script.
`public def `[`script`](#classbitprim_1_1Input_1a648a39c34feb63d42d658bbeaf88fdc5)`(self)` | Script: script object.
`public def `[`previous_output`](#classbitprim_1_1Input_1af9aec2095f608d93c6a3c31d5fd7adf9)`(self)` | OutputPoint: returns previous output, with transaction hash and index.

## Members

#### `public def `[`__init__`](#classbitprim_1_1Input_1ae13083fb6e70555b91861147ebff6329)`(self,ptr)` 

#### `public def `[`__del__`](#classbitprim_1_1Input_1aab52e334cbe944496a112bb726b21530)`(self)` 

#### `public def `[`is_valid`](#classbitprim_1_1Input_1ae29f9ee24d1a123f1dcce44393de606c)`(self)` 

int: returns '0' if previous outputs or script are invalid.

#### `public def `[`is_final`](#classbitprim_1_1Input_1a76fccbec6192bf842745f7acb26adb85)`(self)` 

int: returns '1' if sequence is equal to max_sequence.

#### `public def `[`serialized_size`](#classbitprim_1_1Input_1a0341dd46f71dd163a7e61fed469e9d15)`(self)` 

unsigned int: size in bytes.

#### `public def `[`sequence`](#classbitprim_1_1Input_1a6116ec3110b937e98c12d4af036d14da)`(self)` 

unsigned int: sequence number of inputs. if it equals max_sequence, txs is final.

#### `public def `[`signature_operations`](#classbitprim_1_1Input_1a29cff0c9139870bdc33225a935e461dd)`(self,bip16_active)` 

unsigned int: amount of sigops in the script.

Args:
    bip16_active (int): '1' if bip 16 is active. '0' if not.

#### `public def `[`script`](#classbitprim_1_1Input_1a648a39c34feb63d42d658bbeaf88fdc5)`(self)` 

Script: script object.

#### `public def `[`previous_output`](#classbitprim_1_1Input_1af9aec2095f608d93c6a3c31d5fd7adf9)`(self)` 

OutputPoint: returns previous output, with transaction hash and index.

# class `bitprim::InputList` 

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public def `[`__init__`](#classbitprim_1_1InputList_1a78cd01531883ead04e5d1f1827afd2f0)`(self,ptr)` | 
`public def `[`push_back`](#classbitprim_1_1InputList_1a57753b4177314fd616ab77f244c4b0c2)`(self,inputn)` | 
`public def `[`list_count`](#classbitprim_1_1InputList_1adc59d443ae7e6ddf904531e0e79eff38)`(self)` | 
`public def `[`__getitem__`](#classbitprim_1_1InputList_1abda9474f6b9bf410d501db3628649483)`(self,key)` | 

## Members

#### `public def `[`__init__`](#classbitprim_1_1InputList_1a78cd01531883ead04e5d1f1827afd2f0)`(self,ptr)` 

#### `public def `[`push_back`](#classbitprim_1_1InputList_1a57753b4177314fd616ab77f244c4b0c2)`(self,inputn)` 

#### `public def `[`list_count`](#classbitprim_1_1InputList_1adc59d443ae7e6ddf904531e0e79eff38)`(self)` 

#### `public def `[`__getitem__`](#classbitprim_1_1InputList_1abda9474f6b9bf410d501db3628649483)`(self,key)` 

# class `bitprim::MerkleBlock` 

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public def `[`__init__`](#classbitprim_1_1MerkleBlock_1a23c009fc36170debc9e12fc94b330dda)`(self,pointer,`[`height`](#classbitprim_1_1MerkleBlock_1ab0ebe70c231ddd6e34769eda3778544b)`)` | 
`public def `[`height`](#classbitprim_1_1MerkleBlock_1ab0ebe70c231ddd6e34769eda3778544b)`(self)` | unsigned int: Height of the block in the chain.
`public def `[`__del__`](#classbitprim_1_1MerkleBlock_1add318592cfd1e07138c9a06648e7b560)`(self)` | 
`public def `[`header`](#classbitprim_1_1MerkleBlock_1a16d8f19f35c6fef29d314fbcc3e325fd)`(self)` | Header: header of the block.
`public def `[`is_valid`](#classbitprim_1_1MerkleBlock_1a8b8e074604860353111fba463d3b3c66)`(self)` | int: returns true if it cointains txs hashes, and header is valid.
`public def `[`hash_count`](#classbitprim_1_1MerkleBlock_1a0cd99a8fda5faaf504f3aed41ccbb3de)`(self)` | unsigned int: size of the transaction hashes list.
`public def `[`serialized_size`](#classbitprim_1_1MerkleBlock_1a4bd735a5ec63b1ab7b505073932fb629)`(self,version)` | unsigned int: size of the block in bytes.
`public def `[`total_transaction_count`](#classbitprim_1_1MerkleBlock_1ae8e7f4689bb58379a42ab18211c7e4ae)`(self)` | unsigned int: transactions included in the block.
`public def `[`reset`](#classbitprim_1_1MerkleBlock_1a27ba9a21dc72f6233f9c9d45946ad13e)`(self)` | void: delete all the data inside the block.

## Members

#### `public def `[`__init__`](#classbitprim_1_1MerkleBlock_1a23c009fc36170debc9e12fc94b330dda)`(self,pointer,`[`height`](#classbitprim_1_1MerkleBlock_1ab0ebe70c231ddd6e34769eda3778544b)`)` 

#### `public def `[`height`](#classbitprim_1_1MerkleBlock_1ab0ebe70c231ddd6e34769eda3778544b)`(self)` 

unsigned int: Height of the block in the chain.

#### `public def `[`__del__`](#classbitprim_1_1MerkleBlock_1add318592cfd1e07138c9a06648e7b560)`(self)` 

#### `public def `[`header`](#classbitprim_1_1MerkleBlock_1a16d8f19f35c6fef29d314fbcc3e325fd)`(self)` 

Header: header of the block.

#### `public def `[`is_valid`](#classbitprim_1_1MerkleBlock_1a8b8e074604860353111fba463d3b3c66)`(self)` 

int: returns true if it cointains txs hashes, and header is valid.

#### `public def `[`hash_count`](#classbitprim_1_1MerkleBlock_1a0cd99a8fda5faaf504f3aed41ccbb3de)`(self)` 

unsigned int: size of the transaction hashes list.

#### `public def `[`serialized_size`](#classbitprim_1_1MerkleBlock_1a4bd735a5ec63b1ab7b505073932fb629)`(self,version)` 

unsigned int: size of the block in bytes.

Args:
    version (unsigned int): block protocol version.

#### `public def `[`total_transaction_count`](#classbitprim_1_1MerkleBlock_1ae8e7f4689bb58379a42ab18211c7e4ae)`(self)` 

unsigned int: transactions included in the block.

#### `public def `[`reset`](#classbitprim_1_1MerkleBlock_1a27ba9a21dc72f6233f9c9d45946ad13e)`(self)` 

void: delete all the data inside the block.

# class `bitprim::Output` 

Represents one of the outputs of a Transaction.

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public def `[`__init__`](#classbitprim_1_1Output_1ac72bdb2e1bb09bef47eda818fd6f1867)`(self,ptr)` | 
`public def `[`__del__`](#classbitprim_1_1Output_1ad7b4b7aa1483e0a2b1e176a709e954c5)`(self)` | 
`public def `[`is_valid`](#classbitprim_1_1Output_1a51b38d7bcdac902c5d3815ebd218175f)`(self)` | int: returns '0' if output is not found.
`public def `[`serialized_size`](#classbitprim_1_1Output_1aac3a6e139f1b5a651e5c957103ee843f)`(self,wire)` | unsigned int: size in bytes.
`public def `[`value`](#classbitprim_1_1Output_1a795ca3150bebcb0ac3cd183869a24586)`(self)` | unsigned int: returns output value.
`public def `[`signature_operations`](#classbitprim_1_1Output_1aca5e32f4be5d0d2ee4e5bb6bc36c395f)`(self)` | unsigned int: amount of signature operations in script.
`public def `[`script`](#classbitprim_1_1Output_1a274170cfeabb30c64f2540054c82dc5c)`(self)` | Script: returns the output script.

## Members

#### `public def `[`__init__`](#classbitprim_1_1Output_1ac72bdb2e1bb09bef47eda818fd6f1867)`(self,ptr)` 

#### `public def `[`__del__`](#classbitprim_1_1Output_1ad7b4b7aa1483e0a2b1e176a709e954c5)`(self)` 

#### `public def `[`is_valid`](#classbitprim_1_1Output_1a51b38d7bcdac902c5d3815ebd218175f)`(self)` 

int: returns '0' if output is not found.

#### `public def `[`serialized_size`](#classbitprim_1_1Output_1aac3a6e139f1b5a651e5c957103ee843f)`(self,wire)` 

unsigned int: size in bytes.

Args:
    wire (bool): if 'TRUE' size will include size of 'uint32' for storing spender height.

#### `public def `[`value`](#classbitprim_1_1Output_1a795ca3150bebcb0ac3cd183869a24586)`(self)` 

unsigned int: returns output value.

#### `public def `[`signature_operations`](#classbitprim_1_1Output_1aca5e32f4be5d0d2ee4e5bb6bc36c395f)`(self)` 

unsigned int: amount of signature operations in script.

#### `public def `[`script`](#classbitprim_1_1Output_1a274170cfeabb30c64f2540054c82dc5c)`(self)` 

Script: returns the output script.

# class `bitprim::OutputList` 

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public def `[`__init__`](#classbitprim_1_1OutputList_1a960450aa4813cbd58396551499623da2)`(self,ptr)` | 
`public def `[`push_back`](#classbitprim_1_1OutputList_1aaf6aaff75f7b2b9b3932c9eb30a80c02)`(self,output)` | 
`public def `[`list_count`](#classbitprim_1_1OutputList_1aa0906a801a9402bbf962f6aa95940c67)`(self)` | 
`public def `[`__getitem__`](#classbitprim_1_1OutputList_1add8fdca3e7916ae48fa88cdc63fcad8d)`(self,key)` | 

## Members

#### `public def `[`__init__`](#classbitprim_1_1OutputList_1a960450aa4813cbd58396551499623da2)`(self,ptr)` 

#### `public def `[`push_back`](#classbitprim_1_1OutputList_1aaf6aaff75f7b2b9b3932c9eb30a80c02)`(self,output)` 

#### `public def `[`list_count`](#classbitprim_1_1OutputList_1aa0906a801a9402bbf962f6aa95940c67)`(self)` 

#### `public def `[`__getitem__`](#classbitprim_1_1OutputList_1add8fdca3e7916ae48fa88cdc63fcad8d)`(self,key)` 

# class `bitprim::OutputPoint` 

Transaction hash and index representing one of the transaction outputs.

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public def `[`__init__`](#classbitprim_1_1OutputPoint_1afa86b39354747b6cec4af931c7ec72b2)`(self,ptr)` | 
`public def `[`hash`](#classbitprim_1_1OutputPoint_1a856c2a088c013a6eb786be10b6559695)`(self)` | bytearray: 32 bytes of the transaction hash.
`public def `[`__del__`](#classbitprim_1_1OutputPoint_1a1ecd26d135fced6148b47ff0935ee148)`(self)` | 
`public def `[`index`](#classbitprim_1_1OutputPoint_1a9f2026dc8ea6f24a951bdcd87d1e12de)`(self)` | unsigned int: position of the output in the transaction.
`public def `[`construct`](#classbitprim_1_1OutputPoint_1a01668dcd11e97994c8c1c5d14a2efa07)`(self)` | OutputPoint: creates an empty output point.
`public def `[`construct_from_hash_index`](#classbitprim_1_1OutputPoint_1a1d421f77d0518ce53469ba18c58c1bbc)`(self,hashn,`[`index`](#classbitprim_1_1OutputPoint_1a9f2026dc8ea6f24a951bdcd87d1e12de)`)` | Outputpoint: creates an OutputPoint from a transaction hash and index pair.

## Members

#### `public def `[`__init__`](#classbitprim_1_1OutputPoint_1afa86b39354747b6cec4af931c7ec72b2)`(self,ptr)` 

#### `public def `[`hash`](#classbitprim_1_1OutputPoint_1a856c2a088c013a6eb786be10b6559695)`(self)` 

bytearray: 32 bytes of the transaction hash.

#### `public def `[`__del__`](#classbitprim_1_1OutputPoint_1a1ecd26d135fced6148b47ff0935ee148)`(self)` 

#### `public def `[`index`](#classbitprim_1_1OutputPoint_1a9f2026dc8ea6f24a951bdcd87d1e12de)`(self)` 

unsigned int: position of the output in the transaction.

#### `public def `[`construct`](#classbitprim_1_1OutputPoint_1a01668dcd11e97994c8c1c5d14a2efa07)`(self)` 

OutputPoint: creates an empty output point.

#### `public def `[`construct_from_hash_index`](#classbitprim_1_1OutputPoint_1a1d421f77d0518ce53469ba18c58c1bbc)`(self,hashn,`[`index`](#classbitprim_1_1OutputPoint_1a9f2026dc8ea6f24a951bdcd87d1e12de)`)` 

Outputpoint: creates an OutputPoint from a transaction hash and index pair.

Args:

    hashn (bytearray): 32 bytes of the transaction hash.
    index (unsigned int): position of the output in the transaction.

# class `bitprim::PaymentAddress` 

Represents a Bitcoin wallet address.

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public def `[`__init__`](#classbitprim_1_1PaymentAddress_1a716ff66b7cfa1bab2049d6809b7144fd)`(self,ptr)` | 
`public def `[`encoded`](#classbitprim_1_1PaymentAddress_1a44c336a955badc58d015de528cf04c44)`(self)` | str: readable format of the address.
`public def `[`version`](#classbitprim_1_1PaymentAddress_1a53ccf810b1ad7d0ef3c6fd20a8cf5c61)`(self)` | unsigned int: address version.
`public def `[`construct_from_string`](#classbitprim_1_1PaymentAddress_1ad585e303e02efc54442cc983f71176d8)`(self,address)` | Creates the Payment Address based on the received string.

## Members

#### `public def `[`__init__`](#classbitprim_1_1PaymentAddress_1a716ff66b7cfa1bab2049d6809b7144fd)`(self,ptr)` 

#### `public def `[`encoded`](#classbitprim_1_1PaymentAddress_1a44c336a955badc58d015de528cf04c44)`(self)` 

str: readable format of the address.

#### `public def `[`version`](#classbitprim_1_1PaymentAddress_1a53ccf810b1ad7d0ef3c6fd20a8cf5c61)`(self)` 

unsigned int: address version.

#### `public def `[`construct_from_string`](#classbitprim_1_1PaymentAddress_1ad585e303e02efc54442cc983f71176d8)`(self,address)` 

Creates the Payment Address based on the received string.

Args:
    address(str): a base58 address. example '1MLVpZC2CTFHheox8SCEnAbW5NBdewRTdR'

# class `bitprim::Point` 

Represents one of the txs input.
It's a pair of transaction hash and index.

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public def `[`__init__`](#classbitprim_1_1Point_1a1b2ccac61ef8fe0f2f61aaf58c98fb6c)`(self,ptr)` | 
`public def `[`hash`](#classbitprim_1_1Point_1a46bdd0b6d7df9c3576654b5a091a7263)`(self)` | Hash of the transaction.
`public def `[`is_valid`](#classbitprim_1_1Point_1a6adb5ce23e3ffdd311d07f1fda16d387)`(self)` | returns true if its not null.
`public def `[`index`](#classbitprim_1_1Point_1a876f64f8a82b16ea369a2f1dd4c61be2)`(self)` | Position of the Input in the transaction.
`public def `[`checksum`](#classbitprim_1_1Point_1a547cbaeb732a493881566efc0cc02f9a)`(self)` | This is used with output_point identification within a set of history rows

## Members

#### `public def `[`__init__`](#classbitprim_1_1Point_1a1b2ccac61ef8fe0f2f61aaf58c98fb6c)`(self,ptr)` 

#### `public def `[`hash`](#classbitprim_1_1Point_1a46bdd0b6d7df9c3576654b5a091a7263)`(self)` 

Hash of the transaction.

Returns:
    bytearray: 32 bytes.

#### `public def `[`is_valid`](#classbitprim_1_1Point_1a6adb5ce23e3ffdd311d07f1fda16d387)`(self)` 

returns true if its not null.

Returns:
    bool

#### `public def `[`index`](#classbitprim_1_1Point_1a876f64f8a82b16ea369a2f1dd4c61be2)`(self)` 

Position of the Input in the transaction.

Returns:
    unsigned int.

#### `public def `[`checksum`](#classbitprim_1_1Point_1a547cbaeb732a493881566efc0cc02f9a)`(self)` 

This is used with output_point identification within a set of history rows
of the same address. Collision will result in miscorrelation of points by
client callers. This is NOT a bitcoin checksum.

Returns:
    unsigned int.

# class `bitprim::Script` 

Represents transaction scripts.

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public def `[`__init__`](#classbitprim_1_1Script_1a71167ed9cb1444e1bbed71834469ee05)`(self,ptr,auto_destroy)` | 
`public def `[`__del__`](#classbitprim_1_1Script_1adc903b82b180174f84576bc0389bbf1f)`(self)` | 
`public def `[`is_valid`](#classbitprim_1_1Script_1a5a22ae4af12fd6fc4c2c40f30802da2c)`(self)` | int: All script bytes are valid under some circumstance (e.g. coinbase).
`public def `[`is_valid_operations`](#classbitprim_1_1Script_1a611ffd4030e23d79d54ae18950f9e024)`(self)` | int: Script validity is independent of individual operation validity.
`public def `[`satoshi_content_size`](#classbitprim_1_1Script_1aeca70284e86f8042d28e77e31cd0a894)`(self)` | unsigned int: size in bytes.
`public def `[`serialized_size`](#classbitprim_1_1Script_1a5347d3490612815abb1a009d45abf880)`(self,prefix)` | unsigned int: size in bytes. If prefix '1' size includes a var int size. 
`public def `[`to_string`](#classbitprim_1_1Script_1a8a77d30fc38c0b278aedbc59af993d8e)`(self,active_forks)` | str: translate operations in the script to string. 
`public def `[`sigops`](#classbitprim_1_1Script_1ab0dffa99e266f48d352ece4ddf4f5a4f)`(self,embedded)` | unsigned int: amount of signature operations in the script.
`public def `[`embedded_sigops`](#classbitprim_1_1Script_1a87b18a27b56aa2c5309c9bbd43fdfd76)`(self,prevout_script)` | unsigned int: Count the sigops in the embedded script using BIP16 rules.

## Members

#### `public def `[`__init__`](#classbitprim_1_1Script_1a71167ed9cb1444e1bbed71834469ee05)`(self,ptr,auto_destroy)` 

#### `public def `[`__del__`](#classbitprim_1_1Script_1adc903b82b180174f84576bc0389bbf1f)`(self)` 

#### `public def `[`is_valid`](#classbitprim_1_1Script_1a5a22ae4af12fd6fc4c2c40f30802da2c)`(self)` 

int: All script bytes are valid under some circumstance (e.g. coinbase).
Returns '0' if a prefix and byte count does not match.

#### `public def `[`is_valid_operations`](#classbitprim_1_1Script_1a611ffd4030e23d79d54ae18950f9e024)`(self)` 

int: Script validity is independent of individual operation validity.
There is a trailing invalid/default op if a push op had a size mismatch.

#### `public def `[`satoshi_content_size`](#classbitprim_1_1Script_1aeca70284e86f8042d28e77e31cd0a894)`(self)` 

unsigned int: size in bytes.

#### `public def `[`serialized_size`](#classbitprim_1_1Script_1a5347d3490612815abb1a009d45abf880)`(self,prefix)` 

unsigned int: size in bytes. If prefix '1' size includes a var int size. 

Args:
    prefix (bool): include prefix size in the final result.

#### `public def `[`to_string`](#classbitprim_1_1Script_1a8a77d30fc38c0b278aedbc59af993d8e)`(self,active_forks)` 

str: translate operations in the script to string. 

Args:
    active_forks (unsigned int): which rule is active.

#### `public def `[`sigops`](#classbitprim_1_1Script_1ab0dffa99e266f48d352ece4ddf4f5a4f)`(self,embedded)` 

unsigned int: amount of signature operations in the script.

Args:
    embedded (bool): is embedded script.

#### `public def `[`embedded_sigops`](#classbitprim_1_1Script_1a87b18a27b56aa2c5309c9bbd43fdfd76)`(self,prevout_script)` 

unsigned int: Count the sigops in the embedded script using BIP16 rules.

# class `bitprim::Stealth` 

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public def `[`__init__`](#classbitprim_1_1Stealth_1a66223b8a9e25e938b27fb90e305131b6)`(self,ptr)` | 
`public def `[`ephemeral_public_key_hash`](#classbitprim_1_1Stealth_1ac5b81ac8a33db2fc11076c7741944c5b)`(self)` | bytearray: 33 bytes. Includes  the sign byte (0x02)
`public def `[`transaction_hash`](#classbitprim_1_1Stealth_1a0c2c65c2e7956f422da41e405945ed8b)`(self)` | bytearray: 32 bytes.
`public def `[`public_key_hash`](#classbitprim_1_1Stealth_1a91e692b85f2aca1bff55cef53a7d8f7f)`(self)` | bytearray: 20 bytes.

## Members

#### `public def `[`__init__`](#classbitprim_1_1Stealth_1a66223b8a9e25e938b27fb90e305131b6)`(self,ptr)` 

#### `public def `[`ephemeral_public_key_hash`](#classbitprim_1_1Stealth_1ac5b81ac8a33db2fc11076c7741944c5b)`(self)` 

bytearray: 33 bytes. Includes  the sign byte (0x02)

#### `public def `[`transaction_hash`](#classbitprim_1_1Stealth_1a0c2c65c2e7956f422da41e405945ed8b)`(self)` 

bytearray: 32 bytes.

#### `public def `[`public_key_hash`](#classbitprim_1_1Stealth_1a91e692b85f2aca1bff55cef53a7d8f7f)`(self)` 

bytearray: 20 bytes.

# class `bitprim::StealthCompact` 

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public def `[`__init__`](#classbitprim_1_1StealthCompact_1a096b83602f54149f4a057b2f5e0b537b)`(self,ptr)` | 
`public def `[`ephemeral_public_key_hash`](#classbitprim_1_1StealthCompact_1a321f69a0c64289dd915079e6eb0f34e8)`(self)` | bytearray: 32 bytes. Excludes the sign byte (0x02)
`public def `[`transaction_hash`](#classbitprim_1_1StealthCompact_1afc2e71f2147e7c788ce9f475281f2e20)`(self)` | bytearray: 32 bytes.
`public def `[`public_key_hash`](#classbitprim_1_1StealthCompact_1a62d4aaec36ca9aa5a544097fa9bed367)`(self)` | bytearray: 20 bytes.

## Members

#### `public def `[`__init__`](#classbitprim_1_1StealthCompact_1a096b83602f54149f4a057b2f5e0b537b)`(self,ptr)` 

#### `public def `[`ephemeral_public_key_hash`](#classbitprim_1_1StealthCompact_1a321f69a0c64289dd915079e6eb0f34e8)`(self)` 

bytearray: 32 bytes. Excludes the sign byte (0x02)

#### `public def `[`transaction_hash`](#classbitprim_1_1StealthCompact_1afc2e71f2147e7c788ce9f475281f2e20)`(self)` 

bytearray: 32 bytes.

#### `public def `[`public_key_hash`](#classbitprim_1_1StealthCompact_1a62d4aaec36ca9aa5a544097fa9bed367)`(self)` 

bytearray: 20 bytes.

# class `bitprim::StealthCompactList` 

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public def `[`__init__`](#classbitprim_1_1StealthCompactList_1a80eb34701f18beaddfc056bc81e046c5)`(self,ptr)` | 
`public def `[`__del__`](#classbitprim_1_1StealthCompactList_1a00aedbc6e343018dfb192dc7fbd1773e)`(self)` | 
`public def `[`list_count`](#classbitprim_1_1StealthCompactList_1a9d76141b462701811573a90d4a87f9b9)`(self)` | 
`public def `[`__getitem__`](#classbitprim_1_1StealthCompactList_1a13259edfd3730528a6f025bfc09b9c2d)`(self,key)` | 

## Members

#### `public def `[`__init__`](#classbitprim_1_1StealthCompactList_1a80eb34701f18beaddfc056bc81e046c5)`(self,ptr)` 

#### `public def `[`__del__`](#classbitprim_1_1StealthCompactList_1a00aedbc6e343018dfb192dc7fbd1773e)`(self)` 

#### `public def `[`list_count`](#classbitprim_1_1StealthCompactList_1a9d76141b462701811573a90d4a87f9b9)`(self)` 

#### `public def `[`__getitem__`](#classbitprim_1_1StealthCompactList_1a13259edfd3730528a6f025bfc09b9c2d)`(self,key)` 

# class `bitprim::StealthList` 

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public  `[`constructed`](#classbitprim_1_1StealthList_1a84aebac541d7b2c7601c6f6d2aca2832) | 
`public def `[`__init__`](#classbitprim_1_1StealthList_1a8ba200a5cb697338d42c5950c8dc5735)`(self,ptr)` | 
`public def `[`__del__`](#classbitprim_1_1StealthList_1a6e55a0d3c29eeb27f5150c7758cd3dfb)`(self)` | 
`public def `[`count`](#classbitprim_1_1StealthList_1a12f2cede95c9e4b47ae9aeff6c7b2ff7)`(self)` | 
`public def `[`nth`](#classbitprim_1_1StealthList_1a2565c5589877c4b44979148f1ac91eed)`(self,n)` | 
`public def `[`__getitem__`](#classbitprim_1_1StealthList_1af8ab11d6980e5e5873f41e0acea9df49)`(self,key)` | 

## Members

#### `public  `[`constructed`](#classbitprim_1_1StealthList_1a84aebac541d7b2c7601c6f6d2aca2832) 

#### `public def `[`__init__`](#classbitprim_1_1StealthList_1a8ba200a5cb697338d42c5950c8dc5735)`(self,ptr)` 

#### `public def `[`__del__`](#classbitprim_1_1StealthList_1a6e55a0d3c29eeb27f5150c7758cd3dfb)`(self)` 

#### `public def `[`count`](#classbitprim_1_1StealthList_1a12f2cede95c9e4b47ae9aeff6c7b2ff7)`(self)` 

#### `public def `[`nth`](#classbitprim_1_1StealthList_1a2565c5589877c4b44979148f1ac91eed)`(self,n)` 

#### `public def `[`__getitem__`](#classbitprim_1_1StealthList_1af8ab11d6980e5e5873f41e0acea9df49)`(self,key)` 

# class `bitprim::Transaction` 

Represents a Bitcoin Transaction.

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public def `[`__init__`](#classbitprim_1_1Transaction_1a46725d5acd8c3a8fb06522f401ea204c)`(self,ptr)` | 
`public def `[`__del__`](#classbitprim_1_1Transaction_1a282bbff062532d2589e8ef4fcde173aa)`(self)` | 
`public def `[`version`](#classbitprim_1_1Transaction_1aa78e3b53addcba62cd4417de17aad628)`(self)` | unsigned int: Transaction protocol version.
`public def `[`set_version`](#classbitprim_1_1Transaction_1ae17721a2689408ef4dd28f407eefeb88)`(self,`[`version`](#classbitprim_1_1Transaction_1aa78e3b53addcba62cd4417de17aad628)`)` | 
`public def `[`hash`](#classbitprim_1_1Transaction_1aa679c88ddf7e352528c71bf3ae797ec9)`(self)` | bytearray: 32 bytes transaction hash.
`public def `[`hash_sighash_type`](#classbitprim_1_1Transaction_1ac4b2912c9d68a47cdc8bcdd15c520d89)`(self,sighash_type)` | bytearray: 32 bytes transaction hash.
`public def `[`locktime`](#classbitprim_1_1Transaction_1aab337d983f698afa256bf38287b26820)`(self)` | unsigned int: transaction locktime.
`public def `[`serialized_size`](#classbitprim_1_1Transaction_1af007310b3682d57b74ee70f944cb883e)`(self,wire)` | unsigned int: size of the transaction in bytes.
`public def `[`fees`](#classbitprim_1_1Transaction_1a9ee46a7fc71ab7c9a74322c628802186)`(self)` | unsigned int: fees to pay. Difference between input and output value.
`public def `[`signature_operations`](#classbitprim_1_1Transaction_1ade18c210a75584010597d76fde6b33f8)`(self)` | unsigned int: amount of signature operations in the transaction. 
`public def `[`signature_operations_bip16_active`](#classbitprim_1_1Transaction_1a5897d20624e799b44b458a391fc8aa40)`(self,bip16_active)` | unsigned int: amount of signature operations in the transaction.
`public def `[`total_input_value`](#classbitprim_1_1Transaction_1ac8298d1f71febab13fe5f9b4f539e3ed)`(self)` | unsigned int: sum of every input value in the transaction.
`public def `[`total_output_value`](#classbitprim_1_1Transaction_1a3e3774f262498777003e86eed9d9381d)`(self)` | unsigned int: sum of every output value in the transaction.
`public def `[`is_coinbase`](#classbitprim_1_1Transaction_1ae7d6a8dd291a15968fa5f078a53af242)`(self)` | int: return '1' if transaction is coinbase.
`public def `[`is_null_non_coinbase`](#classbitprim_1_1Transaction_1a5539ce12185ded041ab9ce5b2a775485)`(self)` | int: return '1' if is not coinbase, but has null previous output.
`public def `[`is_oversized_coinbase`](#classbitprim_1_1Transaction_1a4c9a6cb88c82d9d8da7ef4db54dac402)`(self)` | int: returns '1' if coinbase has invalid script size on first input.
`public def `[`is_immature`](#classbitprim_1_1Transaction_1ad2cc8a92dc67e58db75ea3afe606342e)`(self,target_height)` | int: returns '1' if at least one of the inputs is not mature.
`public def `[`is_overspent`](#classbitprim_1_1Transaction_1afc10506073f96f853693d3f2049751ee)`(self)` | int: returns '1' if it is not a coinbase, and outputs value is higher than its inputs.
`public def `[`is_double_spend`](#classbitprim_1_1Transaction_1a4c9912869aa7f16772490a56718dabd2)`(self,include_unconfirmed)` | int: returns '1' if at least one of the previous outputs was already spent.
`public def `[`is_missing_previous_outputs`](#classbitprim_1_1Transaction_1ac4a82072535321b6563cbf0fb70c715a)`(self)` | int: returns '1' if at least one of the previous outputs is invalid.
`public def `[`is_final`](#classbitprim_1_1Transaction_1a814e76e41eac39d0d106a1bf26a879fc)`(self,block_height,block_time)` | int: returns '1' if transaction is final.
`public def `[`is_locktime_conflict`](#classbitprim_1_1Transaction_1ac269016ed1aea06944f1e5d273637ffb)`(self)` | int: returns '1' if its locked, but every input is final.
`public def `[`outputs`](#classbitprim_1_1Transaction_1a1d4f613af7fbd60d2421309fa967461f)`(self)` | OutputList: returns a list with every transaction output.
`public def `[`inputs`](#classbitprim_1_1Transaction_1acd7f943c9d0e9f3c76fddbb1d7c3db3b)`(self)` | InputList: returns a list with every transaction input.

## Members

#### `public def `[`__init__`](#classbitprim_1_1Transaction_1a46725d5acd8c3a8fb06522f401ea204c)`(self,ptr)` 

#### `public def `[`__del__`](#classbitprim_1_1Transaction_1a282bbff062532d2589e8ef4fcde173aa)`(self)` 

#### `public def `[`version`](#classbitprim_1_1Transaction_1aa78e3b53addcba62cd4417de17aad628)`(self)` 

unsigned int: Transaction protocol version.

#### `public def `[`set_version`](#classbitprim_1_1Transaction_1ae17721a2689408ef4dd28f407eefeb88)`(self,`[`version`](#classbitprim_1_1Transaction_1aa78e3b53addcba62cd4417de17aad628)`)` 

#### `public def `[`hash`](#classbitprim_1_1Transaction_1aa679c88ddf7e352528c71bf3ae797ec9)`(self)` 

bytearray: 32 bytes transaction hash.

#### `public def `[`hash_sighash_type`](#classbitprim_1_1Transaction_1ac4b2912c9d68a47cdc8bcdd15c520d89)`(self,sighash_type)` 

bytearray: 32 bytes transaction hash.

Args: 
    sighash_type (unsigned int): signature hash type.

#### `public def `[`locktime`](#classbitprim_1_1Transaction_1aab337d983f698afa256bf38287b26820)`(self)` 

unsigned int: transaction locktime.

#### `public def `[`serialized_size`](#classbitprim_1_1Transaction_1af007310b3682d57b74ee70f944cb883e)`(self,wire)` 

unsigned int: size of the transaction in bytes.

Args:
    wire (bool): if 'TRUE' size will include size of 'uint32' for storing spender height of output.

#### `public def `[`fees`](#classbitprim_1_1Transaction_1a9ee46a7fc71ab7c9a74322c628802186)`(self)` 

unsigned int: fees to pay. Difference between input and output value.

#### `public def `[`signature_operations`](#classbitprim_1_1Transaction_1ade18c210a75584010597d76fde6b33f8)`(self)` 

unsigned int: amount of signature operations in the transaction. 
Returns max int in case of overflow.

#### `public def `[`signature_operations_bip16_active`](#classbitprim_1_1Transaction_1a5897d20624e799b44b458a391fc8aa40)`(self,bip16_active)` 

unsigned int: amount of signature operations in the transaction.
Returns max int in case of overflow.

Args:

    bip16_active (int): '1' if bip 16 is active. '0' if not.

#### `public def `[`total_input_value`](#classbitprim_1_1Transaction_1ac8298d1f71febab13fe5f9b4f539e3ed)`(self)` 

unsigned int: sum of every input value in the transaction.
Returns max int in case of overflow.

#### `public def `[`total_output_value`](#classbitprim_1_1Transaction_1a3e3774f262498777003e86eed9d9381d)`(self)` 

unsigned int: sum of every output value in the transaction.
return max int in case of overflow.

#### `public def `[`is_coinbase`](#classbitprim_1_1Transaction_1ae7d6a8dd291a15968fa5f078a53af242)`(self)` 

int: return '1' if transaction is coinbase.

#### `public def `[`is_null_non_coinbase`](#classbitprim_1_1Transaction_1a5539ce12185ded041ab9ce5b2a775485)`(self)` 

int: return '1' if is not coinbase, but has null previous output.

#### `public def `[`is_oversized_coinbase`](#classbitprim_1_1Transaction_1a4c9a6cb88c82d9d8da7ef4db54dac402)`(self)` 

int: returns '1' if coinbase has invalid script size on first input.

#### `public def `[`is_immature`](#classbitprim_1_1Transaction_1ad2cc8a92dc67e58db75ea3afe606342e)`(self,target_height)` 

int: returns '1' if at least one of the inputs is not mature.

#### `public def `[`is_overspent`](#classbitprim_1_1Transaction_1afc10506073f96f853693d3f2049751ee)`(self)` 

int: returns '1' if it is not a coinbase, and outputs value is higher than its inputs.

#### `public def `[`is_double_spend`](#classbitprim_1_1Transaction_1a4c9912869aa7f16772490a56718dabd2)`(self,include_unconfirmed)` 

int: returns '1' if at least one of the previous outputs was already spent.

#### `public def `[`is_missing_previous_outputs`](#classbitprim_1_1Transaction_1ac4a82072535321b6563cbf0fb70c715a)`(self)` 

int: returns '1' if at least one of the previous outputs is invalid.

#### `public def `[`is_final`](#classbitprim_1_1Transaction_1a814e76e41eac39d0d106a1bf26a879fc)`(self,block_height,block_time)` 

int: returns '1' if transaction is final.

#### `public def `[`is_locktime_conflict`](#classbitprim_1_1Transaction_1ac269016ed1aea06944f1e5d273637ffb)`(self)` 

int: returns '1' if its locked, but every input is final.

#### `public def `[`outputs`](#classbitprim_1_1Transaction_1a1d4f613af7fbd60d2421309fa967461f)`(self)` 

OutputList: returns a list with every transaction output.

#### `public def `[`inputs`](#classbitprim_1_1Transaction_1acd7f943c9d0e9f3c76fddbb1d7c3db3b)`(self)` 

InputList: returns a list with every transaction input.

# class `bitprim::TransactionList` 

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public def `[`__init__`](#classbitprim_1_1TransactionList_1a026cda25b13f6571665fac38e25dc76f)`(self,ptr)` | 
`public def `[`__del__`](#classbitprim_1_1TransactionList_1a934e710f5cfb72c40312702fa9c0a188)`(self)` | 
`public def `[`construct_default`](#classbitprim_1_1TransactionList_1a6d85dafaf12acf196c0a2fa04a380288)`(self)` | 
`public def `[`push_back`](#classbitprim_1_1TransactionList_1a8923845ba6327427e13786ff136790d4)`(self,transaction)` | 
`public def `[`list_count`](#classbitprim_1_1TransactionList_1a93e3ab285e7b747a3af2927e4a8ca9f5)`(self)` | 
`public def `[`__getitem__`](#classbitprim_1_1TransactionList_1a997cffbbab6cfdcbb976e14ae7c3b09c)`(self,key)` | 

## Members

#### `public def `[`__init__`](#classbitprim_1_1TransactionList_1a026cda25b13f6571665fac38e25dc76f)`(self,ptr)` 

#### `public def `[`__del__`](#classbitprim_1_1TransactionList_1a934e710f5cfb72c40312702fa9c0a188)`(self)` 

#### `public def `[`construct_default`](#classbitprim_1_1TransactionList_1a6d85dafaf12acf196c0a2fa04a380288)`(self)` 

#### `public def `[`push_back`](#classbitprim_1_1TransactionList_1a8923845ba6327427e13786ff136790d4)`(self,transaction)` 

#### `public def `[`list_count`](#classbitprim_1_1TransactionList_1a93e3ab285e7b747a3af2927e4a8ca9f5)`(self)` 

#### `public def `[`__getitem__`](#classbitprim_1_1TransactionList_1a997cffbbab6cfdcbb976e14ae7c3b09c)`(self,key)` 

# class `bitprim::Wallet` 

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public def `[`mnemonics_to_seed`](#classbitprim_1_1Wallet_1a4a8552caf0d1d1ff6bc8fdfc54b3a47f)`(cls,mnemonics)` | 

## Members

#### `public def `[`mnemonics_to_seed`](#classbitprim_1_1Wallet_1a4a8552caf0d1d1ff6bc8fdfc54b3a47f)`(cls,mnemonics)` 

Generated by [Moxygen](https://sourcey.com/moxygen)