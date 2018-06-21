# Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`enum `[`point_kind`](#primitives_8h_1a4de8699f33816d833b0d9a69fb08fc8a)            | 0 = output, 1 = spend
`public void `[`block_destruct`](#block_8h_1ac0c31d7ecb4f682fac067a179cc468d1)`(`[`block_t`](#primitives_8h_1a8ed39cb12068667c597f544ec838ccc4)` block)`            | Release the memory held by a block object.
`public int `[`block_is_valid`](#block_8h_1af7395388b4f83298636e05de96b8bb7f)`(`[`block_t`](#primitives_8h_1a8ed39cb12068667c597f544ec838ccc4)` block)`            | Determine if a block is valid.
`public `[`header_t`](#primitives_8h_1ae6323fbfdc3ff99f33acbae250895ab8)` `[`block_header`](#block_8h_1aa644a0753e3d370f683883aecc37a199)`(`[`block_t`](#primitives_8h_1a8ed39cb12068667c597f544ec838ccc4)` block)`            | Get the block's header.
`public `[`hash_t`](#primitives_8h_1aa0ccd30c9c9fb169daec5f65600e7c71)` `[`block_hash`](#block_8h_1a30cfad237bdb5bebe5fd7e3b48f3d410)`(`[`block_t`](#primitives_8h_1a8ed39cb12068667c597f544ec838ccc4)` block)`            | Get the block's hash.
`public size_t `[`block_transaction_count`](#block_8h_1a7efc8cd7a41f4dfe6286629ab9ebe59b)`(`[`block_t`](#primitives_8h_1a8ed39cb12068667c597f544ec838ccc4)` block)`            | Get the block's transaction count.
`public `[`transaction_t`](#primitives_8h_1a5618f23f10ca9f9ad96cf52f4059e995)` `[`block_transaction_nth`](#block_8h_1a0732e73992d9c4c4789fc54f39e8747a)`(`[`block_t`](#primitives_8h_1a8ed39cb12068667c597f544ec838ccc4)` block,size_t n)`            | Get the block's n-th transaction.
`public size_t `[`block_serialized_size`](#block_8h_1a5b8666350465a4501cb3e8002085a2b1)`(`[`block_t`](#primitives_8h_1a8ed39cb12068667c597f544ec838ccc4)` block,uint32_t version)`            | Get the block's serialized size.
`public uint64_t `[`block_subsidy`](#block_8h_1a6c9f4dca5ff1fc402d405e4216a82d86)`(size_t height)`            | Get the block subsidy (miner_reward = block_subsidy + transaction_fees)
`public uint64_t `[`block_fees`](#block_8h_1a0ee8cfa6d663b50aff057932efb0eeaa)`(`[`block_t`](#primitives_8h_1a8ed39cb12068667c597f544ec838ccc4)` block)`            | Get the block's total transaction fees (miner_reward = block_subsidy + transaction_fees)
`public uint64_t `[`block_claim`](#block_8h_1a4a1d431723d6e90f80894bb6b6a9c213)`(`[`block_t`](#primitives_8h_1a8ed39cb12068667c597f544ec838ccc4)` block)`            | Get the block's claim.
`public uint64_t `[`block_reward`](#block_8h_1af91de8cf3d009d9bb291f3fdac1c35dd)`(`[`block_t`](#primitives_8h_1a8ed39cb12068667c597f544ec838ccc4)` block,size_t height)`            | Get the block's miner reward (miner_reward = block_subsidy + transaction_fees)
`public `[`hash_t`](#primitives_8h_1aa0ccd30c9c9fb169daec5f65600e7c71)` `[`block_generate_merkle_root`](#block_8h_1accd9987fa1b37396e047f6e8b2251c12)`(`[`block_t`](#primitives_8h_1a8ed39cb12068667c597f544ec838ccc4)` block)`            | Generate a Merkle root for a block.
`public size_t `[`block_signature_operations`](#block_8h_1a0095ecbd424497725258918fc0c07acc)`(`[`block_t`](#primitives_8h_1a8ed39cb12068667c597f544ec838ccc4)` block)`            | Get the block's signature operations count.
`public size_t `[`block_signature_operations_bip16_active`](#block_8h_1adbc5bcd535157b8fca7e9869db80d68d)`(`[`block_t`](#primitives_8h_1a8ed39cb12068667c597f544ec838ccc4)` block,int bip16_active)`            | Get the block's BIP0016 signature operations count.
`public size_t `[`block_total_inputs`](#block_8h_1aded82b46e51e35812902beec2e60c508)`(`[`block_t`](#primitives_8h_1a8ed39cb12068667c597f544ec838ccc4)` block,int with_coinbase)`            | Get the block's input count.
`public int `[`block_is_extra_coinbases`](#block_8h_1acda164be7d985af0e920396fd5dbf438)`(`[`block_t`](#primitives_8h_1a8ed39cb12068667c597f544ec838ccc4)` block)`            | Determine if a block has extra coinbases.
`public int `[`block_is_final`](#block_8h_1aa3b0657e9a9141472d62e61b6ff7800a)`(`[`block_t`](#primitives_8h_1a8ed39cb12068667c597f544ec838ccc4)` block,size_t height)`            | Determine if a block is final.
`public int `[`block_is_distinct_transaction_set`](#block_8h_1a2a7648c49fb07ad150013289522e9a62)`(`[`block_t`](#primitives_8h_1a8ed39cb12068667c597f544ec838ccc4)` block)`            | Determine if a block contains a distinct transaction set.
`public int `[`block_is_valid_coinbase_claim`](#block_8h_1a18fb299820f406654184facc727f6359)`(`[`block_t`](#primitives_8h_1a8ed39cb12068667c597f544ec838ccc4)` block,size_t height)`            | Determine if a block contains a valid coinbase claim.
`public int `[`block_is_valid_coinbase_script`](#block_8h_1aa8e9758dd0e41b4ebcf0daef7cb50af2)`(`[`block_t`](#primitives_8h_1a8ed39cb12068667c597f544ec838ccc4)` block,size_t height)`            | Determine if a block contains a valid coinbase script.
`public int `[`block_is_internal_double_spend`](#block_8h_1a7c4a0d1bd346fe47a8f0022427b47b9c)`(`[`block_t`](#primitives_8h_1a8ed39cb12068667c597f544ec838ccc4)` block)`            | Determine if a block contains an internal double spend.
`public int `[`block_is_valid_merkle_root`](#block_8h_1ae3e37f3180a5403625db8bdbe6d105ee)`(`[`block_t`](#primitives_8h_1a8ed39cb12068667c597f544ec838ccc4)` block)`            | Determine if a block has a valid Merkle root.
`public `[`header_t`](#primitives_8h_1ae6323fbfdc3ff99f33acbae250895ab8)` `[`compact_block_header`](#compact__block_8h_1a8cf34d1187d38c7d6201453289a19d5c)`(`[`compact_block_t`](#primitives_8h_1a43ccacc67cf17b4bf244f421228028ad)` block)`            | Get compact block header.
`public int `[`compact_block_is_valid`](#compact__block_8h_1accb0d739d132cbed90dc3495886a05b0)`(`[`compact_block_t`](#primitives_8h_1a43ccacc67cf17b4bf244f421228028ad)` block)`            | Determine if a compact block is valid.
`public size_t `[`compact_block_serialized_size`](#compact__block_8h_1aa96e45a0eb41a7d8bcfe03340d8e502b)`(`[`compact_block_t`](#primitives_8h_1a43ccacc67cf17b4bf244f421228028ad)` block,uint32_t version)`            | Get a compact block's serialized size.
`public size_t `[`compact_block_transaction_count`](#compact__block_8h_1ae0785b7c6e06c6cb188c94fa0da5b98c)`(`[`compact_block_t`](#primitives_8h_1a43ccacc67cf17b4bf244f421228028ad)` block)`            | Get the compact block's transaction count.
`public `[`transaction_t`](#primitives_8h_1a5618f23f10ca9f9ad96cf52f4059e995)` `[`compact_block_transaction_nth`](#compact__block_8h_1ad271eeb9ab8a4148a4065e380cb8213b)`(`[`compact_block_t`](#primitives_8h_1a43ccacc67cf17b4bf244f421228028ad)` block,size_t n)`            | Get a compact block's n-th transaction.
`public uint64_t `[`compact_block_nonce`](#compact__block_8h_1aebea00334de2af9b07f9e6a9acd333d7)`(`[`compact_block_t`](#primitives_8h_1a43ccacc67cf17b4bf244f421228028ad)` block)`            | Get compact block's nonce.
`public void `[`compact_block_destruct`](#compact__block_8h_1ace80b5f64b9e64e7c53c65d98a3cae4c)`(`[`compact_block_t`](#primitives_8h_1a43ccacc67cf17b4bf244f421228028ad)` block)`            | Release memory held by compact block instance.
`public void `[`compact_block_reset`](#compact__block_8h_1a24b85a581e03ba42eafbe80f276bf01a)`(`[`compact_block_t`](#primitives_8h_1a43ccacc67cf17b4bf244f421228028ad)` block)`            | Reset compact block.
`public `[`executor_t`](#primitives_8h_1a383e6acdb0d5f5df837fc1838b71fc51)` `[`executor_construct`](#executor__c_8h_1aed246db742bdb2aeee6842a8743ea094)`(char const * path,FILE * sout,FILE * serr)`            | Creates an executor instance, which controls a node in the network.
`public `[`executor_t`](#primitives_8h_1a383e6acdb0d5f5df837fc1838b71fc51)` `[`executor_construct_fd`](#executor__c_8h_1ad9e4e0f23310637271e442585696de0c)`(char const * path,int sout_fd,int serr_fd)`            | Creates an executor instance, which controls a node in the network.
`public void `[`executor_destruct`](#executor__c_8h_1a963f4bbda682b0bdf66d73a374a1ac89)`(`[`executor_t`](#primitives_8h_1a383e6acdb0d5f5df837fc1838b71fc51)` exec)`            | Destroys an executor instance (it only releases memory)
`public void `[`executor_run`](#executor__c_8h_1a53815abff7a75a5c963b342f8aa2f8bf)`(`[`executor_t`](#primitives_8h_1a383e6acdb0d5f5df837fc1838b71fc51)` exec,`[`run_handler_t`](#primitives_8h_1a042c0a527cc2744c80e2565a7b7beb9e)` handler)`            | After [executor_initchain()](#executor__c_8h_1a5edfd9a2012e7345e9908a6d80baeaf6) has been called, the node can be started using this function. This is an asynchronous function, hence the callback parameter.
`public int `[`executor_run_wait`](#executor__c_8h_1abd814e409c84aac34363c21452cabd58)`(`[`executor_t`](#primitives_8h_1a383e6acdb0d5f5df837fc1838b71fc51)` exec)`            | After [executor_initchain()](#executor__c_8h_1a5edfd9a2012e7345e9908a6d80baeaf6) has been called, the node can be started using this function. This is a synchronous function, so it will block until node has started running.
`public int `[`executor_initchain`](#executor__c_8h_1a5edfd9a2012e7345e9908a6d80baeaf6)`(`[`executor_t`](#primitives_8h_1a383e6acdb0d5f5df837fc1838b71fc51)` exec)`            | Initializes the chain for this node. It only creates the structure; the blockchain won't be synced.
`public void `[`executor_stop`](#executor__c_8h_1a80a0e1814db0a389e0ae7ba1a43c78e8)`(`[`executor_t`](#primitives_8h_1a383e6acdb0d5f5df837fc1838b71fc51)` exec)`            | Stops execution of the node.
`public void `[`fetch_last_height`](#executor__c_8h_1a83a045615b9be929f3331ef5302ec772)`(`[`executor_t`](#primitives_8h_1a383e6acdb0d5f5df837fc1838b71fc51)` exec,`[`last_height_fetch_handler_t`](#primitives_8h_1a7319bd077428255061dc7c773ebc0cc4)` handler)`            | Get the current blockchain height.
`public int `[`get_last_height`](#executor__c_8h_1a791b814d3928a00faa6138ea2d33c5b9)`(`[`executor_t`](#primitives_8h_1a383e6acdb0d5f5df837fc1838b71fc51)` exec,size_t * height)`            | Get the current blockchain height. This is the synchronous version of [fetch_last_height()](#executor__c_8h_1a83a045615b9be929f3331ef5302ec772), so it will block until height is retrieved from the network, or an error occurs.
`public void `[`fetch_block_height`](#executor__c_8h_1a903aec1424b51b8810273cf5642b70d0)`(`[`executor_t`](#primitives_8h_1a383e6acdb0d5f5df837fc1838b71fc51)` exec,`[`hash_t`](#primitives_8h_1aa0ccd30c9c9fb169daec5f65600e7c71)` hash,`[`block_height_fetch_handler_t`](#primitives_8h_1a7f26119f3693225e3698e80e8d7e64c9)` handler)`            | Given a block, get its height in the blockchain.
`public int `[`get_block_height`](#executor__c_8h_1a0c140100f1eefa4dc6707e93568fdcc1)`(`[`executor_t`](#primitives_8h_1a383e6acdb0d5f5df837fc1838b71fc51)` exec,`[`hash_t`](#primitives_8h_1aa0ccd30c9c9fb169daec5f65600e7c71)` hash,size_t * height)`            | Given a block, get its height in the blockchain. This is the synchronous version of [fetch_block_height()](#executor__c_8h_1a903aec1424b51b8810273cf5642b70d0), so it will block until height is retrieved from the network, or an error occurs.
`public void `[`fetch_block_header_by_height`](#executor__c_8h_1ae4d491f18285c2b31b6261683ef5679b)`(`[`executor_t`](#primitives_8h_1a383e6acdb0d5f5df837fc1838b71fc51)` exec,size_t height,`[`block_header_fetch_handler_t`](#primitives_8h_1a175320d3fdee884d5b1daba1f51af6cf)` handler)`            | Given a height in the blockchain, retrieve its block's header.
`public int `[`get_block_header_by_height`](#executor__c_8h_1a2b2cb61fd05544b98a8829c6fc357a06)`(`[`executor_t`](#primitives_8h_1a383e6acdb0d5f5df837fc1838b71fc51)` exec,size_t height,`[`header_t`](#primitives_8h_1ae6323fbfdc3ff99f33acbae250895ab8)` * header,size_t * ret_height)`            | Given a height in the blockchain, retrieve its block's header. This is the synchronous version of [fetch_block_header_by_height()](#executor__c_8h_1ae4d491f18285c2b31b6261683ef5679b), so it will block until the header is retrieved from the network, or an error occurs.
`public void `[`fetch_block_header_by_hash`](#executor__c_8h_1a660eb713c231f3daa2a1cfb5fbfa4bd4)`(`[`executor_t`](#primitives_8h_1a383e6acdb0d5f5df837fc1838b71fc51)` exec,`[`hash_t`](#primitives_8h_1aa0ccd30c9c9fb169daec5f65600e7c71)` hash,`[`block_header_fetch_handler_t`](#primitives_8h_1a175320d3fdee884d5b1daba1f51af6cf)` handler)`            | Given a block hash, retrieve its header.
`public int `[`get_block_header_by_hash`](#executor__c_8h_1a21e7310364624f505d7e16190fe1fa3c)`(`[`executor_t`](#primitives_8h_1a383e6acdb0d5f5df837fc1838b71fc51)` exec,`[`hash_t`](#primitives_8h_1aa0ccd30c9c9fb169daec5f65600e7c71)` hash,`[`header_t`](#primitives_8h_1ae6323fbfdc3ff99f33acbae250895ab8)` * header,size_t * ret_height)`            | Given a block hash, retrieve its header. This is the synchronous version of [fetch_block_header_by_height()](#executor__c_8h_1ae4d491f18285c2b31b6261683ef5679b), so it will block until the header is retrieved from the network, or an error occurs.
`public void `[`fetch_block_by_height`](#executor__c_8h_1a1ce9ccf736baf9f52e26093e7787f7a3)`(`[`executor_t`](#primitives_8h_1a383e6acdb0d5f5df837fc1838b71fc51)` exec,size_t height,`[`block_fetch_handler_t`](#primitives_8h_1a8c1fb1e052b08b1188d614222a9de9b2)` handler)`            | Given a block's height, retrieve the block.
`public int `[`get_block_by_height`](#executor__c_8h_1a1887b7fb6d869838e66afd19a09b50d2)`(`[`executor_t`](#primitives_8h_1a383e6acdb0d5f5df837fc1838b71fc51)` exec,size_t height,`[`block_t`](#primitives_8h_1a8ed39cb12068667c597f544ec838ccc4)` * block,size_t * ret_height)`            | Given a block's height, retrieve the block. This is the synchronous version of [fetch_block_by_height()](#executor__c_8h_1a1ce9ccf736baf9f52e26093e7787f7a3), so it will block until the block is retrieved from the network, or an error occurs.
`public void `[`fetch_block_by_hash`](#executor__c_8h_1a0e2e7826e0ed92f46f06fb7c50d0b5e2)`(`[`executor_t`](#primitives_8h_1a383e6acdb0d5f5df837fc1838b71fc51)` exec,`[`hash_t`](#primitives_8h_1aa0ccd30c9c9fb169daec5f65600e7c71)` hash,`[`block_fetch_handler_t`](#primitives_8h_1a8c1fb1e052b08b1188d614222a9de9b2)` handler)`            | Given a block's hash, retrieve the block.
`public int `[`get_block_by_hash`](#executor__c_8h_1a13e08557af5950a19019e4ff55791d12)`(`[`executor_t`](#primitives_8h_1a383e6acdb0d5f5df837fc1838b71fc51)` exec,`[`hash_t`](#primitives_8h_1aa0ccd30c9c9fb169daec5f65600e7c71)` hash,`[`block_t`](#primitives_8h_1a8ed39cb12068667c597f544ec838ccc4)` * block,size_t * ret_height)`            | Given a block's hash, retrieve the block. This is the synchronous version of [fetch_block_by_height()](#executor__c_8h_1a1ce9ccf736baf9f52e26093e7787f7a3), so it will block until the block is retrieved from the network, or an error occurs.
`public void `[`fetch_merkle_block_by_height`](#executor__c_8h_1a8133807dfb7628a247f191608976c47b)`(`[`executor_t`](#primitives_8h_1a383e6acdb0d5f5df837fc1838b71fc51)` exec,size_t height,`[`merkle_block_fetch_handler_t`](#primitives_8h_1aff6e1e0990f9e15ea36d9a1ce64890ff)` handler)`            | Given a Merkle block's height, retrieve the block.
`public void `[`fetch_merkle_block_by_hash`](#executor__c_8h_1aca145cfaa6db94792255beef98e57b94)`(`[`executor_t`](#primitives_8h_1a383e6acdb0d5f5df837fc1838b71fc51)` exec,`[`hash_t`](#primitives_8h_1aa0ccd30c9c9fb169daec5f65600e7c71)` hash,`[`merkle_block_fetch_handler_t`](#primitives_8h_1aff6e1e0990f9e15ea36d9a1ce64890ff)` handler)`            | Given a Merkle block's hash, retrieve the block.
`public void `[`fetch_compact_block_by_height`](#executor__c_8h_1a553b3ba0d2df8d9c3cc0d544f570d976)`(`[`executor_t`](#primitives_8h_1a383e6acdb0d5f5df837fc1838b71fc51)` exec,size_t height,`[`compact_block_fetch_handler_t`](#primitives_8h_1ae4895924faf7b39c24a050618ebf6c51)` handler)`            | Given a compact block's height, retrieve the block.
`public void `[`fetch_compact_block_by_hash`](#executor__c_8h_1a7a2060ab5f19214db5431646c98a09b8)`(`[`executor_t`](#primitives_8h_1a383e6acdb0d5f5df837fc1838b71fc51)` exec,`[`hash_t`](#primitives_8h_1aa0ccd30c9c9fb169daec5f65600e7c71)` hash,`[`compact_block_fetch_handler_t`](#primitives_8h_1ae4895924faf7b39c24a050618ebf6c51)` handler)`            | Given a compact block's hash, retrieve the block.
`public void `[`fetch_transaction`](#executor__c_8h_1a99a0cbcfe63b6381c738d21bd7826b3d)`(`[`executor_t`](#primitives_8h_1a383e6acdb0d5f5df837fc1838b71fc51)` exec,`[`hash_t`](#primitives_8h_1aa0ccd30c9c9fb169daec5f65600e7c71)` hash,int require_confirmed,`[`transaction_fetch_handler_t`](#primitives_8h_1ae0808043043d84636e3a2e3c754b8fd6)` handler)`            | Given a transaction hash, retrieve it (optionally requiring it to be confirmed)
`public int `[`get_transaction`](#executor__c_8h_1a7f74db96f0bd243d3568c771896d3a24)`(`[`executor_t`](#primitives_8h_1a383e6acdb0d5f5df837fc1838b71fc51)` exec,`[`hash_t`](#primitives_8h_1aa0ccd30c9c9fb169daec5f65600e7c71)` hash,int require_confirmed,`[`transaction_t`](#primitives_8h_1a5618f23f10ca9f9ad96cf52f4059e995)` * transaction,size_t * ret_height,size_t * index)`            | Given a transaction's hash, retrieve it This is the synchronous version of [fetch_transaction()](#executor__c_8h_1a99a0cbcfe63b6381c738d21bd7826b3d), so it will block until the transaction is retrieved from the network, or an error occurs.
`public void `[`fetch_transaction_position`](#executor__c_8h_1a699c29f962fa7c4302ee04b21cf82a9a)`(`[`executor_t`](#primitives_8h_1a383e6acdb0d5f5df837fc1838b71fc51)` exec,`[`hash_t`](#primitives_8h_1aa0ccd30c9c9fb169daec5f65600e7c71)` hash,int require_confirmed,`[`transaction_index_fetch_handler_t`](#primitives_8h_1a83733f3195e3e03a0d9f4cc822b48a3d)` handler)`            | Given a transaction hash, retrieve its position inside the block (optionally requiring it to be confirmed)
`public void `[`fetch_output`](#executor__c_8h_1afcc2cb87a88aabb6a712435cee9abc9a)`(`[`executor_t`](#primitives_8h_1a383e6acdb0d5f5df837fc1838b71fc51)` exec,`[`hash_t`](#primitives_8h_1aa0ccd30c9c9fb169daec5f65600e7c71)` hash,uint32_t index,int require_confirmed,`[`output_fetch_handler_t`](#primitives_8h_1aefbd8dfda0d008880de7c60bcf23dde9)` handler)`            | Given an output hash, retrieve it (optionally requiring it to be confirmed)
`public int `[`get_output`](#executor__c_8h_1a8d35fe3911046137e8cace26f8a3c938)`(`[`executor_t`](#primitives_8h_1a383e6acdb0d5f5df837fc1838b71fc51)` exec,`[`hash_t`](#primitives_8h_1aa0ccd30c9c9fb169daec5f65600e7c71)` hash,uint32_t index,int require_confirmed,`[`output_t`](#primitives_8h_1a6db821b2b1332e8be7a662d075ede0b0)` * output)`            | Given an output's hash, retrieve it This is the synchronous version of [fetch_output()](#executor__c_8h_1afcc2cb87a88aabb6a712435cee9abc9a), so it will block until the output is retrieved from the network, or an error occurs.
`public void `[`fetch_spend`](#executor__c_8h_1a4966f126f69c313903cbf0f46be79f9d)`(`[`executor_t`](#primitives_8h_1a383e6acdb0d5f5df837fc1838b71fc51)` exec,`[`output_point_t`](#primitives_8h_1ad4d5035e7d5ca4f6a10eafdfdfd2e074)` outpoint,`[`spend_fetch_handler_t`](#primitives_8h_1aae597f1c61dc1dc585f5425375300ce3)` handler)`            | Given an output point, retrieve its spend.
`public void `[`fetch_history`](#executor__c_8h_1a6ca41df13a8c7d67781d3a6005841ba6)`(`[`executor_t`](#primitives_8h_1a383e6acdb0d5f5df837fc1838b71fc51)` exec,`[`payment_address_t`](#primitives_8h_1acc9e0ae61a6bf90f01911484e4ede07b)` address,size_t limit,size_t from_height,`[`history_fetch_handler_t`](#primitives_8h_1aee0367afd480cf2771d49690c567c25a)` handler)`            | Given a payment address, a starting height and an entry limit, retrieve its transaction history.
`public int `[`get_history`](#executor__c_8h_1a1760fe0ef7ec0479230bf77ca7a2ea21)`(`[`executor_t`](#primitives_8h_1a383e6acdb0d5f5df837fc1838b71fc51)` exec,`[`payment_address_t`](#primitives_8h_1acc9e0ae61a6bf90f01911484e4ede07b)` address,size_t limit,size_t from_height,`[`history_compact_list_t`](#primitives_8h_1aa9b635e04d3d0e124549cbef8b147638)` * out_history)`            | Given a payment address, a starting height and an entry limit, retrieve its transaction history This is the synchronous version of [fetch_history()](#executor__c_8h_1a6ca41df13a8c7d67781d3a6005841ba6), so it will block until the history is retrieved from the network, or an error occurs.
`public `[`transaction_t`](#primitives_8h_1a5618f23f10ca9f9ad96cf52f4059e995)` `[`hex_to_tx`](#executor__c_8h_1a8af262d3a75ff3da484cbbccac8a987a)`(char const * tx_hex)`            | Converts a raw transaction hex string to a transaction object.
`public void `[`validate_tx`](#executor__c_8h_1a26fae1c08f21b9f8097e944ebc8ebcc4)`(`[`executor_t`](#primitives_8h_1a383e6acdb0d5f5df837fc1838b71fc51)` exec,`[`transaction_t`](#primitives_8h_1a5618f23f10ca9f9ad96cf52f4059e995)` tx,`[`validate_tx_handler_t`](#primitives_8h_1a4a5ad506c3c92b9308072dcc1815ec17)` handler)`            | Validates a new transaction (has not been added to the blockchain yet)
`public `[`long_hash_t`](#primitives_8h_1a15a7913e47813e6707bf348da7203f1a)` `[`wallet_mnemonics_to_seed`](#executor__c_8h_1abfdab2c4350be9e094478db62f440547)`(`[`word_list_t`](#primitives_8h_1a547ee5b6df76cdddedd5e12dea357036)` mnemonics)`            | Convert a set of keywords/mnemonics to an HD wallet seed.
`public void `[`long_hash_destroy`](#executor__c_8h_1a636893dd40262d359bde53923e0a5d1c)`(`[`long_hash_t`](#primitives_8h_1a15a7913e47813e6707bf348da7203f1a)` ptr)`            | Release the memory held by a long hash object.
`public void `[`header_destruct`](#header_8h_1a1d1d3fc9341337e1bddd2681fdfed682)`(`[`header_t`](#primitives_8h_1ae6323fbfdc3ff99f33acbae250895ab8)` header)`            | Releases memory held by the header object.
`public int `[`header_is_valid`](#header_8h_1adaabb8aadd2c899fc4c7361532b1fd8e)`(`[`header_t`](#primitives_8h_1ae6323fbfdc3ff99f33acbae250895ab8)` header)`            | Determine if the header is valid.
`public uint32_t `[`header_version`](#header_8h_1a59dc1762a22e8a9ee84c66e20660767b)`(`[`header_t`](#primitives_8h_1ae6323fbfdc3ff99f33acbae250895ab8)` header)`            | Get header version.
`public void `[`header_set_version`](#header_8h_1af95ba2aea724401b648863129ab40a02)`(`[`header_t`](#primitives_8h_1ae6323fbfdc3ff99f33acbae250895ab8)` header,uint32_t version)`            | Set a header's version.
`public uint32_t `[`header_timestamp`](#header_8h_1aa72c883fde1a10067725e0772c6e687f)`(`[`header_t`](#primitives_8h_1ae6323fbfdc3ff99f33acbae250895ab8)` header)`            | Get header timestamp.
`public void `[`header_set_timestamp`](#header_8h_1a29d0a46719548d37c95fc4e1a456353a)`(`[`header_t`](#primitives_8h_1ae6323fbfdc3ff99f33acbae250895ab8)` header,uint32_t timestamp)`            | Set header timestamp.
`public uint32_t `[`header_bits`](#header_8h_1a6a505d7f8f1137fe68b6b096ed35a15a)`(`[`header_t`](#primitives_8h_1ae6323fbfdc3ff99f33acbae250895ab8)` header)`            | Get header bits.
`public void `[`header_set_bits`](#header_8h_1ad9acf477b496b3d6d632b70483dfad81)`(`[`header_t`](#primitives_8h_1ae6323fbfdc3ff99f33acbae250895ab8)` header,uint32_t bits)`            | Set header bits.
`public uint32_t `[`header_nonce`](#header_8h_1acb3466f0d21884c5ba4c272571440610)`(`[`header_t`](#primitives_8h_1ae6323fbfdc3ff99f33acbae250895ab8)` header)`            | Get header nonce.
`public void `[`header_set_nonce`](#header_8h_1ab4dd1bb2ed0a537cf237e7dc82184d0c)`(`[`header_t`](#primitives_8h_1ae6323fbfdc3ff99f33acbae250895ab8)` header,uint32_t nonce)`            | Set header nonce 
`public `[`hash_t`](#primitives_8h_1aa0ccd30c9c9fb169daec5f65600e7c71)` `[`header_previous_block_hash`](#header_8h_1ac048f31bf04639f83e5be544adf9b977)`(`[`header_t`](#primitives_8h_1ae6323fbfdc3ff99f33acbae250895ab8)` header)`            | Get previous block hash.
`public `[`hash_t`](#primitives_8h_1aa0ccd30c9c9fb169daec5f65600e7c71)` `[`header_merkle`](#header_8h_1af0f199ca6fed2c5cc37fedfe5dd86b47)`(`[`header_t`](#primitives_8h_1ae6323fbfdc3ff99f33acbae250895ab8)` header)`            | Get header Merkle.
`public `[`hash_t`](#primitives_8h_1aa0ccd30c9c9fb169daec5f65600e7c71)` `[`header_hash`](#header_8h_1a625887dacbb1b408e292e0ff6a5638fc)`(`[`header_t`](#primitives_8h_1ae6323fbfdc3ff99f33acbae250895ab8)` header)`            | Get header hash.
`public `[`point_kind_t`](#primitives_8h_1a6f08d747fe788aa53ad4e70e58230078)` `[`history_compact_get_point_kind`](#history__compact_8h_1ad821d566985946fe24bc56f95d3a89c2)`(`[`history_compact_t`](#primitives_8h_1afecbcaff5ab6fec4cda05ca77abb093d)` history)`            | Get the entry's point kind.
`public `[`point_t`](#primitives_8h_1af6e7950f472a081d958eb8519843d38b)` `[`history_compact_get_point`](#history__compact_8h_1a86510b343ae158fb7ceefbdbdb92a304)`(`[`history_compact_t`](#primitives_8h_1afecbcaff5ab6fec4cda05ca77abb093d)` history)`            | Get the entry's point.
`public uint32_t `[`history_compact_get_height`](#history__compact_8h_1abbe2e7a92e48a0a32b261bcdfd723f07)`(`[`history_compact_t`](#primitives_8h_1afecbcaff5ab6fec4cda05ca77abb093d)` history)`            | Get the height of history entry in the blockchain.
`public uint64_t `[`history_compact_get_value_or_previous_checksum`](#history__compact_8h_1a3421ce4d489fbda735d8de833bd1e090)`(`[`history_compact_t`](#primitives_8h_1afecbcaff5ab6fec4cda05ca77abb093d)` history)`            | Get the entry's value.
`public void `[`history_compact_list_destruct`](#history__compact__list_8h_1aec9ce8654f6d88baf7deab18764e9b52)`(`[`history_compact_list_t`](#primitives_8h_1aa9b635e04d3d0e124549cbef8b147638)` history_compact_list)`            | Release memory held by a history compact list instance.
`public size_t `[`history_compact_list_count`](#history__compact__list_8h_1a9e3ccd8686469993bb94a73ceb3bac65)`(`[`history_compact_list_t`](#primitives_8h_1aa9b635e04d3d0e124549cbef8b147638)` history_compact_list)`            | Get the amount of entries in the list.
`public `[`history_compact_t`](#primitives_8h_1afecbcaff5ab6fec4cda05ca77abb093d)` `[`history_compact_list_nth`](#history__compact__list_8h_1ad202250e8072936b89cb9381034c05a7)`(`[`history_compact_list_t`](#primitives_8h_1aa9b635e04d3d0e124549cbef8b147638)` history_list,size_t n)`            | Get the list's n-th entry.
`public void `[`input_destruct`](#input_8h_1a07e22ee2679bf79e657229c161e6c669)`(`[`input_t`](#primitives_8h_1acb1903f2f2f7ed4502a5f53615cff8aa)` input)`            | Release the memory held by an input instance.
`public int `[`input_is_valid`](#input_8h_1a2403b0b3e70fc82976302dce797feeb8)`(`[`input_t`](#primitives_8h_1acb1903f2f2f7ed4502a5f53615cff8aa)` input)`            | Determine if an input is valid.
`public int `[`input_is_final`](#input_8h_1ad4c90e8e665df2478bbe2861cf16f3ce)`(`[`input_t`](#primitives_8h_1acb1903f2f2f7ed4502a5f53615cff8aa)` input)`            | Determine if an input is final.
`public size_t `[`input_serialized_size`](#input_8h_1ac5ce4f197473b950042053bc378311e1)`(`[`input_t`](#primitives_8h_1acb1903f2f2f7ed4502a5f53615cff8aa)` input,int wire)`            | Get the input's serialized size.
`public uint32_t `[`input_sequence`](#input_8h_1a17ca854ca78275acddea0a46bcf241f9)`(`[`input_t`](#primitives_8h_1acb1903f2f2f7ed4502a5f53615cff8aa)` input)`            | Get the input's sequence number.
`public size_t `[`input_signature_operations`](#input_8h_1a6112eeed9ced97e9b8a65535d259b455)`(`[`input_t`](#primitives_8h_1acb1903f2f2f7ed4502a5f53615cff8aa)` input,int bip16_active)`            | Get the input's signature operations count.
`public `[`script_t`](#primitives_8h_1a14a6f2e8d8ccced8b9bf7844e22e4aef)` `[`input_script`](#input_8h_1a5962a64778d3825861968bd7b93f37ca)`(`[`input_t`](#primitives_8h_1acb1903f2f2f7ed4502a5f53615cff8aa)` input)`            | Get input script.
`public `[`output_point_t`](#primitives_8h_1ad4d5035e7d5ca4f6a10eafdfdfd2e074)` `[`input_previous_output`](#input_8h_1a6117fe1c39f484f7fef1d76df61cb514)`(`[`input_t`](#primitives_8h_1acb1903f2f2f7ed4502a5f53615cff8aa)` input)`            | Get the input's previous output.
`public `[`hash_t`](#primitives_8h_1aa0ccd30c9c9fb169daec5f65600e7c71)` `[`merkle_block_hash_nth`](#merkle__block_8h_1ae8c9b3a6d6573a51ab7908ae8dd82f78)`(`[`merkle_block_t`](#primitives_8h_1a17bcda76594c1a89acd36ec09d5e41a9)` block,size_t n)`            | Get the block's n-th hash.
`public `[`header_t`](#primitives_8h_1ae6323fbfdc3ff99f33acbae250895ab8)` `[`merkle_block_header`](#merkle__block_8h_1ad4ee91f14e5bab50b388c5438ad59698)`(`[`merkle_block_t`](#primitives_8h_1a17bcda76594c1a89acd36ec09d5e41a9)` block)`            | Get Merkle block header.
`public int `[`merkle_block_is_valid`](#merkle__block_8h_1ab0176f1b613f53a57476828a302a4178)`(`[`merkle_block_t`](#primitives_8h_1a17bcda76594c1a89acd36ec09d5e41a9)` block)`            | Determine if a Merkle block is valid.
`public size_t `[`merkle_block_hash_count`](#merkle__block_8h_1acb42d10ee086d6093266b98840da6c6b)`(`[`merkle_block_t`](#primitives_8h_1a17bcda76594c1a89acd36ec09d5e41a9)` block)`            | Get Merkle block hash count.
`public size_t `[`merkle_block_serialized_size`](#merkle__block_8h_1afb2d66d2e76d8e409b736cd7d0383302)`(`[`merkle_block_t`](#primitives_8h_1a17bcda76594c1a89acd36ec09d5e41a9)` block,uint32_t version)`            | Get Merkle block serialized size.
`public size_t `[`merkle_block_total_transaction_count`](#merkle__block_8h_1afb0c146c7501223601376a6144c953d6)`(`[`merkle_block_t`](#primitives_8h_1a17bcda76594c1a89acd36ec09d5e41a9)` block)`            | Get Merkle block transaction count.
`public void `[`merkle_block_destruct`](#merkle__block_8h_1af871439cfb75225e78af8e3454a20ca3)`(`[`merkle_block_t`](#primitives_8h_1a17bcda76594c1a89acd36ec09d5e41a9)` block)`            | Release memory held by Merkle block instance.
`public void `[`merkle_block_reset`](#merkle__block_8h_1a45c8fca631807d31b893cff090e480e0)`(`[`merkle_block_t`](#primitives_8h_1a17bcda76594c1a89acd36ec09d5e41a9)` block)`            | Reset Merkle block.
`public void `[`output_destruct`](#output_8h_1a974f0d91520ed93250bcd56e2d921590)`(`[`output_t`](#primitives_8h_1a6db821b2b1332e8be7a662d075ede0b0)` output)`            | Release memory held by an output instance.
`public int `[`output_is_valid`](#output_8h_1a0d68a3cfb17807c9a72c5e36a5ee15ce)`(`[`output_t`](#primitives_8h_1a6db821b2b1332e8be7a662d075ede0b0)` output)`            | Determine if an output is valid.
`public size_t `[`output_serialized_size`](#output_8h_1a24adac96e97aa036e0336b309c71fd39)`(`[`output_t`](#primitives_8h_1a6db821b2b1332e8be7a662d075ede0b0)` output,int wire)`            | Get the output's serialized size.
`public uint64_t `[`output_value`](#output_8h_1ab6f944581267dbc41e2fa251f2ff7546)`(`[`output_t`](#primitives_8h_1a6db821b2b1332e8be7a662d075ede0b0)` output)`            | Get the output's value.
`public size_t `[`output_signature_operations`](#output_8h_1a4cbbc9de86c223a7f473c18e8a86f305)`(`[`output_t`](#primitives_8h_1a6db821b2b1332e8be7a662d075ede0b0)` output)`            | Get the output signature operations count.
`public `[`script_t`](#primitives_8h_1a14a6f2e8d8ccced8b9bf7844e22e4aef)` `[`output_script`](#output_8h_1a8d1f20140cb6d480fbfe0e2622fa5065)`(`[`output_t`](#primitives_8h_1a6db821b2b1332e8be7a662d075ede0b0)` output)`            | : Get the output's script
`public `[`hash_t`](#primitives_8h_1aa0ccd30c9c9fb169daec5f65600e7c71)` `[`output_get_hash`](#output_8h_1aabd1bd7f280dc40de4e81b3470bb1ab4)`(`[`output_t`](#primitives_8h_1a6db821b2b1332e8be7a662d075ede0b0)` output)`            | Get output hash.
`public uint32_t `[`output_get_index`](#output_8h_1a0c90a1cb8f51f0a7451a965582a677fb)`(`[`output_t`](#primitives_8h_1a6db821b2b1332e8be7a662d075ede0b0)` output)`            | Get the output's index.
`public `[`hash_t`](#primitives_8h_1aa0ccd30c9c9fb169daec5f65600e7c71)` `[`output_point_get_hash`](#output__point_8h_1ac9f315a515685375a2b015f2afe17eef)`(`[`output_point_t`](#primitives_8h_1ad4d5035e7d5ca4f6a10eafdfdfd2e074)` output)`            | Get the output point's hash.
`public `[`output_point_t`](#primitives_8h_1ad4d5035e7d5ca4f6a10eafdfdfd2e074)` `[`output_point_construct`](#output__point_8h_1aeb7c309b991761bff5cdc4c5cdcbad1e)`()`            | Create an empty output point.
`public uint32_t `[`output_point_get_index`](#output__point_8h_1a496394e7491a75771b40d85c400665c2)`(`[`output_point_t`](#primitives_8h_1ad4d5035e7d5ca4f6a10eafdfdfd2e074)` output)`            | Get output point index inside the point. Starts at 0 (zero) with the first one.
`public void `[`output_point_destruct`](#output__point_8h_1a4ae2358a29f31e9a0351585fbf61b993)`(`[`output_point_t`](#primitives_8h_1ad4d5035e7d5ca4f6a10eafdfdfd2e074)` output)`            | Release memory held by output point.
`public char const  * `[`payment_address_encoded`](#payment__address_8h_1a51b00cfb74d43f59cf2ca2e735a2f7f1)`(`[`payment_address_t`](#primitives_8h_1acc9e0ae61a6bf90f01911484e4ede07b)` payment_address)`            | Encode a payment address.
`public `[`payment_address_t`](#primitives_8h_1acc9e0ae61a6bf90f01911484e4ede07b)` `[`payment_address_construct_from_string`](#payment__address_8h_1a266e2071493b7ed6c7ff9bc9eb80b8fb)`(char const * address)`            | Create a payment address from a string.
`public uint8_t `[`version`](#payment__address_8h_1a20d1238557cc4df561e5b09816ea9450)`(`[`payment_address_t`](#primitives_8h_1acc9e0ae61a6bf90f01911484e4ede07b)` payment_address)`            | Get payment address version.
`public void `[`payment_address_destruct`](#payment__address_8h_1a4b3dbd5712e7c6569c02763e0dfe4baa)`(`[`payment_address_t`](#primitives_8h_1acc9e0ae61a6bf90f01911484e4ede07b)` payment_address)`            | Release memory held by payment address instance.
`public `[`hash_t`](#primitives_8h_1aa0ccd30c9c9fb169daec5f65600e7c71)` `[`point_get_hash`](#point_8h_1a2a624b2b8a7f329d9962b7a1924e12ab)`(`[`point_t`](#primitives_8h_1af6e7950f472a081d958eb8519843d38b)` point)`            | Get point hash.
`public int `[`point_is_valid`](#point_8h_1aa3224fcebb1829ab9916069c4473859c)`(`[`point_t`](#primitives_8h_1af6e7950f472a081d958eb8519843d38b)` point)`            | Determine if point is valid.
`public uint32_t `[`point_get_index`](#point_8h_1a3fc9f37c57e85b06b0f5b4c6c16ba212)`(`[`point_t`](#primitives_8h_1af6e7950f472a081d958eb8519843d38b)` point)`            | Get point index.
`public uint64_t `[`point_get_checksum`](#point_8h_1a643229ebf5215c2068cee98d0e15fc7c)`(`[`point_t`](#primitives_8h_1af6e7950f472a081d958eb8519843d38b)` point)`            | Get point checksum.
`public `[`point_t`](#primitives_8h_1af6e7950f472a081d958eb8519843d38b)` `[`point_list_nth`](#point__list_8h_1a81e77050195c59f9d6a618fe8e3f77e1)`(`[`point_list_t`](#primitives_8h_1a58aa9400b0e0aaa34d6b5a1a2666bb29)` point_list,size_t n)`            | Get the list's n-th point.
`public size_t `[`point_list_count`](#point__list_8h_1a235ce31f8d2e130a3cbb998f7cf9f459)`(`[`point_list_t`](#primitives_8h_1a58aa9400b0e0aaa34d6b5a1a2666bb29)` point_list)`            | Get point list count.
`public void `[`point_list_destruct`](#point__list_8h_1a06f5db8b275deb99ba1c3a31e60e86a2)`(`[`point_list_t`](#primitives_8h_1a58aa9400b0e0aaa34d6b5a1a2666bb29)` point_list)`            | Release memory held by point list instance.
`public void `[`script_destruct`](#script_8h_1a594a6462fb996f38aa6f7b6f54b0c9e0)`(`[`script_t`](#primitives_8h_1a14a6f2e8d8ccced8b9bf7844e22e4aef)` script)`            | Release memory held by a script instance.
`public int `[`script_is_valid`](#script_8h_1ac13f89765de02c5e08a39d8f76c1ad2f)`(`[`script_t`](#primitives_8h_1a14a6f2e8d8ccced8b9bf7844e22e4aef)` script)`            | Determine if a script is valid.
`public int `[`script_is_valid_operations`](#script_8h_1afe1d83cba0d1d005d285882eeacc06a3)`(`[`script_t`](#primitives_8h_1a14a6f2e8d8ccced8b9bf7844e22e4aef)` script)`            | Determine if the script operations are valid.
`public size_t `[`script_satoshi_content_size`](#script_8h_1a022d8a549bdde964bc1c00a77d50f2d0)`(`[`script_t`](#primitives_8h_1a14a6f2e8d8ccced8b9bf7844e22e4aef)` script)`            | Get the script Satoshi content size.
`public size_t `[`script_serialized_size`](#script_8h_1ac7d8b5cbb37e481721fd5dffd58fbc4d)`(`[`script_t`](#primitives_8h_1a14a6f2e8d8ccced8b9bf7844e22e4aef)` script,bool prefix)`            | Get script serialized size.
`public char const  * `[`script_to_string`](#script_8h_1a16eafae91b17dc195dee2fc03b9219f4)`(`[`script_t`](#primitives_8h_1a14a6f2e8d8ccced8b9bf7844e22e4aef)` script,uint32_t active_forks)`            | Get script string representation.
`public size_t `[`script_sigops`](#script_8h_1ab8814aa7853426f6ed6b3de848a27c83)`(`[`script_t`](#primitives_8h_1a14a6f2e8d8ccced8b9bf7844e22e4aef)` script,bool embedded)`            | Get script signature operations (sigops) count.
`public size_t `[`script_embedded_sigops`](#script_8h_1a490c2ea9b3c053eb1048a3a90b8eefea)`(`[`script_t`](#primitives_8h_1a14a6f2e8d8ccced8b9bf7844e22e4aef)` script,`[`script_t`](#primitives_8h_1a14a6f2e8d8ccced8b9bf7844e22e4aef)` prevout_script)`            | Get script embedded signature operations (sigops) count.
`public void `[`transaction_destruct`](#transaction_8h_1ad32fc27899d84318a183ecf152967570)`(`[`transaction_t`](#primitives_8h_1a5618f23f10ca9f9ad96cf52f4059e995)` transaction)`            | Release memory held by transaction instance.
`public int `[`transaction_is_valid`](#transaction_8h_1ad25670d899126e24ab1d156ac967a4df)`(`[`transaction_t`](#primitives_8h_1a5618f23f10ca9f9ad96cf52f4059e995)` transaction)`            | Determine if a transaction is valid.
`public uint32_t `[`transaction_version`](#transaction_8h_1ac2ab82b5e4ce6a7fbe0b253274849c34)`(`[`transaction_t`](#primitives_8h_1a5618f23f10ca9f9ad96cf52f4059e995)` transaction)`            | Get transaction version.
`public void `[`transaction_set_version`](#transaction_8h_1a3a5951371c882dc42d49e1a87ccb7401)`(`[`transaction_t`](#primitives_8h_1a5618f23f10ca9f9ad96cf52f4059e995)` transaction,uint32_t version)`            | Set transaction version.
`public `[`hash_t`](#primitives_8h_1aa0ccd30c9c9fb169daec5f65600e7c71)` `[`transaction_hash`](#transaction_8h_1a0e6db5b986bbc034483d319f1221b37c)`(`[`transaction_t`](#primitives_8h_1a5618f23f10ca9f9ad96cf52f4059e995)` transaction)`            | Get transaction hash.
`public `[`hash_t`](#primitives_8h_1aa0ccd30c9c9fb169daec5f65600e7c71)` `[`transaction_hash_sighash_type`](#transaction_8h_1a922f312aad666746d25921814a6f1272)`(`[`transaction_t`](#primitives_8h_1a5618f23f10ca9f9ad96cf52f4059e995)` transaction,uint32_t sighash_type)`            | Get transaction sighash by type.
`public uint32_t `[`transaction_locktime`](#transaction_8h_1a2c606bb46d54f237d9e19075e8336b4e)`(`[`transaction_t`](#primitives_8h_1a5618f23f10ca9f9ad96cf52f4059e995)` transaction)`            | Get transaction locktime.
`public size_t `[`transaction_serialized_size`](#transaction_8h_1a742cb6b1ef15066f58ea808292888977)`(`[`transaction_t`](#primitives_8h_1a5618f23f10ca9f9ad96cf52f4059e995)` transaction,int wire)`            | Get transaction serialized size.
`public uint64_t `[`transaction_fees`](#transaction_8h_1a18e73484e57bb57571c2496f2fb361da)`(`[`transaction_t`](#primitives_8h_1a5618f23f10ca9f9ad96cf52f4059e995)` transaction)`            | Get transaction fees.
`public size_t `[`transaction_signature_operations`](#transaction_8h_1a2a51456f9e148f42c5dd84e1eca4e119)`(`[`transaction_t`](#primitives_8h_1a5618f23f10ca9f9ad96cf52f4059e995)` transaction)`            | Get transaction signature operations count.
`public size_t `[`transaction_signature_operations_bip16_active`](#transaction_8h_1a56c17116d7235f6ebec6e25ffdcdbc0b)`(`[`transaction_t`](#primitives_8h_1a5618f23f10ca9f9ad96cf52f4059e995)` transaction,int bip16_active)`            | Get transaction BIP0016 signature operations count.
`public uint64_t `[`transaction_total_input_value`](#transaction_8h_1a72a7d67b3a88aea60275c6a4279e3150)`(`[`transaction_t`](#primitives_8h_1a5618f23f10ca9f9ad96cf52f4059e995)` transaction)`            | Get the sum of the transaction input values.
`public uint64_t `[`transaction_total_output_value`](#transaction_8h_1aa3b36997f594a4967808e166173becae)`(`[`transaction_t`](#primitives_8h_1a5618f23f10ca9f9ad96cf52f4059e995)` transaction)`            | Get the sum of the transaction output values.
`public int `[`transaction_is_coinbase`](#transaction_8h_1a7a16bc0444fe445d5e690deb5b26783b)`(`[`transaction_t`](#primitives_8h_1a5618f23f10ca9f9ad96cf52f4059e995)` transaction)`            | Determine if a transaction is coinbase.
`public int `[`transaction_is_null_non_coinbase`](#transaction_8h_1a9133115f7971f603ebe3d579f290a098)`(`[`transaction_t`](#primitives_8h_1a5618f23f10ca9f9ad96cf52f4059e995)` transaction)`            | Determine if a transaction is null and not coinnase.
`public int `[`transaction_is_oversized_coinbase`](#transaction_8h_1a202ed448323427c2bd2bf570da7755f6)`(`[`transaction_t`](#primitives_8h_1a5618f23f10ca9f9ad96cf52f4059e995)` transaction)`            | Determine if a transaction is oversized coinbase.
`public int `[`transaction_is_immature`](#transaction_8h_1af59c2b852425cc6defb83564ac93d930)`(`[`transaction_t`](#primitives_8h_1a5618f23f10ca9f9ad96cf52f4059e995)` transaction,size_t target_height)`            | Determine if a transaction is immature.
`public int `[`transaction_is_overspent`](#transaction_8h_1a9f0a7d2da797716141c12b17ea961409)`(`[`transaction_t`](#primitives_8h_1a5618f23f10ca9f9ad96cf52f4059e995)` transaction)`            | Determine if a transaction is overspent.
`public int `[`transaction_is_double_spend`](#transaction_8h_1abeb082da354f1794b20bde7c59fdeecb)`(`[`transaction_t`](#primitives_8h_1a5618f23f10ca9f9ad96cf52f4059e995)` transaction,int include_unconfirmed)`            | Determine if a transaction is double spent.
`public int `[`transaction_is_missing_previous_outputs`](#transaction_8h_1a6aa8bd4e08e142f6a14a4ab702dc8f69)`(`[`transaction_t`](#primitives_8h_1a5618f23f10ca9f9ad96cf52f4059e995)` transaction)`            | Determine whether transaction is missing previous outputs.
`public int `[`transaction_is_final`](#transaction_8h_1a516abef95a61b04e9275caaac85a1632)`(`[`transaction_t`](#primitives_8h_1a5618f23f10ca9f9ad96cf52f4059e995)` transaction,size_t block_height,uint32_t block_time)`            | Determine if a transaction is final.
`public int `[`transaction_is_locktime_conflict`](#transaction_8h_1a4e24096bfbadeea91e45715186137e7f)`(`[`transaction_t`](#primitives_8h_1a5618f23f10ca9f9ad96cf52f4059e995)` transaction)`            | Determine if a transaction incurs in a locktime conflict.
`public size_t `[`transaction_output_count`](#transaction_8h_1a44ce3dcf50895f79b005c4ffd2820358)`(`[`transaction_t`](#primitives_8h_1a5618f23f10ca9f9ad96cf52f4059e995)` transaction)`            | Get transaction output count.
`public `[`output_t`](#primitives_8h_1a6db821b2b1332e8be7a662d075ede0b0)` `[`transaction_output_nth`](#transaction_8h_1ab85fba65372d0078afedcc839ed50d46)`(`[`transaction_t`](#primitives_8h_1a5618f23f10ca9f9ad96cf52f4059e995)` transaction,size_t n)`            | Get the transaction's n-th output.
`public size_t `[`transaction_input_count`](#transaction_8h_1ae6ce6c6592b7a4666592f23050bf51c9)`(`[`transaction_t`](#primitives_8h_1a5618f23f10ca9f9ad96cf52f4059e995)` transaction)`            | Get transaction input count.
`public `[`input_t`](#primitives_8h_1acb1903f2f2f7ed4502a5f53615cff8aa)` `[`transaction_input_nth`](#transaction_8h_1a58617f586abf033ed1cdaf77e087d538)`(`[`transaction_t`](#primitives_8h_1a5618f23f10ca9f9ad96cf52f4059e995)` transaction,size_t n)`            | Get n-th transaction input.
`public `[`word_list_t`](#primitives_8h_1a547ee5b6df76cdddedd5e12dea357036)` `[`word_list_construct`](#word__list_8h_1ac30529cbf0ce5a79d53add1f61c0c90d)`()`            | Create a new word list instance.
`public void `[`word_list_add_word`](#word__list_8h_1af359d913e1eb715be21608dbb90ee558)`(`[`word_list_t`](#primitives_8h_1a547ee5b6df76cdddedd5e12dea357036)` word_list,const char * word)`            | Add a word to the word list 
`public void `[`word_list_destruct`](#word__list_8h_1a47d1b62e1dc307bac37279d213920436)`(`[`word_list_t`](#primitives_8h_1a547ee5b6df76cdddedd5e12dea357036)` word_list)`            | Release memory held by word list object.

## Members

#### `enum `[`point_kind`](#primitives_8h_1a4de8699f33816d833b0d9a69fb08fc8a) {#primitives_8h_1a4de8699f33816d833b0d9a69fb08fc8a}

0 = output, 1 = spend

 Values                         | Descriptions                                
--------------------------------|---------------------------------------------
output            | 
spend            | 

#### `public void `[`block_destruct`](#block_8h_1ac0c31d7ecb4f682fac067a179cc468d1)`(`[`block_t`](#primitives_8h_1a8ed39cb12068667c597f544ec838ccc4)` block)` {#block_8h_1ac0c31d7ecb4f682fac067a179cc468d1}

Release the memory held by a block object.

#### Parameters
* `block` Handle to a block instance

#### `public int `[`block_is_valid`](#block_8h_1af7395388b4f83298636e05de96b8bb7f)`(`[`block_t`](#primitives_8h_1a8ed39cb12068667c597f544ec838ccc4)` block)` {#block_8h_1af7395388b4f83298636e05de96b8bb7f}

Determine if a block is valid.

#### Parameters
* `block` Handle to a block instance 

#### Returns
True (non zero) iif the block is valid

#### `public `[`header_t`](#primitives_8h_1ae6323fbfdc3ff99f33acbae250895ab8)` `[`block_header`](#block_8h_1aa644a0753e3d370f683883aecc37a199)`(`[`block_t`](#primitives_8h_1a8ed39cb12068667c597f544ec838ccc4)` block)` {#block_8h_1aa644a0753e3d370f683883aecc37a199}

Get the block's header.

#### Parameters
* `block` Handle to a block instance 

#### Returns
Handle to the block's header. Must be released by calling [header_destruct()](#header_8h_1a1d1d3fc9341337e1bddd2681fdfed682)

#### `public `[`hash_t`](#primitives_8h_1aa0ccd30c9c9fb169daec5f65600e7c71)` `[`block_hash`](#block_8h_1a30cfad237bdb5bebe5fd7e3b48f3d410)`(`[`block_t`](#primitives_8h_1a8ed39cb12068667c597f544ec838ccc4)` block)` {#block_8h_1a30cfad237bdb5bebe5fd7e3b48f3d410}

Get the block's hash.

#### Parameters
* `block` Handle to a block instance 

#### Returns
Block hash as a byte array. Must be released by calling delete[]

#### `public size_t `[`block_transaction_count`](#block_8h_1a7efc8cd7a41f4dfe6286629ab9ebe59b)`(`[`block_t`](#primitives_8h_1a8ed39cb12068667c597f544ec838ccc4)` block)` {#block_8h_1a7efc8cd7a41f4dfe6286629ab9ebe59b}

Get the block's transaction count.

#### Parameters
* `block` Handle to a block instance 

#### Returns
The amount of transactions that comprise the block

#### `public `[`transaction_t`](#primitives_8h_1a5618f23f10ca9f9ad96cf52f4059e995)` `[`block_transaction_nth`](#block_8h_1a0732e73992d9c4c4789fc54f39e8747a)`(`[`block_t`](#primitives_8h_1a8ed39cb12068667c597f544ec838ccc4)` block,size_t n)` {#block_8h_1a0732e73992d9c4c4789fc54f39e8747a}

Get the block's n-th transaction.

#### Parameters
* `block` Handle to a block instance 

* `n` Index to the desired transaction. Starts at zero (0) for the first one 

#### Returns
Handle to the selected transaction. Must be released by calling [transaction_destruct()](#transaction_8h_1ad32fc27899d84318a183ecf152967570)

#### `public size_t `[`block_serialized_size`](#block_8h_1a5b8666350465a4501cb3e8002085a2b1)`(`[`block_t`](#primitives_8h_1a8ed39cb12068667c597f544ec838ccc4)` block,uint32_t version)` {#block_8h_1a5b8666350465a4501cb3e8002085a2b1}

Get the block's serialized size.

#### Parameters
* `block` Handle to a block instance 

* `version` The protocol version as a 32-bit integer 

#### Returns
The block's serialized size

#### `public uint64_t `[`block_subsidy`](#block_8h_1a6c9f4dca5ff1fc402d405e4216a82d86)`(size_t height)` {#block_8h_1a6c9f4dca5ff1fc402d405e4216a82d86}

Get the block subsidy (miner_reward = block_subsidy + transaction_fees)

#### Parameters
* `height` The block's height 

#### Returns
The block's subsidy

#### `public uint64_t `[`block_fees`](#block_8h_1a0ee8cfa6d663b50aff057932efb0eeaa)`(`[`block_t`](#primitives_8h_1a8ed39cb12068667c597f544ec838ccc4)` block)` {#block_8h_1a0ee8cfa6d663b50aff057932efb0eeaa}

Get the block's total transaction fees (miner_reward = block_subsidy + transaction_fees)

#### Parameters
* `block` Handle to a block instance 

#### Returns
The block's total transaction fees

#### `public uint64_t `[`block_claim`](#block_8h_1a4a1d431723d6e90f80894bb6b6a9c213)`(`[`block_t`](#primitives_8h_1a8ed39cb12068667c597f544ec838ccc4)` block)` {#block_8h_1a4a1d431723d6e90f80894bb6b6a9c213}

Get the block's claim.

#### Parameters
* `block` Handle to a block instance 

#### Returns
The block's claim

#### `public uint64_t `[`block_reward`](#block_8h_1af91de8cf3d009d9bb291f3fdac1c35dd)`(`[`block_t`](#primitives_8h_1a8ed39cb12068667c597f544ec838ccc4)` block,size_t height)` {#block_8h_1af91de8cf3d009d9bb291f3fdac1c35dd}

Get the block's miner reward (miner_reward = block_subsidy + transaction_fees)

#### Parameters
* `block` Handle to a block instance 

* `height` The block's height 

#### Returns
The block's miner reward

#### `public `[`hash_t`](#primitives_8h_1aa0ccd30c9c9fb169daec5f65600e7c71)` `[`block_generate_merkle_root`](#block_8h_1accd9987fa1b37396e047f6e8b2251c12)`(`[`block_t`](#primitives_8h_1a8ed39cb12068667c597f544ec838ccc4)` block)` {#block_8h_1accd9987fa1b37396e047f6e8b2251c12}

Generate a Merkle root for a block.

#### Parameters
* `block` Handle to a block instance 

#### Returns
The new Merkle root's hash. Must be released by calling delete[]

#### `public size_t `[`block_signature_operations`](#block_8h_1a0095ecbd424497725258918fc0c07acc)`(`[`block_t`](#primitives_8h_1a8ed39cb12068667c597f544ec838ccc4)` block)` {#block_8h_1a0095ecbd424497725258918fc0c07acc}

Get the block's signature operations count.

#### Parameters
* `block` Handle to a block instance 

#### Returns
Amount of block signature operations

#### `public size_t `[`block_signature_operations_bip16_active`](#block_8h_1adbc5bcd535157b8fca7e9869db80d68d)`(`[`block_t`](#primitives_8h_1a8ed39cb12068667c597f544ec838ccc4)` block,int bip16_active)` {#block_8h_1adbc5bcd535157b8fca7e9869db80d68d}

Get the block's BIP0016 signature operations count.

#### Parameters
* `block` Handle to a block instance 

* `bip16_active` If true (non zero), don't consider inactive operations for the total count 

#### Returns
Amount of BIP0016 block signature operations

#### `public size_t `[`block_total_inputs`](#block_8h_1aded82b46e51e35812902beec2e60c508)`(`[`block_t`](#primitives_8h_1a8ed39cb12068667c597f544ec838ccc4)` block,int with_coinbase)` {#block_8h_1aded82b46e51e35812902beec2e60c508}

Get the block's input count.

#### Parameters
* `block` Handle to a block instance 

* `with_coinbase` If true (non zero), count coinbase inputs 

#### Returns
Amount of inputs owned by the transaction

#### `public int `[`block_is_extra_coinbases`](#block_8h_1acda164be7d985af0e920396fd5dbf438)`(`[`block_t`](#primitives_8h_1a8ed39cb12068667c597f544ec838ccc4)` block)` {#block_8h_1acda164be7d985af0e920396fd5dbf438}

Determine if a block has extra coinbases.

#### Parameters
* `block` Handle to a block instance 

#### Returns
True (non zero) iif the block has extra coinbases

#### `public int `[`block_is_final`](#block_8h_1aa3b0657e9a9141472d62e61b6ff7800a)`(`[`block_t`](#primitives_8h_1a8ed39cb12068667c597f544ec838ccc4)` block,size_t height)` {#block_8h_1aa3b0657e9a9141472d62e61b6ff7800a}

Determine if a block is final.

#### Parameters
* `block` Handle to a block instance 

* `height` Block height 

#### Returns
True (non zero) iif the block is final

#### `public int `[`block_is_distinct_transaction_set`](#block_8h_1a2a7648c49fb07ad150013289522e9a62)`(`[`block_t`](#primitives_8h_1a8ed39cb12068667c597f544ec838ccc4)` block)` {#block_8h_1a2a7648c49fb07ad150013289522e9a62}

Determine if a block contains a distinct transaction set.

#### Parameters
* `block` Handle to a block instance 

#### Returns
True (non zero) iif the block contains a distinct transaction set

#### `public int `[`block_is_valid_coinbase_claim`](#block_8h_1a18fb299820f406654184facc727f6359)`(`[`block_t`](#primitives_8h_1a8ed39cb12068667c597f544ec838ccc4)` block,size_t height)` {#block_8h_1a18fb299820f406654184facc727f6359}

Determine if a block contains a valid coinbase claim.

#### Parameters
* `block` Handle to a block instance 

* `height` Block height 

#### Returns
True (non zero) iif the block contains a valid coinbase claim

#### `public int `[`block_is_valid_coinbase_script`](#block_8h_1aa8e9758dd0e41b4ebcf0daef7cb50af2)`(`[`block_t`](#primitives_8h_1a8ed39cb12068667c597f544ec838ccc4)` block,size_t height)` {#block_8h_1aa8e9758dd0e41b4ebcf0daef7cb50af2}

Determine if a block contains a valid coinbase script.

#### Parameters
* `block` Handle to a block instance 

* `height` Block height 

#### Returns
True (non zero) iif the block contains a valid coinbase script

#### `public int `[`block_is_internal_double_spend`](#block_8h_1a7c4a0d1bd346fe47a8f0022427b47b9c)`(`[`block_t`](#primitives_8h_1a8ed39cb12068667c597f544ec838ccc4)` block)` {#block_8h_1a7c4a0d1bd346fe47a8f0022427b47b9c}

Determine if a block contains an internal double spend.

#### Parameters
* `block` Handle to a block instance 

#### Returns
True (non zero) iif the block contains an internal double spend

#### `public int `[`block_is_valid_merkle_root`](#block_8h_1ae3e37f3180a5403625db8bdbe6d105ee)`(`[`block_t`](#primitives_8h_1a8ed39cb12068667c597f544ec838ccc4)` block)` {#block_8h_1ae3e37f3180a5403625db8bdbe6d105ee}

Determine if a block has a valid Merkle root.

#### Parameters
* `block` Handle to a block instance 

#### Returns
True (non zero) iif the block has a valid Merkle root

#### `public `[`header_t`](#primitives_8h_1ae6323fbfdc3ff99f33acbae250895ab8)` `[`compact_block_header`](#compact__block_8h_1a8cf34d1187d38c7d6201453289a19d5c)`(`[`compact_block_t`](#primitives_8h_1a43ccacc67cf17b4bf244f421228028ad)` block)` {#compact__block_8h_1a8cf34d1187d38c7d6201453289a19d5c}

Get compact block header.

#### Parameters
* `block` Handle to a compact block instance 

#### Returns
Handle to the compact block's header. Must be released by calling [header_destruct()](#header_8h_1a1d1d3fc9341337e1bddd2681fdfed682)

#### `public int `[`compact_block_is_valid`](#compact__block_8h_1accb0d739d132cbed90dc3495886a05b0)`(`[`compact_block_t`](#primitives_8h_1a43ccacc67cf17b4bf244f421228028ad)` block)` {#compact__block_8h_1accb0d739d132cbed90dc3495886a05b0}

Determine if a compact block is valid.

#### Parameters
* `block` Handle to a compact block instance 

#### Returns
True (non zero) iif the compact block is valid

#### `public size_t `[`compact_block_serialized_size`](#compact__block_8h_1aa96e45a0eb41a7d8bcfe03340d8e502b)`(`[`compact_block_t`](#primitives_8h_1a43ccacc67cf17b4bf244f421228028ad)` block,uint32_t version)` {#compact__block_8h_1aa96e45a0eb41a7d8bcfe03340d8e502b}

Get a compact block's serialized size.

#### Parameters
* `block` Handle to a compact block instance 

* `version` Protocol version 

#### Returns
The compact block's serialized size

#### `public size_t `[`compact_block_transaction_count`](#compact__block_8h_1ae0785b7c6e06c6cb188c94fa0da5b98c)`(`[`compact_block_t`](#primitives_8h_1a43ccacc67cf17b4bf244f421228028ad)` block)` {#compact__block_8h_1ae0785b7c6e06c6cb188c94fa0da5b98c}

Get the compact block's transaction count.

#### Parameters
* `block` Handle to a compact block instance 

#### Returns
Amount of transactions that comprise the compact block

#### `public `[`transaction_t`](#primitives_8h_1a5618f23f10ca9f9ad96cf52f4059e995)` `[`compact_block_transaction_nth`](#compact__block_8h_1ad271eeb9ab8a4148a4065e380cb8213b)`(`[`compact_block_t`](#primitives_8h_1a43ccacc67cf17b4bf244f421228028ad)` block,size_t n)` {#compact__block_8h_1ad271eeb9ab8a4148a4065e380cb8213b}

Get a compact block's n-th transaction.

#### Parameters
* `block` Handle to a compact block instance 

* `n` Index to the transaction inside the block. Starts at 0 (zero) for the first one 

#### Returns
Handle to the n-th transaction. Must be released by calling [transaction_destruct()](#transaction_8h_1ad32fc27899d84318a183ecf152967570)

#### `public uint64_t `[`compact_block_nonce`](#compact__block_8h_1aebea00334de2af9b07f9e6a9acd333d7)`(`[`compact_block_t`](#primitives_8h_1a43ccacc67cf17b4bf244f421228028ad)` block)` {#compact__block_8h_1aebea00334de2af9b07f9e6a9acd333d7}

Get compact block's nonce.

#### Parameters
* `block` Handle to a compact block instance 

#### Returns
Compact block's nonce

#### `public void `[`compact_block_destruct`](#compact__block_8h_1ace80b5f64b9e64e7c53c65d98a3cae4c)`(`[`compact_block_t`](#primitives_8h_1a43ccacc67cf17b4bf244f421228028ad)` block)` {#compact__block_8h_1ace80b5f64b9e64e7c53c65d98a3cae4c}

Release memory held by compact block instance.

#### Parameters
* `block` Handle to a compact block instance

#### `public void `[`compact_block_reset`](#compact__block_8h_1a24b85a581e03ba42eafbe80f276bf01a)`(`[`compact_block_t`](#primitives_8h_1a43ccacc67cf17b4bf244f421228028ad)` block)` {#compact__block_8h_1a24b85a581e03ba42eafbe80f276bf01a}

Reset compact block.

#### Parameters
* `block` Handle to a compact block instance

#### `public `[`executor_t`](#primitives_8h_1a383e6acdb0d5f5df837fc1838b71fc51)` `[`executor_construct`](#executor__c_8h_1aed246db742bdb2aeee6842a8743ea094)`(char const * path,FILE * sout,FILE * serr)` {#executor__c_8h_1aed246db742bdb2aeee6842a8743ea094}

Creates an executor instance, which controls a node in the network.

#### Parameters
* `path` Points to node configuration file 

* `sout` FILE* to where standard output will be redirected 

* `serr` FILE* to which standard error output will be redirected 

#### Returns
A new executor instance. Must be released manually by calling [executor_destruct()](#executor__c_8h_1a963f4bbda682b0bdf66d73a374a1ac89)

#### `public `[`executor_t`](#primitives_8h_1a383e6acdb0d5f5df837fc1838b71fc51)` `[`executor_construct_fd`](#executor__c_8h_1ad9e4e0f23310637271e442585696de0c)`(char const * path,int sout_fd,int serr_fd)` {#executor__c_8h_1ad9e4e0f23310637271e442585696de0c}

Creates an executor instance, which controls a node in the network.

#### Parameters
* `path` Points to node configuration file 

* `sout_fd` File descriptor to where standard output will be redirected 

* `serr_fd` File descriptor to which standard error output will be redirected 

#### Returns
A new executor instance. Must be released manually by calling [executor_destruct()](#executor__c_8h_1a963f4bbda682b0bdf66d73a374a1ac89)

#### `public void `[`executor_destruct`](#executor__c_8h_1a963f4bbda682b0bdf66d73a374a1ac89)`(`[`executor_t`](#primitives_8h_1a383e6acdb0d5f5df837fc1838b71fc51)` exec)` {#executor__c_8h_1a963f4bbda682b0bdf66d73a374a1ac89}

Destroys an executor instance (it only releases memory)

#### Parameters
* `exec` Handle to executor instance

#### `public void `[`executor_run`](#executor__c_8h_1a53815abff7a75a5c963b342f8aa2f8bf)`(`[`executor_t`](#primitives_8h_1a383e6acdb0d5f5df837fc1838b71fc51)` exec,`[`run_handler_t`](#primitives_8h_1a042c0a527cc2744c80e2565a7b7beb9e)` handler)` {#executor__c_8h_1a53815abff7a75a5c963b342f8aa2f8bf}

After [executor_initchain()](#executor__c_8h_1a5edfd9a2012e7345e9908a6d80baeaf6) has been called, the node can be started using this function. This is an asynchronous function, hence the callback parameter.

#### Parameters
* `exec` Handle to executor instance 

* `handler` Callback which will be invoked when the node starts running. It must point to a C function matching the signature defined by run_handler_t 

**See also**: [run_handler_t](#primitives_8h_1a042c0a527cc2744c80e2565a7b7beb9e)

#### `public int `[`executor_run_wait`](#executor__c_8h_1abd814e409c84aac34363c21452cabd58)`(`[`executor_t`](#primitives_8h_1a383e6acdb0d5f5df837fc1838b71fc51)` exec)` {#executor__c_8h_1abd814e409c84aac34363c21452cabd58}

After [executor_initchain()](#executor__c_8h_1a5edfd9a2012e7345e9908a6d80baeaf6) has been called, the node can be started using this function. This is a synchronous function, so it will block until node has started running.

#### Parameters
* `exec` Handle to executor instance 

#### Returns
Error code. Zero for success, non zero for error.

#### `public int `[`executor_initchain`](#executor__c_8h_1a5edfd9a2012e7345e9908a6d80baeaf6)`(`[`executor_t`](#primitives_8h_1a383e6acdb0d5f5df837fc1838b71fc51)` exec)` {#executor__c_8h_1a5edfd9a2012e7345e9908a6d80baeaf6}

Initializes the chain for this node. It only creates the structure; the blockchain won't be synced.

#### Parameters
* `exec` Handle to executor instance 

#### Returns
Error code. Zero for success, non zero for error.

#### `public void `[`executor_stop`](#executor__c_8h_1a80a0e1814db0a389e0ae7ba1a43c78e8)`(`[`executor_t`](#primitives_8h_1a383e6acdb0d5f5df837fc1838b71fc51)` exec)` {#executor__c_8h_1a80a0e1814db0a389e0ae7ba1a43c78e8}

Stops execution of the node.

#### Parameters
* `exec` Handle to executor instance

#### `public void `[`fetch_last_height`](#executor__c_8h_1a83a045615b9be929f3331ef5302ec772)`(`[`executor_t`](#primitives_8h_1a383e6acdb0d5f5df837fc1838b71fc51)` exec,`[`last_height_fetch_handler_t`](#primitives_8h_1a7319bd077428255061dc7c773ebc0cc4)` handler)` {#executor__c_8h_1a83a045615b9be929f3331ef5302ec772}

Get the current blockchain height.

#### Parameters
* `exec` Handle to executor instance 

* `handler` Callback which will be invoked when the blockchain height is retrieved from the network, or retrieval fails. This parameter must point to a C function matching the signature defined by last_height_fetch_handler_t 

**See also**: [last_height_fetch_handler_t](#primitives_8h_1a7319bd077428255061dc7c773ebc0cc4)

#### `public int `[`get_last_height`](#executor__c_8h_1a791b814d3928a00faa6138ea2d33c5b9)`(`[`executor_t`](#primitives_8h_1a383e6acdb0d5f5df837fc1838b71fc51)` exec,size_t * height)` {#executor__c_8h_1a791b814d3928a00faa6138ea2d33c5b9}

Get the current blockchain height. This is the synchronous version of [fetch_last_height()](#executor__c_8h_1a83a045615b9be929f3331ef5302ec772), so it will block until height is retrieved from the network, or an error occurs.

#### Parameters
* `exec` Handle to executor instance 

* `height` Current blockchain height 

#### Returns
Error code. Zero for success, non zero for error

#### `public void `[`fetch_block_height`](#executor__c_8h_1a903aec1424b51b8810273cf5642b70d0)`(`[`executor_t`](#primitives_8h_1a383e6acdb0d5f5df837fc1838b71fc51)` exec,`[`hash_t`](#primitives_8h_1aa0ccd30c9c9fb169daec5f65600e7c71)` hash,`[`block_height_fetch_handler_t`](#primitives_8h_1a7f26119f3693225e3698e80e8d7e64c9)` handler)` {#executor__c_8h_1a903aec1424b51b8810273cf5642b70d0}

Given a block, get its height in the blockchain.

#### Parameters
* `exec` Handle to executor instance 

* `hash` Block hash, which univocally identifies a single block, as an array of bytes 

* `handler` Callback which will be invoked when the block height is retrieved from the network, or retrieval fails. This parameter must point to a C function matching the signature defined by block_height_fetch_handler_t 

**See also**: [block_height_fetch_handler_t](#primitives_8h_1a7f26119f3693225e3698e80e8d7e64c9)

#### `public int `[`get_block_height`](#executor__c_8h_1a0c140100f1eefa4dc6707e93568fdcc1)`(`[`executor_t`](#primitives_8h_1a383e6acdb0d5f5df837fc1838b71fc51)` exec,`[`hash_t`](#primitives_8h_1aa0ccd30c9c9fb169daec5f65600e7c71)` hash,size_t * height)` {#executor__c_8h_1a0c140100f1eefa4dc6707e93568fdcc1}

Given a block, get its height in the blockchain. This is the synchronous version of [fetch_block_height()](#executor__c_8h_1a903aec1424b51b8810273cf5642b70d0), so it will block until height is retrieved from the network, or an error occurs.

#### Parameters
* `exec` Handle to executor instance 

* `hash` Block hash, which univocally identifies a single block, as an array of bytes 

* `height` Block height 

#### Returns
Error code. Zero for success, non zero for error

#### `public void `[`fetch_block_header_by_height`](#executor__c_8h_1ae4d491f18285c2b31b6261683ef5679b)`(`[`executor_t`](#primitives_8h_1a383e6acdb0d5f5df837fc1838b71fc51)` exec,size_t height,`[`block_header_fetch_handler_t`](#primitives_8h_1a175320d3fdee884d5b1daba1f51af6cf)` handler)` {#executor__c_8h_1ae4d491f18285c2b31b6261683ef5679b}

Given a height in the blockchain, retrieve its block's header.

#### Parameters
* `exec` Handle to executor instance 

* `height` The height which identifies the desired block 

* `handler` Callback which will be invoked when the block header is retrieved from the network, or retrieval fails. This parameter must point to a C function matching the signature defined by block_header_fetch_handler_t 

**See also**: [block_header_fetch_handler_t](#primitives_8h_1a175320d3fdee884d5b1daba1f51af6cf)

#### `public int `[`get_block_header_by_height`](#executor__c_8h_1a2b2cb61fd05544b98a8829c6fc357a06)`(`[`executor_t`](#primitives_8h_1a383e6acdb0d5f5df837fc1838b71fc51)` exec,size_t height,`[`header_t`](#primitives_8h_1ae6323fbfdc3ff99f33acbae250895ab8)` * header,size_t * ret_height)` {#executor__c_8h_1a2b2cb61fd05544b98a8829c6fc357a06}

Given a height in the blockchain, retrieve its block's header. This is the synchronous version of [fetch_block_header_by_height()](#executor__c_8h_1ae4d491f18285c2b31b6261683ef5679b), so it will block until the header is retrieved from the network, or an error occurs.

#### Parameters
* `exec` Handle to executor instance 

* `height` The height which identifies the desired block 

* `header` The block's header. It must be released by calling [header_destruct()](#header_8h_1a1d1d3fc9341337e1bddd2681fdfed682)

* `ret_height` The block's height 

#### Returns
Error code. Zero for success, non zero for error

#### `public void `[`fetch_block_header_by_hash`](#executor__c_8h_1a660eb713c231f3daa2a1cfb5fbfa4bd4)`(`[`executor_t`](#primitives_8h_1a383e6acdb0d5f5df837fc1838b71fc51)` exec,`[`hash_t`](#primitives_8h_1aa0ccd30c9c9fb169daec5f65600e7c71)` hash,`[`block_header_fetch_handler_t`](#primitives_8h_1a175320d3fdee884d5b1daba1f51af6cf)` handler)` {#executor__c_8h_1a660eb713c231f3daa2a1cfb5fbfa4bd4}

Given a block hash, retrieve its header.

#### Parameters
* `exec` Handle to executor instance 

* `hash` The hash which identifies the desired block 

* `handler` Callback which will be invoked when the block header is retrieved from the network, or retrieval fails. This parameter must point to a C function matching the signature defined by block_header_fetch_handler_t 

**See also**: [block_header_fetch_handler_t](#primitives_8h_1a175320d3fdee884d5b1daba1f51af6cf)

#### `public int `[`get_block_header_by_hash`](#executor__c_8h_1a21e7310364624f505d7e16190fe1fa3c)`(`[`executor_t`](#primitives_8h_1a383e6acdb0d5f5df837fc1838b71fc51)` exec,`[`hash_t`](#primitives_8h_1aa0ccd30c9c9fb169daec5f65600e7c71)` hash,`[`header_t`](#primitives_8h_1ae6323fbfdc3ff99f33acbae250895ab8)` * header,size_t * ret_height)` {#executor__c_8h_1a21e7310364624f505d7e16190fe1fa3c}

Given a block hash, retrieve its header. This is the synchronous version of [fetch_block_header_by_height()](#executor__c_8h_1ae4d491f18285c2b31b6261683ef5679b), so it will block until the header is retrieved from the network, or an error occurs.

#### Parameters
* `exec` Handle to executor instance 

* `hash` The hash which identifies the desired block 

* `header` Block header 

* `ret_height` Block height 

#### Returns
Error code. Zero for success, non zero for error

#### `public void `[`fetch_block_by_height`](#executor__c_8h_1a1ce9ccf736baf9f52e26093e7787f7a3)`(`[`executor_t`](#primitives_8h_1a383e6acdb0d5f5df837fc1838b71fc51)` exec,size_t height,`[`block_fetch_handler_t`](#primitives_8h_1a8c1fb1e052b08b1188d614222a9de9b2)` handler)` {#executor__c_8h_1a1ce9ccf736baf9f52e26093e7787f7a3}

Given a block's height, retrieve the block.

#### Parameters
* `exec` Handle to executor instance 

* `height` The height which identifies the desired block 

* `handler` Callback which will be invoked when the block is retrieved from the network, or retrieval fails. This parameter must point to a C function matching the signature defined by block_fetch_handler_t 

**See also**: [block_fetch_handler_t](#primitives_8h_1a8c1fb1e052b08b1188d614222a9de9b2)

#### `public int `[`get_block_by_height`](#executor__c_8h_1a1887b7fb6d869838e66afd19a09b50d2)`(`[`executor_t`](#primitives_8h_1a383e6acdb0d5f5df837fc1838b71fc51)` exec,size_t height,`[`block_t`](#primitives_8h_1a8ed39cb12068667c597f544ec838ccc4)` * block,size_t * ret_height)` {#executor__c_8h_1a1887b7fb6d869838e66afd19a09b50d2}

Given a block's height, retrieve the block. This is the synchronous version of [fetch_block_by_height()](#executor__c_8h_1a1ce9ccf736baf9f52e26093e7787f7a3), so it will block until the block is retrieved from the network, or an error occurs.

#### Parameters
* `exec` Handle to executor instance 

* `height` The height which identifies the desired block 

* `block` Block 

* `ret_height` Block height 

#### Returns
Error code. Zero for success, non zero for error

#### `public void `[`fetch_block_by_hash`](#executor__c_8h_1a0e2e7826e0ed92f46f06fb7c50d0b5e2)`(`[`executor_t`](#primitives_8h_1a383e6acdb0d5f5df837fc1838b71fc51)` exec,`[`hash_t`](#primitives_8h_1aa0ccd30c9c9fb169daec5f65600e7c71)` hash,`[`block_fetch_handler_t`](#primitives_8h_1a8c1fb1e052b08b1188d614222a9de9b2)` handler)` {#executor__c_8h_1a0e2e7826e0ed92f46f06fb7c50d0b5e2}

Given a block's hash, retrieve the block.

#### Parameters
* `exec` Handle to executor instance 

* `hash` The hash which identifies the desired block 

* `handler` Callback which will be invoked when the block is retrieved from the network, or retrieval fails. This parameter must point to a C function matching the signature defined by block_fetch_handler_t 

**See also**: [block_fetch_handler_t](#primitives_8h_1a8c1fb1e052b08b1188d614222a9de9b2)

#### `public int `[`get_block_by_hash`](#executor__c_8h_1a13e08557af5950a19019e4ff55791d12)`(`[`executor_t`](#primitives_8h_1a383e6acdb0d5f5df837fc1838b71fc51)` exec,`[`hash_t`](#primitives_8h_1aa0ccd30c9c9fb169daec5f65600e7c71)` hash,`[`block_t`](#primitives_8h_1a8ed39cb12068667c597f544ec838ccc4)` * block,size_t * ret_height)` {#executor__c_8h_1a13e08557af5950a19019e4ff55791d12}

Given a block's hash, retrieve the block. This is the synchronous version of [fetch_block_by_height()](#executor__c_8h_1a1ce9ccf736baf9f52e26093e7787f7a3), so it will block until the block is retrieved from the network, or an error occurs.

#### Parameters
* `exec` Handle to executor instance 

* `hash` The hash which identifies the desired block 

* `block` Handle to block. Must be released by calling [block_destruct()](#block_8h_1ac0c31d7ecb4f682fac067a179cc468d1)

* `ret_height` Block height 

#### Returns
Error code. Zero for success, non zero for error

#### `public void `[`fetch_merkle_block_by_height`](#executor__c_8h_1a8133807dfb7628a247f191608976c47b)`(`[`executor_t`](#primitives_8h_1a383e6acdb0d5f5df837fc1838b71fc51)` exec,size_t height,`[`merkle_block_fetch_handler_t`](#primitives_8h_1aff6e1e0990f9e15ea36d9a1ce64890ff)` handler)` {#executor__c_8h_1a8133807dfb7628a247f191608976c47b}

Given a Merkle block's height, retrieve the block.

#### Parameters
* `exec` Handle to executor instance 

* `height` The height which identifies the desired block 

* `handler` Callback which will be invoked when the block is retrieved from the network, or retrieval fails. This parameter must point to a C function matching the signature defined by merkle_block_fetch_handler_t 

**See also**: [merkle_block_fetch_handler_t](#primitives_8h_1aff6e1e0990f9e15ea36d9a1ce64890ff)

#### `public void `[`fetch_merkle_block_by_hash`](#executor__c_8h_1aca145cfaa6db94792255beef98e57b94)`(`[`executor_t`](#primitives_8h_1a383e6acdb0d5f5df837fc1838b71fc51)` exec,`[`hash_t`](#primitives_8h_1aa0ccd30c9c9fb169daec5f65600e7c71)` hash,`[`merkle_block_fetch_handler_t`](#primitives_8h_1aff6e1e0990f9e15ea36d9a1ce64890ff)` handler)` {#executor__c_8h_1aca145cfaa6db94792255beef98e57b94}

Given a Merkle block's hash, retrieve the block.

#### Parameters
* `exec` Handle to executor instance 

* `hash` The hash which identifies the desired block 

* `handler` Callback which will be invoked when the block is retrieved from the network, or retrieval fails. This parameter must point to a C function matching the signature defined by merkle_block_fetch_handler_t 

**See also**: [merkle_block_fetch_handler_t](#primitives_8h_1aff6e1e0990f9e15ea36d9a1ce64890ff)

#### `public void `[`fetch_compact_block_by_height`](#executor__c_8h_1a553b3ba0d2df8d9c3cc0d544f570d976)`(`[`executor_t`](#primitives_8h_1a383e6acdb0d5f5df837fc1838b71fc51)` exec,size_t height,`[`compact_block_fetch_handler_t`](#primitives_8h_1ae4895924faf7b39c24a050618ebf6c51)` handler)` {#executor__c_8h_1a553b3ba0d2df8d9c3cc0d544f570d976}

Given a compact block's height, retrieve the block.

#### Parameters
* `exec` Handle to executor instance 

* `height` The height which identifies the desired block 

* `handler` Callback which will be invoked when the block is retrieved from the network, or retrieval fails. This parameter must point to a C function matching the signature defined by compact_block_fetch_handler_t 

**See also**: [compact_block_fetch_handler_t](#primitives_8h_1ae4895924faf7b39c24a050618ebf6c51)

#### `public void `[`fetch_compact_block_by_hash`](#executor__c_8h_1a7a2060ab5f19214db5431646c98a09b8)`(`[`executor_t`](#primitives_8h_1a383e6acdb0d5f5df837fc1838b71fc51)` exec,`[`hash_t`](#primitives_8h_1aa0ccd30c9c9fb169daec5f65600e7c71)` hash,`[`compact_block_fetch_handler_t`](#primitives_8h_1ae4895924faf7b39c24a050618ebf6c51)` handler)` {#executor__c_8h_1a7a2060ab5f19214db5431646c98a09b8}

Given a compact block's hash, retrieve the block.

#### Parameters
* `exec` Handle to executor instance 

* `hash` The hash which identifies the desired block 

* `handler` Callback which will be invoked when the block is retrieved from the network, or retrieval fails. This parameter must point to a C function matching the signature defined by compact_block_fetch_handler_t 

**See also**: [compact_block_fetch_handler_t](#primitives_8h_1ae4895924faf7b39c24a050618ebf6c51)

#### `public void `[`fetch_transaction`](#executor__c_8h_1a99a0cbcfe63b6381c738d21bd7826b3d)`(`[`executor_t`](#primitives_8h_1a383e6acdb0d5f5df837fc1838b71fc51)` exec,`[`hash_t`](#primitives_8h_1aa0ccd30c9c9fb169daec5f65600e7c71)` hash,int require_confirmed,`[`transaction_fetch_handler_t`](#primitives_8h_1ae0808043043d84636e3a2e3c754b8fd6)` handler)` {#executor__c_8h_1a99a0cbcfe63b6381c738d21bd7826b3d}

Given a transaction hash, retrieve it (optionally requiring it to be confirmed)

#### Parameters
* `exec` Handle to executor instance 

* `hash` The hash which identifies the desired transaction 

* `require_confirmed` If this is set to true (non zero), the transaction will only be fetched if it has already been confirmed 

* `handler` Callback which will be invoked when the transaction is retrieved from the network, or retrieval fails. This parameter must point to a C function matching the signature defined by transaction_fetch_handler_t 

**See also**: [transaction_fetch_handler_t](#primitives_8h_1ae0808043043d84636e3a2e3c754b8fd6)

#### `public int `[`get_transaction`](#executor__c_8h_1a7f74db96f0bd243d3568c771896d3a24)`(`[`executor_t`](#primitives_8h_1a383e6acdb0d5f5df837fc1838b71fc51)` exec,`[`hash_t`](#primitives_8h_1aa0ccd30c9c9fb169daec5f65600e7c71)` hash,int require_confirmed,`[`transaction_t`](#primitives_8h_1a5618f23f10ca9f9ad96cf52f4059e995)` * transaction,size_t * ret_height,size_t * index)` {#executor__c_8h_1a7f74db96f0bd243d3568c771896d3a24}

Given a transaction's hash, retrieve it This is the synchronous version of [fetch_transaction()](#executor__c_8h_1a99a0cbcfe63b6381c738d21bd7826b3d), so it will block until the transaction is retrieved from the network, or an error occurs.

#### Parameters
* `exec` Handle to executor instance 

* `hash` The hash which identifies the desired transaction 

* `require_confirmed` If this is set to true (non zero), the transaction will only be fetched if it has already been confirmed 

* `transaction` Block 

* `ret_height` Block height 

* `index` Transaction index inside the block (zero-based, i.e. the first one is zero) 

#### Returns
Error code. Zero for success, non zero for error

#### `public void `[`fetch_transaction_position`](#executor__c_8h_1a699c29f962fa7c4302ee04b21cf82a9a)`(`[`executor_t`](#primitives_8h_1a383e6acdb0d5f5df837fc1838b71fc51)` exec,`[`hash_t`](#primitives_8h_1aa0ccd30c9c9fb169daec5f65600e7c71)` hash,int require_confirmed,`[`transaction_index_fetch_handler_t`](#primitives_8h_1a83733f3195e3e03a0d9f4cc822b48a3d)` handler)` {#executor__c_8h_1a699c29f962fa7c4302ee04b21cf82a9a}

Given a transaction hash, retrieve its position inside the block (optionally requiring it to be confirmed)

#### Parameters
* `exec` Handle to executor instance 

* `hash` The hash which identifies the desired transaction 

* `require_confirmed` If this is set to true (non zero), the transaction will only be fetched if it has already been confirmed 

* `handler` Callback which will be invoked when the transaction position is retrieved from the network, or retrieval fails. This parameter must point to a C function matching the signature defined by transaction_index_fetch_handler_t 

**See also**: [transaction_index_fetch_handler_t](#primitives_8h_1a83733f3195e3e03a0d9f4cc822b48a3d)

#### `public void `[`fetch_output`](#executor__c_8h_1afcc2cb87a88aabb6a712435cee9abc9a)`(`[`executor_t`](#primitives_8h_1a383e6acdb0d5f5df837fc1838b71fc51)` exec,`[`hash_t`](#primitives_8h_1aa0ccd30c9c9fb169daec5f65600e7c71)` hash,uint32_t index,int require_confirmed,`[`output_fetch_handler_t`](#primitives_8h_1aefbd8dfda0d008880de7c60bcf23dde9)` handler)` {#executor__c_8h_1afcc2cb87a88aabb6a712435cee9abc9a}

Given an output hash, retrieve it (optionally requiring it to be confirmed)

#### Parameters
* `exec` Handle to executor instance 

* `hash` The hash which identifies the output's transaction 

* `index` The index which identifies the output among the transaction's other outputs 

* `require_confirmed` If this is set to true (non zero), the output will only be fetched if it has already been confirmed 

* `handler` Callback which will be invoked when the output is retrieved from the network, or retrieval fails. This parameter must point to a C function matching the signature defined by output_fetch_handler_t 

**See also**: [output_fetch_handler_t](#primitives_8h_1aefbd8dfda0d008880de7c60bcf23dde9)

#### `public int `[`get_output`](#executor__c_8h_1a8d35fe3911046137e8cace26f8a3c938)`(`[`executor_t`](#primitives_8h_1a383e6acdb0d5f5df837fc1838b71fc51)` exec,`[`hash_t`](#primitives_8h_1aa0ccd30c9c9fb169daec5f65600e7c71)` hash,uint32_t index,int require_confirmed,`[`output_t`](#primitives_8h_1a6db821b2b1332e8be7a662d075ede0b0)` * output)` {#executor__c_8h_1a8d35fe3911046137e8cace26f8a3c938}

Given an output's hash, retrieve it This is the synchronous version of [fetch_output()](#executor__c_8h_1afcc2cb87a88aabb6a712435cee9abc9a), so it will block until the output is retrieved from the network, or an error occurs.

#### Parameters
* `exec` Handle to executor instance 

* `hash` The hash which identifies the desired output 

* `index` The index which identifies the output among the transaction's other outputs 

* `require_confirmed` If this is set to true (non zero), the output will only be fetched if it has already been confirmed 

* `output` Handle to output. Must be released by calling [output_destruct()](#output_8h_1a974f0d91520ed93250bcd56e2d921590)

#### Returns
Error code. Zero for success, non zero for error

#### `public void `[`fetch_spend`](#executor__c_8h_1a4966f126f69c313903cbf0f46be79f9d)`(`[`executor_t`](#primitives_8h_1a383e6acdb0d5f5df837fc1838b71fc51)` exec,`[`output_point_t`](#primitives_8h_1ad4d5035e7d5ca4f6a10eafdfdfd2e074)` outpoint,`[`spend_fetch_handler_t`](#primitives_8h_1aae597f1c61dc1dc585f5425375300ce3)` handler)` {#executor__c_8h_1a4966f126f69c313903cbf0f46be79f9d}

Given an output point, retrieve its spend.

#### Parameters
* `exec` Handle to executor instance 

* `outpoint` The output point whose spend we wish to retrieve 

* `handler` Callback which will be invoked when the spend is retrieved from the network, or retrieval fails. This parameter must point to a C function matching the signature defined by spend_fetch_handler_t 

**See also**: [spend_fetch_handler_t](#primitives_8h_1aae597f1c61dc1dc585f5425375300ce3)

#### `public void `[`fetch_history`](#executor__c_8h_1a6ca41df13a8c7d67781d3a6005841ba6)`(`[`executor_t`](#primitives_8h_1a383e6acdb0d5f5df837fc1838b71fc51)` exec,`[`payment_address_t`](#primitives_8h_1acc9e0ae61a6bf90f01911484e4ede07b)` address,size_t limit,size_t from_height,`[`history_fetch_handler_t`](#primitives_8h_1aee0367afd480cf2771d49690c567c25a)` handler)` {#executor__c_8h_1a6ca41df13a8c7d67781d3a6005841ba6}

Given a payment address, a starting height and an entry limit, retrieve its transaction history.

#### Parameters
* `exec` Handle to executor instance 

* `address` Payment address whose history we want to fetch 

* `limit` Maximum entries to fetch 

* `from_height` Starting blockchain height for the history 

* `handler` Callback which will be invoked when the history is retrieved from the network, or retrieval fails. This parameter must point to a C function matching the signature defined by history_fetch_handler_t 

**See also**: [history_fetch_handler_t](#primitives_8h_1aee0367afd480cf2771d49690c567c25a)

#### `public int `[`get_history`](#executor__c_8h_1a1760fe0ef7ec0479230bf77ca7a2ea21)`(`[`executor_t`](#primitives_8h_1a383e6acdb0d5f5df837fc1838b71fc51)` exec,`[`payment_address_t`](#primitives_8h_1acc9e0ae61a6bf90f01911484e4ede07b)` address,size_t limit,size_t from_height,`[`history_compact_list_t`](#primitives_8h_1aa9b635e04d3d0e124549cbef8b147638)` * out_history)` {#executor__c_8h_1a1760fe0ef7ec0479230bf77ca7a2ea21}

Given a payment address, a starting height and an entry limit, retrieve its transaction history This is the synchronous version of [fetch_history()](#executor__c_8h_1a6ca41df13a8c7d67781d3a6005841ba6), so it will block until the history is retrieved from the network, or an error occurs.

#### Parameters
* `exec` Handle to executor instance 

* `address` Payment address whose history we want to fetch 

* `limit` Maximum entries to fetch 

* `from_height` Starting blockchain height for the history 

* `out_history` Handle to history. Must be released by calling [history_compact_list_destruct()](#history__compact__list_8h_1aec9ce8654f6d88baf7deab18764e9b52)

#### Returns
Error code. Zero for success, non zero for error

#### `public `[`transaction_t`](#primitives_8h_1a5618f23f10ca9f9ad96cf52f4059e995)` `[`hex_to_tx`](#executor__c_8h_1a8af262d3a75ff3da484cbbccac8a987a)`(char const * tx_hex)` {#executor__c_8h_1a8af262d3a75ff3da484cbbccac8a987a}

Converts a raw transaction hex string to a transaction object.

#### Parameters
* `tx_hex` Raw transaction hex string 

#### Returns
Handle to new transaction object built from the hex string. Must be released by calling [transaction_destruct()](#transaction_8h_1ad32fc27899d84318a183ecf152967570)

#### `public void `[`validate_tx`](#executor__c_8h_1a26fae1c08f21b9f8097e944ebc8ebcc4)`(`[`executor_t`](#primitives_8h_1a383e6acdb0d5f5df837fc1838b71fc51)` exec,`[`transaction_t`](#primitives_8h_1a5618f23f10ca9f9ad96cf52f4059e995)` tx,`[`validate_tx_handler_t`](#primitives_8h_1a4a5ad506c3c92b9308072dcc1815ec17)` handler)` {#executor__c_8h_1a26fae1c08f21b9f8097e944ebc8ebcc4}

Validates a new transaction (has not been added to the blockchain yet)

#### Parameters
* `exec` Handle to executor instance 

* `tx` Transaction to validate 

* `handler` Callback which will be invoked when the history is retrieved from the network, or retrieval fails. This parameter must point to a C function matching the signature defined by validate_tx_handler_t 

**See also**: [validate_tx_handler_t](#primitives_8h_1a4a5ad506c3c92b9308072dcc1815ec17)

#### `public `[`long_hash_t`](#primitives_8h_1a15a7913e47813e6707bf348da7203f1a)` `[`wallet_mnemonics_to_seed`](#executor__c_8h_1abfdab2c4350be9e094478db62f440547)`(`[`word_list_t`](#primitives_8h_1a547ee5b6df76cdddedd5e12dea357036)` mnemonics)` {#executor__c_8h_1abfdab2c4350be9e094478db62f440547}

Convert a set of keywords/mnemonics to an HD wallet seed.

#### Parameters
* `mnemonics` List of keywords/mnemonics 

#### Returns
Handle to long_hash object containing the seed. Must be released by calling [long_hash_destroy()](#executor__c_8h_1a636893dd40262d359bde53923e0a5d1c)

#### `public void `[`long_hash_destroy`](#executor__c_8h_1a636893dd40262d359bde53923e0a5d1c)`(`[`long_hash_t`](#primitives_8h_1a15a7913e47813e6707bf348da7203f1a)` ptr)` {#executor__c_8h_1a636893dd40262d359bde53923e0a5d1c}

Release the memory held by a long hash object.

#### Parameters
* `ptr` Handle to long hash object

#### `public void `[`header_destruct`](#header_8h_1a1d1d3fc9341337e1bddd2681fdfed682)`(`[`header_t`](#primitives_8h_1ae6323fbfdc3ff99f33acbae250895ab8)` header)` {#header_8h_1a1d1d3fc9341337e1bddd2681fdfed682}

Releases memory held by the header object.

#### Parameters
* `header` Handle to the header instance

#### `public int `[`header_is_valid`](#header_8h_1adaabb8aadd2c899fc4c7361532b1fd8e)`(`[`header_t`](#primitives_8h_1ae6323fbfdc3ff99f33acbae250895ab8)` header)` {#header_8h_1adaabb8aadd2c899fc4c7361532b1fd8e}

Determine if the header is valid.

#### Parameters
* `header` Handle to a header instance 

#### Returns
True (non zero) iif the header is valid

#### `public uint32_t `[`header_version`](#header_8h_1a59dc1762a22e8a9ee84c66e20660767b)`(`[`header_t`](#primitives_8h_1ae6323fbfdc3ff99f33acbae250895ab8)` header)` {#header_8h_1a59dc1762a22e8a9ee84c66e20660767b}

Get header version.

#### Parameters
* `header` Handle to a header instance 

#### Returns
Header version

#### `public void `[`header_set_version`](#header_8h_1af95ba2aea724401b648863129ab40a02)`(`[`header_t`](#primitives_8h_1ae6323fbfdc3ff99f33acbae250895ab8)` header,uint32_t version)` {#header_8h_1af95ba2aea724401b648863129ab40a02}

Set a header's version.

#### Parameters
* `header` Handle to a header instance 

* `version` New version value

#### `public uint32_t `[`header_timestamp`](#header_8h_1aa72c883fde1a10067725e0772c6e687f)`(`[`header_t`](#primitives_8h_1ae6323fbfdc3ff99f33acbae250895ab8)` header)` {#header_8h_1aa72c883fde1a10067725e0772c6e687f}

Get header timestamp.

#### Parameters
* `header` Handle to a header instance 

#### Returns
Header timestamp

#### `public void `[`header_set_timestamp`](#header_8h_1a29d0a46719548d37c95fc4e1a456353a)`(`[`header_t`](#primitives_8h_1ae6323fbfdc3ff99f33acbae250895ab8)` header,uint32_t timestamp)` {#header_8h_1a29d0a46719548d37c95fc4e1a456353a}

Set header timestamp.

#### Parameters
* `header` Handle to a header instance 

* `timestamp` New header timestamp value

#### `public uint32_t `[`header_bits`](#header_8h_1a6a505d7f8f1137fe68b6b096ed35a15a)`(`[`header_t`](#primitives_8h_1ae6323fbfdc3ff99f33acbae250895ab8)` header)` {#header_8h_1a6a505d7f8f1137fe68b6b096ed35a15a}

Get header bits.

#### Parameters
* `header` Handle to a header instance 

#### Returns
Header bits

#### `public void `[`header_set_bits`](#header_8h_1ad9acf477b496b3d6d632b70483dfad81)`(`[`header_t`](#primitives_8h_1ae6323fbfdc3ff99f33acbae250895ab8)` header,uint32_t bits)` {#header_8h_1ad9acf477b496b3d6d632b70483dfad81}

Set header bits.

#### Parameters
* `header` Handle to a header instance 

* `bits` New header bits value

#### `public uint32_t `[`header_nonce`](#header_8h_1acb3466f0d21884c5ba4c272571440610)`(`[`header_t`](#primitives_8h_1ae6323fbfdc3ff99f33acbae250895ab8)` header)` {#header_8h_1acb3466f0d21884c5ba4c272571440610}

Get header nonce.

#### Parameters
* `header` Handle to a header instance 

#### Returns
Header nonce

#### `public void `[`header_set_nonce`](#header_8h_1ab4dd1bb2ed0a537cf237e7dc82184d0c)`(`[`header_t`](#primitives_8h_1ae6323fbfdc3ff99f33acbae250895ab8)` header,uint32_t nonce)` {#header_8h_1ab4dd1bb2ed0a537cf237e7dc82184d0c}

Set header nonce 
#### Parameters
* `header` Handle to a header instance 

* `nonce` New header nonce value

#### `public `[`hash_t`](#primitives_8h_1aa0ccd30c9c9fb169daec5f65600e7c71)` `[`header_previous_block_hash`](#header_8h_1ac048f31bf04639f83e5be544adf9b977)`(`[`header_t`](#primitives_8h_1ae6323fbfdc3ff99f33acbae250895ab8)` header)` {#header_8h_1ac048f31bf04639f83e5be544adf9b977}

Get previous block hash.

#### Parameters
* `header` Handle to a header instance

#### `public `[`hash_t`](#primitives_8h_1aa0ccd30c9c9fb169daec5f65600e7c71)` `[`header_merkle`](#header_8h_1af0f199ca6fed2c5cc37fedfe5dd86b47)`(`[`header_t`](#primitives_8h_1ae6323fbfdc3ff99f33acbae250895ab8)` header)` {#header_8h_1af0f199ca6fed2c5cc37fedfe5dd86b47}

Get header Merkle.

#### Parameters
* `header` Handle to a header instance 

#### Returns
Header Merkle hash. Must be released by calling delete[]

#### `public `[`hash_t`](#primitives_8h_1aa0ccd30c9c9fb169daec5f65600e7c71)` `[`header_hash`](#header_8h_1a625887dacbb1b408e292e0ff6a5638fc)`(`[`header_t`](#primitives_8h_1ae6323fbfdc3ff99f33acbae250895ab8)` header)` {#header_8h_1a625887dacbb1b408e292e0ff6a5638fc}

Get header hash.

#### Parameters
* `header` Handle to a header instance 

#### Returns
Header hash as byte array. Must be released by calling delete[]

#### `public `[`point_kind_t`](#primitives_8h_1a6f08d747fe788aa53ad4e70e58230078)` `[`history_compact_get_point_kind`](#history__compact_8h_1ad821d566985946fe24bc56f95d3a89c2)`(`[`history_compact_t`](#primitives_8h_1afecbcaff5ab6fec4cda05ca77abb093d)` history)` {#history__compact_8h_1ad821d566985946fe24bc56f95d3a89c2}

Get the entry's point kind.

#### Parameters
* `history` Handle to a history entry instance 

#### Returns
Entry's point kind

#### `public `[`point_t`](#primitives_8h_1af6e7950f472a081d958eb8519843d38b)` `[`history_compact_get_point`](#history__compact_8h_1a86510b343ae158fb7ceefbdbdb92a304)`(`[`history_compact_t`](#primitives_8h_1afecbcaff5ab6fec4cda05ca77abb093d)` history)` {#history__compact_8h_1a86510b343ae158fb7ceefbdbdb92a304}

Get the entry's point.

#### Parameters
* `history` Handle to a history entry instance 

#### Returns
Entry's point

#### `public uint32_t `[`history_compact_get_height`](#history__compact_8h_1abbe2e7a92e48a0a32b261bcdfd723f07)`(`[`history_compact_t`](#primitives_8h_1afecbcaff5ab6fec4cda05ca77abb093d)` history)` {#history__compact_8h_1abbe2e7a92e48a0a32b261bcdfd723f07}

Get the height of history entry in the blockchain.

#### Parameters
* `history` Handle to a history entry instance 

#### Returns
Entry height in the blockchain

#### `public uint64_t `[`history_compact_get_value_or_previous_checksum`](#history__compact_8h_1a3421ce4d489fbda735d8de833bd1e090)`(`[`history_compact_t`](#primitives_8h_1afecbcaff5ab6fec4cda05ca77abb093d)` history)` {#history__compact_8h_1a3421ce4d489fbda735d8de833bd1e090}

Get the entry's value.

#### Parameters
* `history` Handle to a history entry instance 

#### Returns
Entry value, which can be a Satoshi value if point kind is output, or the previous entry's checksum if point kind is spend

#### `public void `[`history_compact_list_destruct`](#history__compact__list_8h_1aec9ce8654f6d88baf7deab18764e9b52)`(`[`history_compact_list_t`](#primitives_8h_1aa9b635e04d3d0e124549cbef8b147638)` history_compact_list)` {#history__compact__list_8h_1aec9ce8654f6d88baf7deab18764e9b52}

Release memory held by a history compact list instance.

#### Parameters
* `history_compact_list` Handle to a history compact list instance

#### `public size_t `[`history_compact_list_count`](#history__compact__list_8h_1a9e3ccd8686469993bb94a73ceb3bac65)`(`[`history_compact_list_t`](#primitives_8h_1aa9b635e04d3d0e124549cbef8b147638)` history_compact_list)` {#history__compact__list_8h_1a9e3ccd8686469993bb94a73ceb3bac65}

Get the amount of entries in the list.

#### Parameters
* `history_compact_list` Handle to a history compact list instance 

#### Returns
Entry count

#### `public `[`history_compact_t`](#primitives_8h_1afecbcaff5ab6fec4cda05ca77abb093d)` `[`history_compact_list_nth`](#history__compact__list_8h_1ad202250e8072936b89cb9381034c05a7)`(`[`history_compact_list_t`](#primitives_8h_1aa9b635e04d3d0e124549cbef8b147638)` history_list,size_t n)` {#history__compact__list_8h_1ad202250e8072936b89cb9381034c05a7}

Get the list's n-th entry.

#### Parameters
* `history_list` Handle to a history compact list instance 

* `n` Index for selecting an entry. Starts at 0 (zero) for the first one 

#### Returns
Handle to a history compact entry. Must be released by calling history_compact_destruct()

#### `public void `[`input_destruct`](#input_8h_1a07e22ee2679bf79e657229c161e6c669)`(`[`input_t`](#primitives_8h_1acb1903f2f2f7ed4502a5f53615cff8aa)` input)` {#input_8h_1a07e22ee2679bf79e657229c161e6c669}

Release the memory held by an input instance.

#### Parameters
* `input` Handle to an input instance

#### `public int `[`input_is_valid`](#input_8h_1a2403b0b3e70fc82976302dce797feeb8)`(`[`input_t`](#primitives_8h_1acb1903f2f2f7ed4502a5f53615cff8aa)` input)` {#input_8h_1a2403b0b3e70fc82976302dce797feeb8}

Determine if an input is valid.

#### Parameters
* `input` Handle to an input instance 

#### Returns
True (non zero) iif the input is valid

#### `public int `[`input_is_final`](#input_8h_1ad4c90e8e665df2478bbe2861cf16f3ce)`(`[`input_t`](#primitives_8h_1acb1903f2f2f7ed4502a5f53615cff8aa)` input)` {#input_8h_1ad4c90e8e665df2478bbe2861cf16f3ce}

Determine if an input is final.

#### Parameters
* `input` Handle to an input instance 

#### Returns
True (non zero) iif the input is final

#### `public size_t `[`input_serialized_size`](#input_8h_1ac5ce4f197473b950042053bc378311e1)`(`[`input_t`](#primitives_8h_1acb1903f2f2f7ed4502a5f53615cff8aa)` input,int wire)` {#input_8h_1ac5ce4f197473b950042053bc378311e1}

Get the input's serialized size.

#### Parameters
* `input` Handle to an input instance 

* `wire` Deprecated; currently ignored 

#### Returns
Input's serialized size

#### `public uint32_t `[`input_sequence`](#input_8h_1a17ca854ca78275acddea0a46bcf241f9)`(`[`input_t`](#primitives_8h_1acb1903f2f2f7ed4502a5f53615cff8aa)` input)` {#input_8h_1a17ca854ca78275acddea0a46bcf241f9}

Get the input's sequence number.

#### Parameters
* `input` Handle to an input instance 

#### Returns
The input's sequence number

#### `public size_t `[`input_signature_operations`](#input_8h_1a6112eeed9ced97e9b8a65535d259b455)`(`[`input_t`](#primitives_8h_1acb1903f2f2f7ed4502a5f53615cff8aa)` input,int bip16_active)` {#input_8h_1a6112eeed9ced97e9b8a65535d259b455}

Get the input's signature operations count.

#### Parameters
* `input` Handle to an input instance 

* `bip16_active` If true (non zero), consider only active operations 

#### Returns
Signature operations count

#### `public `[`script_t`](#primitives_8h_1a14a6f2e8d8ccced8b9bf7844e22e4aef)` `[`input_script`](#input_8h_1a5962a64778d3825861968bd7b93f37ca)`(`[`input_t`](#primitives_8h_1acb1903f2f2f7ed4502a5f53615cff8aa)` input)` {#input_8h_1a5962a64778d3825861968bd7b93f37ca}

Get input script.

#### Parameters
* `input` Handle to an input instance 

#### Returns
Handle to input script. Must be released by calling [script_destruct()](#script_8h_1a594a6462fb996f38aa6f7b6f54b0c9e0)

#### `public `[`output_point_t`](#primitives_8h_1ad4d5035e7d5ca4f6a10eafdfdfd2e074)` `[`input_previous_output`](#input_8h_1a6117fe1c39f484f7fef1d76df61cb514)`(`[`input_t`](#primitives_8h_1acb1903f2f2f7ed4502a5f53615cff8aa)` input)` {#input_8h_1a6117fe1c39f484f7fef1d76df61cb514}

Get the input's previous output.

#### Parameters
* `input` Handle to an input instance 

#### Returns
Handle to input's previous output. Must be released by calling output_point_destruct

#### `public `[`hash_t`](#primitives_8h_1aa0ccd30c9c9fb169daec5f65600e7c71)` `[`merkle_block_hash_nth`](#merkle__block_8h_1ae8c9b3a6d6573a51ab7908ae8dd82f78)`(`[`merkle_block_t`](#primitives_8h_1a17bcda76594c1a89acd36ec09d5e41a9)` block,size_t n)` {#merkle__block_8h_1ae8c9b3a6d6573a51ab7908ae8dd82f78}

Get the block's n-th hash.

#### Parameters
* `block` Handle to a Merkle block instance 

* `n` Index for selecting hash 

#### Returns
Handle to Merkle block's n-th hash. Must be released by calling delete[]

#### `public `[`header_t`](#primitives_8h_1ae6323fbfdc3ff99f33acbae250895ab8)` `[`merkle_block_header`](#merkle__block_8h_1ad4ee91f14e5bab50b388c5438ad59698)`(`[`merkle_block_t`](#primitives_8h_1a17bcda76594c1a89acd36ec09d5e41a9)` block)` {#merkle__block_8h_1ad4ee91f14e5bab50b388c5438ad59698}

Get Merkle block header.

#### Parameters
* `block` Handle to a Merkle block instance 

#### Returns
Handle to Merkle block header. Must be released by calling [header_destruct()](#header_8h_1a1d1d3fc9341337e1bddd2681fdfed682)

#### `public int `[`merkle_block_is_valid`](#merkle__block_8h_1ab0176f1b613f53a57476828a302a4178)`(`[`merkle_block_t`](#primitives_8h_1a17bcda76594c1a89acd36ec09d5e41a9)` block)` {#merkle__block_8h_1ab0176f1b613f53a57476828a302a4178}

Determine if a Merkle block is valid.

#### Parameters
* `block` Handle to a Merkle block instance 

#### Returns
True (non zero) iif the Merkle block is valid

#### `public size_t `[`merkle_block_hash_count`](#merkle__block_8h_1acb42d10ee086d6093266b98840da6c6b)`(`[`merkle_block_t`](#primitives_8h_1a17bcda76594c1a89acd36ec09d5e41a9)` block)` {#merkle__block_8h_1acb42d10ee086d6093266b98840da6c6b}

Get Merkle block hash count.

#### Parameters
* `block` Handle to a Merkle block instance 

#### Returns
The Merkle block hash count

#### `public size_t `[`merkle_block_serialized_size`](#merkle__block_8h_1afb2d66d2e76d8e409b736cd7d0383302)`(`[`merkle_block_t`](#primitives_8h_1a17bcda76594c1a89acd36ec09d5e41a9)` block,uint32_t version)` {#merkle__block_8h_1afb2d66d2e76d8e409b736cd7d0383302}

Get Merkle block serialized size.

#### Parameters
* `block` Handle to a Merkle block instance 

* `version` Protocol version 

#### Returns
The Merkle block serialized size

#### `public size_t `[`merkle_block_total_transaction_count`](#merkle__block_8h_1afb0c146c7501223601376a6144c953d6)`(`[`merkle_block_t`](#primitives_8h_1a17bcda76594c1a89acd36ec09d5e41a9)` block)` {#merkle__block_8h_1afb0c146c7501223601376a6144c953d6}

Get Merkle block transaction count.

#### Parameters
* `block` Handle to a Merkle block instance 

#### Returns
Merkle block transaction count

#### `public void `[`merkle_block_destruct`](#merkle__block_8h_1af871439cfb75225e78af8e3454a20ca3)`(`[`merkle_block_t`](#primitives_8h_1a17bcda76594c1a89acd36ec09d5e41a9)` block)` {#merkle__block_8h_1af871439cfb75225e78af8e3454a20ca3}

Release memory held by Merkle block instance.

#### Parameters
* `block` Handle to a Merkle block instance

#### `public void `[`merkle_block_reset`](#merkle__block_8h_1a45c8fca631807d31b893cff090e480e0)`(`[`merkle_block_t`](#primitives_8h_1a17bcda76594c1a89acd36ec09d5e41a9)` block)` {#merkle__block_8h_1a45c8fca631807d31b893cff090e480e0}

Reset Merkle block.

#### Parameters
* `block` Handle to a Merkle block instance

#### `public void `[`output_destruct`](#output_8h_1a974f0d91520ed93250bcd56e2d921590)`(`[`output_t`](#primitives_8h_1a6db821b2b1332e8be7a662d075ede0b0)` output)` {#output_8h_1a974f0d91520ed93250bcd56e2d921590}

Release memory held by an output instance.

#### Parameters
* `output` Handle to an output instance

#### `public int `[`output_is_valid`](#output_8h_1a0d68a3cfb17807c9a72c5e36a5ee15ce)`(`[`output_t`](#primitives_8h_1a6db821b2b1332e8be7a662d075ede0b0)` output)` {#output_8h_1a0d68a3cfb17807c9a72c5e36a5ee15ce}

Determine if an output is valid.

#### Parameters
* `output` Handle to an output instance 

#### Returns
True (non zero) iif the output is valid

#### `public size_t `[`output_serialized_size`](#output_8h_1a24adac96e97aa036e0336b309c71fd39)`(`[`output_t`](#primitives_8h_1a6db821b2b1332e8be7a662d075ede0b0)` output,int wire)` {#output_8h_1a24adac96e97aa036e0336b309c71fd39}

Get the output's serialized size.

#### Parameters
* `output` Handle to an output instance 

* `wire` Deprecated; currently ignored 

#### Returns
The output's serialized size

#### `public uint64_t `[`output_value`](#output_8h_1ab6f944581267dbc41e2fa251f2ff7546)`(`[`output_t`](#primitives_8h_1a6db821b2b1332e8be7a662d075ede0b0)` output)` {#output_8h_1ab6f944581267dbc41e2fa251f2ff7546}

Get the output's value.

#### Parameters
* `output` Handle to an output instance 

#### Returns
The output's value

#### `public size_t `[`output_signature_operations`](#output_8h_1a4cbbc9de86c223a7f473c18e8a86f305)`(`[`output_t`](#primitives_8h_1a6db821b2b1332e8be7a662d075ede0b0)` output)` {#output_8h_1a4cbbc9de86c223a7f473c18e8a86f305}

Get the output signature operations count.

#### Parameters
* `output` Handle to an output instance 

#### Returns
Amount of signature operations in the output

#### `public `[`script_t`](#primitives_8h_1a14a6f2e8d8ccced8b9bf7844e22e4aef)` `[`output_script`](#output_8h_1a8d1f20140cb6d480fbfe0e2622fa5065)`(`[`output_t`](#primitives_8h_1a6db821b2b1332e8be7a662d075ede0b0)` output)` {#output_8h_1a8d1f20140cb6d480fbfe0e2622fa5065}

: Get the output's script

#### Parameters
* `output` Handle to an output instance 

#### Returns
Handle to the output script instance. Must be released by calling script_destruct

#### `public `[`hash_t`](#primitives_8h_1aa0ccd30c9c9fb169daec5f65600e7c71)` `[`output_get_hash`](#output_8h_1aabd1bd7f280dc40de4e81b3470bb1ab4)`(`[`output_t`](#primitives_8h_1a6db821b2b1332e8be7a662d075ede0b0)` output)` {#output_8h_1aabd1bd7f280dc40de4e81b3470bb1ab4}

Get output hash.

#### Parameters
* `output` Handle to an output instance 

#### Returns
The output hash as a byte array. Must be released by calling delete[]

#### `public uint32_t `[`output_get_index`](#output_8h_1a0c90a1cb8f51f0a7451a965582a677fb)`(`[`output_t`](#primitives_8h_1a6db821b2b1332e8be7a662d075ede0b0)` output)` {#output_8h_1a0c90a1cb8f51f0a7451a965582a677fb}

Get the output's index.

#### Parameters
* `output` Handle to an output instance 

#### Returns
Output index

#### `public `[`hash_t`](#primitives_8h_1aa0ccd30c9c9fb169daec5f65600e7c71)` `[`output_point_get_hash`](#output__point_8h_1ac9f315a515685375a2b015f2afe17eef)`(`[`output_point_t`](#primitives_8h_1ad4d5035e7d5ca4f6a10eafdfdfd2e074)` output)` {#output__point_8h_1ac9f315a515685375a2b015f2afe17eef}

Get the output point's hash.

#### Parameters
* `output` Handle to an output point instance 

#### Returns
Point hash as byte array. Must be released by calling delete[]

#### `public `[`output_point_t`](#primitives_8h_1ad4d5035e7d5ca4f6a10eafdfdfd2e074)` `[`output_point_construct`](#output__point_8h_1aeb7c309b991761bff5cdc4c5cdcbad1e)`()` {#output__point_8h_1aeb7c309b991761bff5cdc4c5cdcbad1e}

Create an empty output point.

#### Returns
Handle to new output point instance. Must be released by calling outpout_point_destruct()

#### `public uint32_t `[`output_point_get_index`](#output__point_8h_1a496394e7491a75771b40d85c400665c2)`(`[`output_point_t`](#primitives_8h_1ad4d5035e7d5ca4f6a10eafdfdfd2e074)` output)` {#output__point_8h_1a496394e7491a75771b40d85c400665c2}

Get output point index inside the point. Starts at 0 (zero) with the first one.

#### Parameters
* `output` Handle to an output point instance 

#### Returns
Output point index

#### `public void `[`output_point_destruct`](#output__point_8h_1a4ae2358a29f31e9a0351585fbf61b993)`(`[`output_point_t`](#primitives_8h_1ad4d5035e7d5ca4f6a10eafdfdfd2e074)` output)` {#output__point_8h_1a4ae2358a29f31e9a0351585fbf61b993}

Release memory held by output point.

#### Parameters
* `output` Handle to an output point instance

#### `public char const  * `[`payment_address_encoded`](#payment__address_8h_1a51b00cfb74d43f59cf2ca2e735a2f7f1)`(`[`payment_address_t`](#primitives_8h_1acc9e0ae61a6bf90f01911484e4ede07b)` payment_address)` {#payment__address_8h_1a51b00cfb74d43f59cf2ca2e735a2f7f1}

Encode a payment address.

#### Parameters
* `payment_address` Handle to a payment address instance 

#### Returns
Encoded payment address

#### `public `[`payment_address_t`](#primitives_8h_1acc9e0ae61a6bf90f01911484e4ede07b)` `[`payment_address_construct_from_string`](#payment__address_8h_1a266e2071493b7ed6c7ff9bc9eb80b8fb)`(char const * address)` {#payment__address_8h_1a266e2071493b7ed6c7ff9bc9eb80b8fb}

Create a payment address from a string.

#### Parameters
* `address` String representing a payment address 

#### Returns
Handle to encoded payment address. Must be released by calling [payment_address_destruct()](#payment__address_8h_1a4b3dbd5712e7c6569c02763e0dfe4baa)

#### `public uint8_t `[`version`](#payment__address_8h_1a20d1238557cc4df561e5b09816ea9450)`(`[`payment_address_t`](#primitives_8h_1acc9e0ae61a6bf90f01911484e4ede07b)` payment_address)` {#payment__address_8h_1a20d1238557cc4df561e5b09816ea9450}

Get payment address version.

#### Parameters
* `payment_address` Handle to a payment address instance 

#### Returns
Payment address version

#### `public void `[`payment_address_destruct`](#payment__address_8h_1a4b3dbd5712e7c6569c02763e0dfe4baa)`(`[`payment_address_t`](#primitives_8h_1acc9e0ae61a6bf90f01911484e4ede07b)` payment_address)` {#payment__address_8h_1a4b3dbd5712e7c6569c02763e0dfe4baa}

Release memory held by payment address instance.

#### Parameters
* `payment_address` Handle to a payment address instance

#### `public `[`hash_t`](#primitives_8h_1aa0ccd30c9c9fb169daec5f65600e7c71)` `[`point_get_hash`](#point_8h_1a2a624b2b8a7f329d9962b7a1924e12ab)`(`[`point_t`](#primitives_8h_1af6e7950f472a081d958eb8519843d38b)` point)` {#point_8h_1a2a624b2b8a7f329d9962b7a1924e12ab}

Get point hash.

#### Parameters
* `point` Handle to point instance 

#### Returns
Point hash as byte array. Must be released by calling delete[]

#### `public int `[`point_is_valid`](#point_8h_1aa3224fcebb1829ab9916069c4473859c)`(`[`point_t`](#primitives_8h_1af6e7950f472a081d958eb8519843d38b)` point)` {#point_8h_1aa3224fcebb1829ab9916069c4473859c}

Determine if point is valid.

#### Parameters
* `point` Handle to point instance 

#### Returns
True (non zero) iif point is valid

#### `public uint32_t `[`point_get_index`](#point_8h_1a3fc9f37c57e85b06b0f5b4c6c16ba212)`(`[`point_t`](#primitives_8h_1af6e7950f472a081d958eb8519843d38b)` point)` {#point_8h_1a3fc9f37c57e85b06b0f5b4c6c16ba212}

Get point index.

#### Parameters
* `point` Handle to point instance 

#### Returns
Point index

#### `public uint64_t `[`point_get_checksum`](#point_8h_1a643229ebf5215c2068cee98d0e15fc7c)`(`[`point_t`](#primitives_8h_1af6e7950f472a081d958eb8519843d38b)` point)` {#point_8h_1a643229ebf5215c2068cee98d0e15fc7c}

Get point checksum.

#### Parameters
* `point` Handle to point instance 

#### Returns
Point checksum

#### `public `[`point_t`](#primitives_8h_1af6e7950f472a081d958eb8519843d38b)` `[`point_list_nth`](#point__list_8h_1a81e77050195c59f9d6a618fe8e3f77e1)`(`[`point_list_t`](#primitives_8h_1a58aa9400b0e0aaa34d6b5a1a2666bb29)` point_list,size_t n)` {#point__list_8h_1a81e77050195c59f9d6a618fe8e3f77e1}

Get the list's n-th point.

#### Parameters
* `point_list` Handle to a point list instance 

* `n` Index for the selected point. Starts at 0 (zero) with the first one 

#### Returns
Handle to selected point instance. Must be released with point_destruct()

#### `public size_t `[`point_list_count`](#point__list_8h_1a235ce31f8d2e130a3cbb998f7cf9f459)`(`[`point_list_t`](#primitives_8h_1a58aa9400b0e0aaa34d6b5a1a2666bb29)` point_list)` {#point__list_8h_1a235ce31f8d2e130a3cbb998f7cf9f459}

Get point list count.

#### Parameters
* `point_list` Handle to a point list instance 

#### Returns
Point list count

#### `public void `[`point_list_destruct`](#point__list_8h_1a06f5db8b275deb99ba1c3a31e60e86a2)`(`[`point_list_t`](#primitives_8h_1a58aa9400b0e0aaa34d6b5a1a2666bb29)` point_list)` {#point__list_8h_1a06f5db8b275deb99ba1c3a31e60e86a2}

Release memory held by point list instance.

#### Parameters
* `point_list` Handle to a point list instance

#### `public void `[`script_destruct`](#script_8h_1a594a6462fb996f38aa6f7b6f54b0c9e0)`(`[`script_t`](#primitives_8h_1a14a6f2e8d8ccced8b9bf7844e22e4aef)` script)` {#script_8h_1a594a6462fb996f38aa6f7b6f54b0c9e0}

Release memory held by a script instance.

#### Parameters
* `script` Handle to a script instance

#### `public int `[`script_is_valid`](#script_8h_1ac13f89765de02c5e08a39d8f76c1ad2f)`(`[`script_t`](#primitives_8h_1a14a6f2e8d8ccced8b9bf7844e22e4aef)` script)` {#script_8h_1ac13f89765de02c5e08a39d8f76c1ad2f}

Determine if a script is valid.

#### Parameters
* `script` Handle to a script instance 

#### Returns
True (non zero) iif the script is valid

#### `public int `[`script_is_valid_operations`](#script_8h_1afe1d83cba0d1d005d285882eeacc06a3)`(`[`script_t`](#primitives_8h_1a14a6f2e8d8ccced8b9bf7844e22e4aef)` script)` {#script_8h_1afe1d83cba0d1d005d285882eeacc06a3}

Determine if the script operations are valid.

#### Parameters
* `script` Handle to a script instance 

#### Returns
True (non zero) iif the script operations are valid

#### `public size_t `[`script_satoshi_content_size`](#script_8h_1a022d8a549bdde964bc1c00a77d50f2d0)`(`[`script_t`](#primitives_8h_1a14a6f2e8d8ccced8b9bf7844e22e4aef)` script)` {#script_8h_1a022d8a549bdde964bc1c00a77d50f2d0}

Get the script Satoshi content size.

#### Parameters
* `script` Handle to a script instance 

#### Returns
Script Satoshi content size

#### `public size_t `[`script_serialized_size`](#script_8h_1ac7d8b5cbb37e481721fd5dffd58fbc4d)`(`[`script_t`](#primitives_8h_1a14a6f2e8d8ccced8b9bf7844e22e4aef)` script,bool prefix)` {#script_8h_1ac7d8b5cbb37e481721fd5dffd58fbc4d}

Get script serialized size.

#### Parameters
* `script` Handle to a script instance 

* `prefix` If true, add prefix size to total size 

#### Returns
Script serialized size

#### `public char const  * `[`script_to_string`](#script_8h_1a16eafae91b17dc195dee2fc03b9219f4)`(`[`script_t`](#primitives_8h_1a14a6f2e8d8ccced8b9bf7844e22e4aef)` script,uint32_t active_forks)` {#script_8h_1a16eafae91b17dc195dee2fc03b9219f4}

Get script string representation.

#### Parameters
* `script` Handle to a script instance 

* `active_forks` Active forks count 

#### Returns
Script string representation

#### `public size_t `[`script_sigops`](#script_8h_1ab8814aa7853426f6ed6b3de848a27c83)`(`[`script_t`](#primitives_8h_1a14a6f2e8d8ccced8b9bf7844e22e4aef)` script,bool embedded)` {#script_8h_1ab8814aa7853426f6ed6b3de848a27c83}

Get script signature operations (sigops) count.

#### Parameters
* `script` Handle to a script instance 

* `embedded` Tells whether to consider embedded sigops in the count or not 

#### Returns
Script sigops count

#### `public size_t `[`script_embedded_sigops`](#script_8h_1a490c2ea9b3c053eb1048a3a90b8eefea)`(`[`script_t`](#primitives_8h_1a14a6f2e8d8ccced8b9bf7844e22e4aef)` script,`[`script_t`](#primitives_8h_1a14a6f2e8d8ccced8b9bf7844e22e4aef)` prevout_script)` {#script_8h_1a490c2ea9b3c053eb1048a3a90b8eefea}

Get script embedded signature operations (sigops) count.

#### Parameters
* `script` Handle to a script instance 

* `prevout_script` Handle to previous script instance 

#### Returns
Embedded signature operations count

#### `public void `[`transaction_destruct`](#transaction_8h_1ad32fc27899d84318a183ecf152967570)`(`[`transaction_t`](#primitives_8h_1a5618f23f10ca9f9ad96cf52f4059e995)` transaction)` {#transaction_8h_1ad32fc27899d84318a183ecf152967570}

Release memory held by transaction instance.

#### Parameters
* `transaction` Handle to transaction instance

#### `public int `[`transaction_is_valid`](#transaction_8h_1ad25670d899126e24ab1d156ac967a4df)`(`[`transaction_t`](#primitives_8h_1a5618f23f10ca9f9ad96cf52f4059e995)` transaction)` {#transaction_8h_1ad25670d899126e24ab1d156ac967a4df}

Determine if a transaction is valid.

#### Parameters
* `transaction` Handle to transaction instance 

#### Returns
True (non zero) iif a transaction is valid

#### `public uint32_t `[`transaction_version`](#transaction_8h_1ac2ab82b5e4ce6a7fbe0b253274849c34)`(`[`transaction_t`](#primitives_8h_1a5618f23f10ca9f9ad96cf52f4059e995)` transaction)` {#transaction_8h_1ac2ab82b5e4ce6a7fbe0b253274849c34}

Get transaction version.

#### Parameters
* `transaction` Handle to transaction instance 

#### Returns
Transaction version

#### `public void `[`transaction_set_version`](#transaction_8h_1a3a5951371c882dc42d49e1a87ccb7401)`(`[`transaction_t`](#primitives_8h_1a5618f23f10ca9f9ad96cf52f4059e995)` transaction,uint32_t version)` {#transaction_8h_1a3a5951371c882dc42d49e1a87ccb7401}

Set transaction version.

#### Parameters
* `transaction` Handle to transaction instance 

* `version` New value for transaction version

#### `public `[`hash_t`](#primitives_8h_1aa0ccd30c9c9fb169daec5f65600e7c71)` `[`transaction_hash`](#transaction_8h_1a0e6db5b986bbc034483d319f1221b37c)`(`[`transaction_t`](#primitives_8h_1a5618f23f10ca9f9ad96cf52f4059e995)` transaction)` {#transaction_8h_1a0e6db5b986bbc034483d319f1221b37c}

Get transaction hash.

#### Parameters
* `transaction` Handle to transaction instance 

#### Returns
Transaction hash as byte array. Must be released by calling delete[]

#### `public `[`hash_t`](#primitives_8h_1aa0ccd30c9c9fb169daec5f65600e7c71)` `[`transaction_hash_sighash_type`](#transaction_8h_1a922f312aad666746d25921814a6f1272)`(`[`transaction_t`](#primitives_8h_1a5618f23f10ca9f9ad96cf52f4059e995)` transaction,uint32_t sighash_type)` {#transaction_8h_1a922f312aad666746d25921814a6f1272}

Get transaction sighash by type.

#### Parameters
* `transaction` Handle to transaction instance 

* `sighash_type` Sighash type 

#### Returns
Sighash as byte array. Must be released by calling delete[]

#### `public uint32_t `[`transaction_locktime`](#transaction_8h_1a2c606bb46d54f237d9e19075e8336b4e)`(`[`transaction_t`](#primitives_8h_1a5618f23f10ca9f9ad96cf52f4059e995)` transaction)` {#transaction_8h_1a2c606bb46d54f237d9e19075e8336b4e}

Get transaction locktime.

#### Parameters
* `transaction` Handle to transaction instance 

#### Returns
Transaction locktime

#### `public size_t `[`transaction_serialized_size`](#transaction_8h_1a742cb6b1ef15066f58ea808292888977)`(`[`transaction_t`](#primitives_8h_1a5618f23f10ca9f9ad96cf52f4059e995)` transaction,int wire)` {#transaction_8h_1a742cb6b1ef15066f58ea808292888977}

Get transaction serialized size.

#### Parameters
* `transaction` Handle to transaction instance 

* `wire` Deprecated; currently ignored 

#### Returns
Transaction serialized size

#### `public uint64_t `[`transaction_fees`](#transaction_8h_1a18e73484e57bb57571c2496f2fb361da)`(`[`transaction_t`](#primitives_8h_1a5618f23f10ca9f9ad96cf52f4059e995)` transaction)` {#transaction_8h_1a18e73484e57bb57571c2496f2fb361da}

Get transaction fees.

#### Parameters
* `transaction` Handle to transaction instance 

#### Returns
Transaction fees

#### `public size_t `[`transaction_signature_operations`](#transaction_8h_1a2a51456f9e148f42c5dd84e1eca4e119)`(`[`transaction_t`](#primitives_8h_1a5618f23f10ca9f9ad96cf52f4059e995)` transaction)` {#transaction_8h_1a2a51456f9e148f42c5dd84e1eca4e119}

Get transaction signature operations count.

#### Parameters
* `transaction` Handle to transaction instance 

#### Returns
Transaction signature operations count

#### `public size_t `[`transaction_signature_operations_bip16_active`](#transaction_8h_1a56c17116d7235f6ebec6e25ffdcdbc0b)`(`[`transaction_t`](#primitives_8h_1a5618f23f10ca9f9ad96cf52f4059e995)` transaction,int bip16_active)` {#transaction_8h_1a56c17116d7235f6ebec6e25ffdcdbc0b}

Get transaction BIP0016 signature operations count.

#### Parameters
* `transaction` Handle to transaction instance 

* `bip16_active` If true, only consider active operations 

#### Returns
Transaction BIP0016 signature operations count

#### `public uint64_t `[`transaction_total_input_value`](#transaction_8h_1a72a7d67b3a88aea60275c6a4279e3150)`(`[`transaction_t`](#primitives_8h_1a5618f23f10ca9f9ad96cf52f4059e995)` transaction)` {#transaction_8h_1a72a7d67b3a88aea60275c6a4279e3150}

Get the sum of the transaction input values.

#### Parameters
* `transaction` Handle to transaction instance 

#### Returns
Sum of transaction input values

#### `public uint64_t `[`transaction_total_output_value`](#transaction_8h_1aa3b36997f594a4967808e166173becae)`(`[`transaction_t`](#primitives_8h_1a5618f23f10ca9f9ad96cf52f4059e995)` transaction)` {#transaction_8h_1aa3b36997f594a4967808e166173becae}

Get the sum of the transaction output values.

#### Parameters
* `transaction` Handle to transaction instance 

#### Returns
Sum of transaction output values

#### `public int `[`transaction_is_coinbase`](#transaction_8h_1a7a16bc0444fe445d5e690deb5b26783b)`(`[`transaction_t`](#primitives_8h_1a5618f23f10ca9f9ad96cf52f4059e995)` transaction)` {#transaction_8h_1a7a16bc0444fe445d5e690deb5b26783b}

Determine if a transaction is coinbase.

#### Parameters
* `transaction` Handle to transaction instance 

#### Returns
True (non zero) iif transaction is coinbase

#### `public int `[`transaction_is_null_non_coinbase`](#transaction_8h_1a9133115f7971f603ebe3d579f290a098)`(`[`transaction_t`](#primitives_8h_1a5618f23f10ca9f9ad96cf52f4059e995)` transaction)` {#transaction_8h_1a9133115f7971f603ebe3d579f290a098}

Determine if a transaction is null and not coinnase.

#### Parameters
* `transaction` Handle to transaction instance 

#### Returns
True (non zero) iif the transaction is null and not coinbase

#### `public int `[`transaction_is_oversized_coinbase`](#transaction_8h_1a202ed448323427c2bd2bf570da7755f6)`(`[`transaction_t`](#primitives_8h_1a5618f23f10ca9f9ad96cf52f4059e995)` transaction)` {#transaction_8h_1a202ed448323427c2bd2bf570da7755f6}

Determine if a transaction is oversized coinbase.

#### Parameters
* `transaction` Handle to transaction instance 

#### Returns
True (non zero) iif the transaction is oversized coinbase

#### `public int `[`transaction_is_immature`](#transaction_8h_1af59c2b852425cc6defb83564ac93d930)`(`[`transaction_t`](#primitives_8h_1a5618f23f10ca9f9ad96cf52f4059e995)` transaction,size_t target_height)` {#transaction_8h_1af59c2b852425cc6defb83564ac93d930}

Determine if a transaction is immature.

#### Parameters
* `transaction` Handle to transaction instance 

* `target_height` Target height 

#### Returns
True (non zero) iif the transaction is immature

#### `public int `[`transaction_is_overspent`](#transaction_8h_1a9f0a7d2da797716141c12b17ea961409)`(`[`transaction_t`](#primitives_8h_1a5618f23f10ca9f9ad96cf52f4059e995)` transaction)` {#transaction_8h_1a9f0a7d2da797716141c12b17ea961409}

Determine if a transaction is overspent.

#### Parameters
* `transaction` Handle to transaction instance 

#### Returns
True (non zero) iif the transaction is overspent

#### `public int `[`transaction_is_double_spend`](#transaction_8h_1abeb082da354f1794b20bde7c59fdeecb)`(`[`transaction_t`](#primitives_8h_1a5618f23f10ca9f9ad96cf52f4059e995)` transaction,int include_unconfirmed)` {#transaction_8h_1abeb082da354f1794b20bde7c59fdeecb}

Determine if a transaction is double spent.

#### Parameters
* `transaction` Handle to transaction instance 

* `include_unconfirmed` Tells whether to include unconfirmed outputs/inputs 

#### Returns
True (non zero) iif transaction is double spent

#### `public int `[`transaction_is_missing_previous_outputs`](#transaction_8h_1a6aa8bd4e08e142f6a14a4ab702dc8f69)`(`[`transaction_t`](#primitives_8h_1a5618f23f10ca9f9ad96cf52f4059e995)` transaction)` {#transaction_8h_1a6aa8bd4e08e142f6a14a4ab702dc8f69}

Determine whether transaction is missing previous outputs.

#### Parameters
* `transaction` Handle to transaction instance 

#### Returns
True (non zero) iif transaction is missing previous outputs

#### `public int `[`transaction_is_final`](#transaction_8h_1a516abef95a61b04e9275caaac85a1632)`(`[`transaction_t`](#primitives_8h_1a5618f23f10ca9f9ad96cf52f4059e995)` transaction,size_t block_height,uint32_t block_time)` {#transaction_8h_1a516abef95a61b04e9275caaac85a1632}

Determine if a transaction is final.

#### Parameters
* `transaction` Handle to transaction instance 

* `block_height` Transaction block height 

* `block_time` Transaction block time 

#### Returns
True (non zero) iif the transaction is final

#### `public int `[`transaction_is_locktime_conflict`](#transaction_8h_1a4e24096bfbadeea91e45715186137e7f)`(`[`transaction_t`](#primitives_8h_1a5618f23f10ca9f9ad96cf52f4059e995)` transaction)` {#transaction_8h_1a4e24096bfbadeea91e45715186137e7f}

Determine if a transaction incurs in a locktime conflict.

#### Parameters
* `transaction` Handle to transaction instance 

#### Returns
True (non zero) iif the transaction incurs in a locktime conflict

#### `public size_t `[`transaction_output_count`](#transaction_8h_1a44ce3dcf50895f79b005c4ffd2820358)`(`[`transaction_t`](#primitives_8h_1a5618f23f10ca9f9ad96cf52f4059e995)` transaction)` {#transaction_8h_1a44ce3dcf50895f79b005c4ffd2820358}

Get transaction output count.

#### Parameters
* `transaction` Handle to transaction instance 

#### Returns
Transaction output count

#### `public `[`output_t`](#primitives_8h_1a6db821b2b1332e8be7a662d075ede0b0)` `[`transaction_output_nth`](#transaction_8h_1ab85fba65372d0078afedcc839ed50d46)`(`[`transaction_t`](#primitives_8h_1a5618f23f10ca9f9ad96cf52f4059e995)` transaction,size_t n)` {#transaction_8h_1ab85fba65372d0078afedcc839ed50d46}

Get the transaction's n-th output.

#### Parameters
* `transaction` Handle to transaction instance 

* `n` Index to select transaction output. Starts at 0 (zero) for the first one 

#### Returns
Handle to n-th transaction output. Must be released by calling [output_destruct()](#output_8h_1a974f0d91520ed93250bcd56e2d921590)

#### `public size_t `[`transaction_input_count`](#transaction_8h_1ae6ce6c6592b7a4666592f23050bf51c9)`(`[`transaction_t`](#primitives_8h_1a5618f23f10ca9f9ad96cf52f4059e995)` transaction)` {#transaction_8h_1ae6ce6c6592b7a4666592f23050bf51c9}

Get transaction input count.

#### Parameters
* `transaction` Handle to transaction instance 

#### Returns
Transaction input count

#### `public `[`input_t`](#primitives_8h_1acb1903f2f2f7ed4502a5f53615cff8aa)` `[`transaction_input_nth`](#transaction_8h_1a58617f586abf033ed1cdaf77e087d538)`(`[`transaction_t`](#primitives_8h_1a5618f23f10ca9f9ad96cf52f4059e995)` transaction,size_t n)` {#transaction_8h_1a58617f586abf033ed1cdaf77e087d538}

Get n-th transaction input.

#### Parameters
* `transaction` Handle to transaction instance 

* `n` Index to transaction input. Starts at 0 (zero) for the first one 

#### Returns
Transaction's n-th input

#### `public `[`word_list_t`](#primitives_8h_1a547ee5b6df76cdddedd5e12dea357036)` `[`word_list_construct`](#word__list_8h_1ac30529cbf0ce5a79d53add1f61c0c90d)`()` {#word__list_8h_1ac30529cbf0ce5a79d53add1f61c0c90d}

Create a new word list instance.

#### Returns
Handle to new word list instance. Must be released by calling [word_list_destruct()](#word__list_8h_1a47d1b62e1dc307bac37279d213920436)

#### `public void `[`word_list_add_word`](#word__list_8h_1af359d913e1eb715be21608dbb90ee558)`(`[`word_list_t`](#primitives_8h_1a547ee5b6df76cdddedd5e12dea357036)` word_list,const char * word)` {#word__list_8h_1af359d913e1eb715be21608dbb90ee558}

Add a word to the word list 
#### Parameters
* `word_list` Handle to a word list instance 

* `word` New word

#### `public void `[`word_list_destruct`](#word__list_8h_1a47d1b62e1dc307bac37279d213920436)`(`[`word_list_t`](#primitives_8h_1a547ee5b6df76cdddedd5e12dea357036)` word_list)` {#word__list_8h_1a47d1b62e1dc307bac37279d213920436}

Release memory held by word list object.

#### Parameters
* `word_list` Handle to a word list instance

Generated by [Moxygen](https://sourcey.com/moxygen)