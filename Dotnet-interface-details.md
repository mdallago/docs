# Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`namespace `[`Bitprim`](#namespace_bitprim) | 
`namespace `[`Bitprim::Logging`](#namespace_bitprim_1_1_logging) | 
`namespace `[`Bitprim::Logging::LogProviders`](#namespace_bitprim_1_1_logging_1_1_log_providers) | 
`class `[`Bitprim::Logging::LoggerExecutionWrapper::CallSiteExtension`](#class_bitprim_1_1_logging_1_1_logger_execution_wrapper_1_1_call_site_extension) | 
`class `[`Constants`](#class_constants) | 
`class `[`Bitprim::Logging::LogProviders::Log4NetLogProvider::Log4NetLogger`](#class_bitprim_1_1_logging_1_1_log_providers_1_1_log4_net_log_provider_1_1_log4_net_logger) | 
`class `[`Bitprim::Logging::LogProviders::LoupeLogProvider::LoupeLogger`](#class_bitprim_1_1_logging_1_1_log_providers_1_1_loupe_log_provider_1_1_loupe_logger) | 
`class `[`Bitprim::Logging::LogProviders::NLogLogProvider::NLogLogger`](#class_bitprim_1_1_logging_1_1_log_providers_1_1_n_log_log_provider_1_1_n_log_logger) | 
`class `[`Bitprim::Logging::LogProvider::NoOpLogger`](#class_bitprim_1_1_logging_1_1_log_provider_1_1_no_op_logger) | 
`class `[`Bitprim::Logging::LogProviders::SerilogLogProvider::SerilogLogger`](#class_bitprim_1_1_logging_1_1_log_providers_1_1_serilog_log_provider_1_1_serilog_logger) | 

# namespace `Bitprim` 

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`enum `[`CurrencyType`](#namespace_bitprim_1a3f533178085ca25f9713df9565ad8182)            | 
`enum `[`ErrorCode`](#namespace_bitprim_1a3a9a6bda5cf124c14b0cd5c459566186)            | 
`enum `[`NetworkType`](#namespace_bitprim_1a22160858220a577b3c9c38dc3c0142cd)            | 
`class `[`Bitprim::ApiCallResult`](#class_bitprim_1_1_api_call_result) | 
`class `[`Bitprim::Binary`](#class_bitprim_1_1_binary) | Represents a binary filter.
`class `[`Bitprim::Block`](#class_bitprim_1_1_block) | Represents a full Bitcoin blockchain block.
`class `[`Bitprim::BlockReader`](#class_bitprim_1_1_block_reader) | Allows user to read a specific set of blocks from the blockchain.
`class `[`Bitprim::Chain`](#class_bitprim_1_1_chain) | Represents the Bitcoin blockchain; meant to offer its different interfaces (query, mining, network)
`class `[`Bitprim::DisposableApiCallResult`](#class_bitprim_1_1_disposable_api_call_result) | 
`class `[`Bitprim::Executor`](#class_bitprim_1_1_executor) | Controls the execution of the [Bitprim](#namespace_bitprim) bitcoin node.
`class `[`Bitprim::GetBlockDataResult`](#class_bitprim_1_1_get_block_data_result) | 
`class `[`Bitprim::GetBlockHashTimestampResult`](#class_bitprim_1_1_get_block_hash_timestamp_result) | 
`class `[`Bitprim::GetBlockHeaderByHashTxSizeResult`](#class_bitprim_1_1_get_block_header_by_hash_tx_size_result) | 
`class `[`Bitprim::GetTxDataResult`](#class_bitprim_1_1_get_tx_data_result) | 
`class `[`Bitprim::Header`](#class_bitprim_1_1_header) | Represents a full Bitcoin blockchain block.
`class `[`Bitprim::HeaderReader`](#class_bitprim_1_1_header_reader) | Helper for reading the header for each block in a specific set of blocks.
`class `[`Bitprim::HistoryCompact`](#class_bitprim_1_1_history_compact) | [Output](#class_bitprim_1_1_output) points, values, and spends for a payment address.
`class `[`Bitprim::Input`](#class_bitprim_1_1_input) | Represents a [Transaction](#class_bitprim_1_1_transaction) input.
`class `[`Bitprim::MempoolTransaction`](#class_bitprim_1_1_mempool_transaction) | Represents an unconfirmed transaction.
`class `[`Bitprim::MerkleBlock`](#class_bitprim_1_1_merkle_block) | Merkle tree representation of a blockchain block.
`class `[`Bitprim::NativeBuffer`](#class_bitprim_1_1_native_buffer) | RAII wrapper for native memory. Guarantees that even if an exception is thrown, platform_free will be used to release it. Also, it prevents the user from forgetting to call platform_free.
`class `[`Bitprim::NativeString`](#class_bitprim_1_1_native_string) | RAII wrapper for native strings. Guarantees that even if an exception is thrown, platform_free will be used to release the native memory. Also, it prevents the user from forgetting to call platform_free.
`class `[`Bitprim::NodeSettings`](#class_bitprim_1_1_node_settings) | 
`class `[`Bitprim::Output`](#class_bitprim_1_1_output) | Represents one of the outputs of a [Transaction](#class_bitprim_1_1_transaction).
`class `[`Bitprim::OutputPoint`](#class_bitprim_1_1_output_point) | [Transaction](#class_bitprim_1_1_transaction) hash and index pair representing one of the transaction outputs.
`class `[`Bitprim::PaymentAddress`](#class_bitprim_1_1_payment_address) | Represents a Bitcoin wallet address.
`class `[`Bitprim::Point`](#class_bitprim_1_1_point) | Represents one of the transaction inputs. It's a transaction hash and index pair.
`class `[`Bitprim::Script`](#class_bitprim_1_1_script) | Represents a transaction script.
`class `[`Bitprim::StealthCompact`](#class_bitprim_1_1_stealth_compact) | Stealth payment related data.
`class `[`Bitprim::TaskHelper`](#class_bitprim_1_1_task_helper) | 
`class `[`Bitprim::Transaction`](#class_bitprim_1_1_transaction) | Represents a Bitcoin transaction.
`class `[`Bitprim::Validations`](#class_bitprim_1_1_validations) | 
`struct `[`Bitprim::GetTxPositionResult`](#struct_bitprim_1_1_get_tx_position_result) | 

## Members

#### `enum `[`CurrencyType`](#namespace_bitprim_1a3f533178085ca25f9713df9565ad8182) 

 Values                         | Descriptions                                
--------------------------------|---------------------------------------------
None            | 
Bitcoin            | 
BitcoinCash            | 
Litecoin            | 

#### `enum `[`ErrorCode`](#namespace_bitprim_1a3a9a6bda5cf124c14b0cd5c459566186) 

 Values                         | Descriptions                                
--------------------------------|---------------------------------------------
Success            | 
Deprecated            | 
Unknown            | 
NotFound            | 
FileSystem            | 
NonStandard            | 
NotImplemented            | 
Oversubscribed            | 
ServiceStopped            | 
OperationFailed            | 
ResolveFailed            | 
NetworkUnreachable            | 
AddressInUse            | 
ListenFailed            | 
AcceptFailed            | 
BadStream            | 
ChannelTimeout            | 
AddressBlocked            | 
ChannelStopped            | 
PeerThrottling            | 
StoreBlockDuplicate            | 
StoreBlockInvalidHeight            | 
StoreBlockMissingParent            | 
DuplicateBlock            | 
OrphanBlock            | 
InvalidPreviousBlock            | 
InsufficientWork            | 
OrphanTransaction            | 
InsufficientFee            | 
DustyTransaction            | 
StaleChain            | 
InvalidProofOfWork            | 
FuturisticTimestamp            | 
CheckpointsFailed            | 
OldVersionBlock            | 
IncorrectProofOfWork            | 
TimestampTooEarly            | 
BlockSizeLimit            | 
EmptyBlock            | 
FirstNotCoinbase            | 
ExtraCoinbases            | 
InternalDuplicate            | 
BlockInternalDoubleSpend            | 
MerkleMismatch            | 
BlockLegacySigopLimit            | 
BlockNonFinal            | 
CoinbaseHeightMismatch            | 
CoinbaseValueLimit            | 
BlockEmbeddedSigopLimit            | 
EmptyTransaction            | 
PreviousOutputNull            | 
SpendOverflow            | 
InvalidCoinbaseScriptSize            | 
CoinbaseTransaction            | 
TransactionInternalDoubleSpend            | 
TransactionSizeLimit            | 
TransactionLegacySigopLimit            | 
TransactionNonFinal            | 
PrematureValidation            | 
UnspentDuplicate            | 
MissingPreviousOutput            | 
DoubleSpend            | 
CoinbaseMaturity            | 
SpendExceedsValue            | 
TransactionEmbeddedSigopLimit            | 
SequenceLocked            | 
InvalidScript            | 
InvalidScriptSize            | 
InvalidPushDataSize            | 
InvalidOperationCount            | 
InvalidStackSize            | 
InvalidStackScope            | 
InvalidScriptEmbed            | 
InvalidSignatureEncoding            | 
invalidSignatureLaxEncoding            | 
IncorrectSignature            | 
StackFalse            | 
OpDisabled            | 
OpReserved            | 
OpPushSize            | 
OpPushData            | 
OpIf            | 
OpNotIf            | 
OpElse            | 
OpEndIf            | 
OpVerify1            | 
OpVerify2            | 
OpReturn            | 
OpToAltStack            | 
OpFromAltStack            | 
OpDrop2            | 
OpDup2            | 
OpDup3            | 
OpOver2            | 
OpRot2            | 
OpSwap2            | 
OpIfDup            | 
OpDrop            | 
OpDup            | 
OpNip            | 
OpOver            | 
OpPick            | 
OpRoll            | 
OpRot            | 
OpSwap            | 
OpTuck            | 
OpSize            | 
OpEqual            | 
OpEqualVerify1            | 
OpEqualVerify2            | 
OpAdd1            | 
OpSub1            | 
OpNegate            | 
OpAbs            | 
OpNot            | 
OpNonZero            | 
OpAdd            | 
OpSub            | 
OpBoolAnd            | 
OpBoolOr            | 
OpNumEqual            | 
OpNumEqualVerify1            | 
OpNumEqualVerify2            | 
OpNumNotEqual            | 
OpLessThan            | 
OpGreaterThan            | 
OpLessThanOrEqual            | 
OpGreaterThanOrEqual            | 
OpMin            | 
OpMax            | 
OpWithin            | 
OpRipemd160            | 
OpSha1            | 
OpSha256            | 
OpHash160            | 
OpHash256            | 
OpCodeSeperator            | 
OpCheckSigVerify1            | 
OpCheckSig            | 
OpCheckMultisigVerify1            | 
OpCheckMultisigVerify2            | 
OpCheckMultisigVerify3            | 
OpCheckMultisigVerify4            | 
OpCheckMultisigVerify5            | 
OpCheckMultisigVerify6            | 
OpCheckMultisigVerify7            | 
OpCheckMultisig            | 
OpCheckLocktimeVerify1            | 
OpCheckLocktimeVerify2            | 
OpCheckLocktimeVerify3            | 
OpCheckLocktimeVerify4            | 
OpCheckLocktimeVerify5            | 
OpCheckLocktimeVerify6            | 
OpCheckSequenceVerify1            | 
OpCheckSequenceVerify2            | 
OpCheckSequenceVerify3            | 
OpCheckSequenceVerify4            | 
OpCheckSequenceVerify5            | 
OpCheckSequenceVerify6            | 
OpCheckSequenceVerify7            | 

#### `enum `[`NetworkType`](#namespace_bitprim_1a22160858220a577b3c9c38dc3c0142cd) 

 Values                         | Descriptions                                
--------------------------------|---------------------------------------------
None            | 
Mainnet            | 
Testnet            | 
Regtest            | 

# class `Bitprim::ApiCallResult` 

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`{property} ErrorCode `[`ErrorCode`](#class_bitprim_1_1_api_call_result_1a848f2895e2539ab00461ef32f19aaee9) | 
`{property} TResultData `[`Result`](#class_bitprim_1_1_api_call_result_1a8796a232b021151d3dd0da31f11c94c8) | 

## Members

#### `{property} ErrorCode `[`ErrorCode`](#class_bitprim_1_1_api_call_result_1a848f2895e2539ab00461ef32f19aaee9) 

#### `{property} TResultData `[`Result`](#class_bitprim_1_1_api_call_result_1a8796a232b021151d3dd0da31f11c94c8) 

# class `Bitprim::Binary` 

```
class Bitprim::Binary
  : public IDisposable
```  

Represents a binary filter.

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`{property} string `[`Encoded`](#class_bitprim_1_1_binary_1a348a5cb892a0ce13438ff51935a99729) | Filter representation as binary string.
`{property} IntPtr `[`NativeInstance`](#class_bitprim_1_1_binary_1a82cf37ab828336a0f9d5069c74cbf473) | 
`public inline  `[`Binary`](#class_bitprim_1_1_binary_1aacca6d3c790c49a363fbd27641c99556)`()` | Create an empty binary object.
`public inline  `[`Binary`](#class_bitprim_1_1_binary_1a6744d5e8c73ec3320c8cfd64b500a290)`(string hexString)` | Creates a binary filter from a binary string.
`public inline  `[`Binary`](#class_bitprim_1_1_binary_1aebec751d8756b49f20eb7b1de47ee505)`(UInt64 bitsSize,byte [] blocks,UInt64 n)` | Creates a binary filter from an int array.

## Members

#### `{property} string `[`Encoded`](#class_bitprim_1_1_binary_1a348a5cb892a0ce13438ff51935a99729) 

Filter representation as binary string.

#### `{property} IntPtr `[`NativeInstance`](#class_bitprim_1_1_binary_1a82cf37ab828336a0f9d5069c74cbf473) 

#### `public inline  `[`Binary`](#class_bitprim_1_1_binary_1aacca6d3c790c49a363fbd27641c99556)`()` 

Create an empty binary object.

#### `public inline  `[`Binary`](#class_bitprim_1_1_binary_1a6744d5e8c73ec3320c8cfd64b500a290)`(string hexString)` 

Creates a binary filter from a binary string.

#### Parameters
* `hexString` [Binary](#class_bitprim_1_1_binary) string. Example: '10111010101011011111000000001101'

#### `public inline  `[`Binary`](#class_bitprim_1_1_binary_1aebec751d8756b49f20eb7b1de47ee505)`(UInt64 bitsSize,byte [] blocks,UInt64 n)` 

Creates a binary filter from an int array.

#### Parameters
* `bitsSize` Elements size 

* `blocks` Filter representation. Example: '[186,173,240,13]'. 

* `n` Array length in amount of elements.

# class `Bitprim::Block` 

```
class Bitprim::Block
  : public IDisposable
```  

Represents a full Bitcoin blockchain block.

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`{property} bool `[`IsDistinctTransactionSet`](#class_bitprim_1_1_block_1afe00a47b830014c432d79377a1fcf1cc) | Returns true iif all transactions in the block have a unique hash (i.e. no duplicates)
`{property} bool `[`IsExtraCoinbase`](#class_bitprim_1_1_block_1a87a47aa97c8ef31879f1d46fb5825721) | Returns true iif there is more than one coinbase transaction in the block.
`{property} bool `[`IsInternalDoubleSpend`](#class_bitprim_1_1_block_1a02b6dc463e369c4cc989482eb0a82290) | Returns true iif there is at least one double-spent transaction in this block
`{property} bool `[`IsValid`](#class_bitprim_1_1_block_1ab97c0f6e1a70608223c06a5267e65d3a) | Returns true iif the block is valid
`{property} bool `[`IsValidMerkleRoot`](#class_bitprim_1_1_block_1a962a4437dd4b5fdaae6e07248ea12d14) | Returns true iif the generated Merkle root equals the header's Merkle root.
`{property} byte [] `[`Hash`](#class_bitprim_1_1_block_1ad2bfcf76b735aa2c26838d32a03f6d48) | The block's hash as a 32 byte array.
`{property} byte [] `[`MerkleRoot`](#class_bitprim_1_1_block_1a12cd915f751441bc6f9c4c268a4fa349) | The block's Merkle root, as a 32 byte array.
`{property} `[`Header`](#class_bitprim_1_1_header)` `[`Header`](#class_bitprim_1_1_block_1a8e8c733200d3defbd8f71609f54a928d) | The block's header
`{property} string `[`Proof`](#class_bitprim_1_1_block_1a6f2f056f16e77fa4072a22caf3ea8ac1) | 
`{property} UInt64 `[`Fees`](#class_bitprim_1_1_block_1a05b35dd6f0f40f631f09846992b8d2ea) | Miner fees included in the block's coinbase transaction.
`{property} UInt64 `[`Claim`](#class_bitprim_1_1_block_1a0d05159ba470f6392f0b21b7f2e7cb25) | Sum of coinbase outputs.
`{property} UInt64 `[`SignatureOperationsCount`](#class_bitprim_1_1_block_1a4731e46255eadfe9aeab1ca9595dfaa1) | Amount of signature operations in the block.
`{property} UInt64 `[`TransactionCount`](#class_bitprim_1_1_block_1a99e6bc147a2c5375cec10bc180793899) | The total amount of transactions that the block contains.
`{property} IntPtr `[`NativeInstance`](#class_bitprim_1_1_block_1a9cf18b56ed584c02e3c361ded648712f) | 
`public inline bool `[`IsFinal`](#class_bitprim_1_1_block_1a1811740e5097c938813f535aa6563e19)`(UInt64 height)` | Returns true iif every transaction in the block is final or not.
`public inline bool `[`IsValidCoinbaseClaim`](#class_bitprim_1_1_block_1a36bab07eeb6975e123d28d9f6bd2e268)`(UInt64 height)` | Given a block height, return true iif its coinbase claim is not higher than the deserved reward.
`public inline bool `[`IsValidCoinbaseScript`](#class_bitprim_1_1_block_1a700e460e6f249f175c719e874c085561)`(UInt64 height)` | Returns true iif the block's coinbase script is valid.
`public inline byte [] `[`ToData`](#class_bitprim_1_1_block_1a175982ee3e3e8fc96d00af710866838d)`(bool wire)` | Raw block data.
`public inline `[`Transaction`](#class_bitprim_1_1_transaction)` `[`GetNthTransaction`](#class_bitprim_1_1_block_1a4b82ec51f06d880ab179a22e6d27e515)`(UInt64 n)` | Given a position in the block, returns the corresponding transaction.
`public inline UInt64 `[`GetBlockReward`](#class_bitprim_1_1_block_1a65806245a063c53aa11fe46306a97578)`(UInt64 height)` | Reward = Subsidy + Fees, for the block at the given height.
`public inline UInt64 `[`GetSerializedSize`](#class_bitprim_1_1_block_1a0922fac15c8b25e31895bc4e014ae3bc)`(UInt32 version)` | [Block](#class_bitprim_1_1_block) size in bytes.
`public inline UInt64 `[`GetSignatureOperationsCount`](#class_bitprim_1_1_block_1a3b4c90d08441c351b6e4c016a0ad433f)`(bool bip16Active)` | Amount of signature operations in the block.
`public inline UInt64 `[`GetTotalInputs`](#class_bitprim_1_1_block_1a7dcaac2c475eb12f158f23fc1bba6808)`(bool withCoinbase)` | The sum of all inputs of all transactions in the block.

## Members

#### `{property} bool `[`IsDistinctTransactionSet`](#class_bitprim_1_1_block_1afe00a47b830014c432d79377a1fcf1cc) 

Returns true iif all transactions in the block have a unique hash (i.e. no duplicates)

#### `{property} bool `[`IsExtraCoinbase`](#class_bitprim_1_1_block_1a87a47aa97c8ef31879f1d46fb5825721) 

Returns true iif there is more than one coinbase transaction in the block.

#### `{property} bool `[`IsInternalDoubleSpend`](#class_bitprim_1_1_block_1a02b6dc463e369c4cc989482eb0a82290) 

Returns true iif there is at least one double-spent transaction in this block

#### `{property} bool `[`IsValid`](#class_bitprim_1_1_block_1ab97c0f6e1a70608223c06a5267e65d3a) 

Returns true iif the block is valid

#### `{property} bool `[`IsValidMerkleRoot`](#class_bitprim_1_1_block_1a962a4437dd4b5fdaae6e07248ea12d14) 

Returns true iif the generated Merkle root equals the header's Merkle root.

#### `{property} byte [] `[`Hash`](#class_bitprim_1_1_block_1ad2bfcf76b735aa2c26838d32a03f6d48) 

The block's hash as a 32 byte array.

#### `{property} byte [] `[`MerkleRoot`](#class_bitprim_1_1_block_1a12cd915f751441bc6f9c4c268a4fa349) 

The block's Merkle root, as a 32 byte array.

#### `{property} `[`Header`](#class_bitprim_1_1_header)` `[`Header`](#class_bitprim_1_1_block_1a8e8c733200d3defbd8f71609f54a928d) 

The block's header

#### `{property} string `[`Proof`](#class_bitprim_1_1_block_1a6f2f056f16e77fa4072a22caf3ea8ac1) 

#### `{property} UInt64 `[`Fees`](#class_bitprim_1_1_block_1a05b35dd6f0f40f631f09846992b8d2ea) 

Miner fees included in the block's coinbase transaction.

#### `{property} UInt64 `[`Claim`](#class_bitprim_1_1_block_1a0d05159ba470f6392f0b21b7f2e7cb25) 

Sum of coinbase outputs.

#### `{property} UInt64 `[`SignatureOperationsCount`](#class_bitprim_1_1_block_1a4731e46255eadfe9aeab1ca9595dfaa1) 

Amount of signature operations in the block.

#### `{property} UInt64 `[`TransactionCount`](#class_bitprim_1_1_block_1a99e6bc147a2c5375cec10bc180793899) 

The total amount of transactions that the block contains.

#### `{property} IntPtr `[`NativeInstance`](#class_bitprim_1_1_block_1a9cf18b56ed584c02e3c361ded648712f) 

#### `public inline bool `[`IsFinal`](#class_bitprim_1_1_block_1a1811740e5097c938813f535aa6563e19)`(UInt64 height)` 

Returns true iif every transaction in the block is final or not.

#### Parameters
* `height` 

#### Returns

#### `public inline bool `[`IsValidCoinbaseClaim`](#class_bitprim_1_1_block_1a36bab07eeb6975e123d28d9f6bd2e268)`(UInt64 height)` 

Given a block height, return true iif its coinbase claim is not higher than the deserved reward.

#### Parameters
* `height` The height which identifies the block to examine

#### Returns
True iif 1 if coinbase claim is not higher than the deserved reward.

#### `public inline bool `[`IsValidCoinbaseScript`](#class_bitprim_1_1_block_1a700e460e6f249f175c719e874c085561)`(UInt64 height)` 

Returns true iif the block's coinbase script is valid.

#### Parameters
* `height` The block's height. Identifies it univocally. 

#### Returns
True iif the block's coinbase script is valid.

#### `public inline byte [] `[`ToData`](#class_bitprim_1_1_block_1a175982ee3e3e8fc96d00af710866838d)`(bool wire)` 

Raw block data.

#### Parameters
* `wire` Iif true, include data size at the beginning.

#### Returns
Byte array with block data.

#### `public inline `[`Transaction`](#class_bitprim_1_1_transaction)` `[`GetNthTransaction`](#class_bitprim_1_1_block_1a4b82ec51f06d880ab179a22e6d27e515)`(UInt64 n)` 

Given a position in the block, returns the corresponding transaction.

#### Parameters
* `n` Zero-based index 

#### Returns
Full transaction object

#### `public inline UInt64 `[`GetBlockReward`](#class_bitprim_1_1_block_1a65806245a063c53aa11fe46306a97578)`(UInt64 height)` 

Reward = Subsidy + Fees, for the block at the given height.

#### Parameters
* `height` [Block](#class_bitprim_1_1_block) height in the chain; identifies it univocally. 

#### Returns
UInt64 representation of the block's reward.

#### `public inline UInt64 `[`GetSerializedSize`](#class_bitprim_1_1_block_1a0922fac15c8b25e31895bc4e014ae3bc)`(UInt32 version)` 

[Block](#class_bitprim_1_1_block) size in bytes.

#### Parameters
* `version` Protocol version. 

#### Returns
UInt64 representation of the block size in bytes.

#### `public inline UInt64 `[`GetSignatureOperationsCount`](#class_bitprim_1_1_block_1a3b4c90d08441c351b6e4c016a0ad433f)`(bool bip16Active)` 

Amount of signature operations in the block.

#### Parameters
* `bip16Active` Iif true, count bip16 active operations. 

#### Returns
The amount of signature operations in this block

#### `public inline UInt64 `[`GetTotalInputs`](#class_bitprim_1_1_block_1a7dcaac2c475eb12f158f23fc1bba6808)`(bool withCoinbase)` 

The sum of all inputs of all transactions in the block.

#### Parameters
* `withCoinbase` Iif true, consider coinbase transactions. 

#### Returns
UInt64 representation of the sum

# class `Bitprim::BlockReader` 

```
class Bitprim::BlockReader
  : public IDisposable
```  

Allows user to read a specific set of blocks from the blockchain.

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`{property} bool `[`IsValid`](#class_bitprim_1_1_block_reader_1abc3a66acbadba275e8c53c9bb95414d0) | Return true iif all blocks in the specified set are valid
`{property} byte [] `[`StopHash`](#class_bitprim_1_1_block_reader_1a645f071f77d3bec92772d8d0fbf6728f) | Get or set on which block to stop reading.
`{property} HashList `[`StartHashes`](#class_bitprim_1_1_block_reader_1ae8994bb2e2da8bbd60646ecba426d3da) | Get or set the hashes that have to be read in order to start reading.
`public inline  `[`BlockReader`](#class_bitprim_1_1_block_reader_1a2f3517010212c08923713744102191f8)`()` | 
`public inline  `[`BlockReader`](#class_bitprim_1_1_block_reader_1afe8436a6e4f16343654fcfea4709120c)`(HashList start,byte [] stop)` | 
`public inline UInt64 `[`GetSerializedSize`](#class_bitprim_1_1_block_reader_1a610a7c455b51380ac5afc0ac623cd843)`(UInt32 version)` | The sum of the sizes of the read blocks.
`public inline void `[`Reset`](#class_bitprim_1_1_block_reader_1afb00b31f123c231a970b4cdf16e20d08)`()` | Go back to the beginning of the block set.

## Members

#### `{property} bool `[`IsValid`](#class_bitprim_1_1_block_reader_1abc3a66acbadba275e8c53c9bb95414d0) 

Return true iif all blocks in the specified set are valid

#### `{property} byte [] `[`StopHash`](#class_bitprim_1_1_block_reader_1a645f071f77d3bec92772d8d0fbf6728f) 

Get or set on which block to stop reading.

#### `{property} HashList `[`StartHashes`](#class_bitprim_1_1_block_reader_1ae8994bb2e2da8bbd60646ecba426d3da) 

Get or set the hashes that have to be read in order to start reading.

#### `public inline  `[`BlockReader`](#class_bitprim_1_1_block_reader_1a2f3517010212c08923713744102191f8)`()` 

#### `public inline  `[`BlockReader`](#class_bitprim_1_1_block_reader_1afe8436a6e4f16343654fcfea4709120c)`(HashList start,byte [] stop)` 

#### `public inline UInt64 `[`GetSerializedSize`](#class_bitprim_1_1_block_reader_1a610a7c455b51380ac5afc0ac623cd843)`(UInt32 version)` 

The sum of the sizes of the read blocks.

#### Parameters
* `version` Protocol version to consider when calculating block size. 

#### Returns
UInt64 representation of the sum

#### `public inline void `[`Reset`](#class_bitprim_1_1_block_reader_1afb00b31f123c231a970b4cdf16e20d08)`()` 

Go back to the beginning of the block set.

# class `Bitprim::Chain` 

Represents the Bitcoin blockchain; meant to offer its different interfaces (query, mining, network)

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`{property} IntPtr `[`NativeInstance`](#class_bitprim_1_1_chain_1a6ba45403dfc6b61b59c8849a9bf565f3) | 
`{property} bool `[`IsStale`](#class_bitprim_1_1_chain_1a8b8851b7dd1cb47efdec3817277faaad) | Determine if the node is synchronized (i.e. has the latest copy of the blockchain/is at top height)
`public inline async Task< `[`ApiCallResult`](#class_bitprim_1_1_api_call_result)`< UInt64 > > `[`FetchBlockHeightAsync`](#class_bitprim_1_1_chain_1a05e73bd15a88afc5005319018e6dda39)`(byte [] blockHash)` | Given a block hash, it queries the chain asynchronously for the block's height. Return right away and uses a callback to return the result.
`public inline async Task< `[`ApiCallResult`](#class_bitprim_1_1_api_call_result)`< UInt64 > > `[`FetchLastHeightAsync`](#class_bitprim_1_1_chain_1aa99d17cc65a7b313b93513d92634bbd9)`()` | Gets the height of the highest block in the local copy of the blockchain, asynchronously.
`public inline async Task< `[`DisposableApiCallResult](#class_bitprim_1_1_disposable_api_call_result)< [GetBlockDataResult](#class_bitprim_1_1_get_block_data_result)< [Block`](#class_bitprim_1_1_block)` > > > `[`FetchBlockByHashAsync`](#class_bitprim_1_1_chain_1a4c912cb5da30ad7373f5869f37b66bbc)`(byte [] blockHash)` | Given a block hash, retrieve the full block it identifies, asynchronously.
`public inline async Task< `[`DisposableApiCallResult](#class_bitprim_1_1_disposable_api_call_result)< [GetBlockDataResult](#class_bitprim_1_1_get_block_data_result)< [Block`](#class_bitprim_1_1_block)` > > > `[`FetchBlockByHeightAsync`](#class_bitprim_1_1_chain_1a07cf0ef0db61d176403b7107aad8cca0)`(UInt64 height)` | Given a block height, retrieve the full block it identifies, asynchronously.
`public inline async Task< `[`DisposableApiCallResult](#class_bitprim_1_1_disposable_api_call_result)< [GetBlockHeaderByHashTxSizeResult`](#class_bitprim_1_1_get_block_header_by_hash_tx_size_result)` > > `[`FetchBlockHeaderByHashTxSizesAsync`](#class_bitprim_1_1_chain_1a16fbf9347d382e413596738050e477cc)`(byte [] blockHash)` | Given a block hash, retrieve block header, tx hashes and serialized block size, asynchronously.
`public inline async Task< `[`ApiCallResult](#class_bitprim_1_1_api_call_result)< [GetBlockHashTimestampResult`](#class_bitprim_1_1_get_block_hash_timestamp_result)` > > `[`FetchBlockByHeightHashTimestampAsync`](#class_bitprim_1_1_chain_1a0ed827e80a50f6ef1537f4e3323161ec)`(UInt64 height)` | Given a block height, retrieve only block hash and timestamp, asynchronously.
`public inline async Task< `[`DisposableApiCallResult](#class_bitprim_1_1_disposable_api_call_result)< [GetBlockDataResult](#class_bitprim_1_1_get_block_data_result)< [Header`](#class_bitprim_1_1_header)` > > > `[`FetchBlockHeaderByHashAsync`](#class_bitprim_1_1_chain_1a481afe875fea3bed18fdcc5f34881d24)`(byte [] blockHash)` | Given a block hash, get the header from the block it identifies, asynchronously.
`public inline async Task< `[`DisposableApiCallResult](#class_bitprim_1_1_disposable_api_call_result)< [GetBlockDataResult](#class_bitprim_1_1_get_block_data_result)< [Header`](#class_bitprim_1_1_header)` > > > `[`FetchBlockHeaderByHeightAsync`](#class_bitprim_1_1_chain_1af8dde319dada6e5fc337110280e7ecdf)`(UInt64 height)` | Given a block height, get the header from the block it identifies, asynchronously.
`public inline async Task< `[`DisposableApiCallResult](#class_bitprim_1_1_disposable_api_call_result)< [GetBlockDataResult](#class_bitprim_1_1_get_block_data_result)< [MerkleBlock`](#class_bitprim_1_1_merkle_block)` > > > `[`FetchMerkleBlockByHashAsync`](#class_bitprim_1_1_chain_1a3065a220899aa4e7499e00c82a986800)`(byte [] blockHash)` | Given a block hash, get the merkle block from the block it identifies, asynchronously.
`public inline async Task< `[`DisposableApiCallResult](#class_bitprim_1_1_disposable_api_call_result)< [GetBlockDataResult](#class_bitprim_1_1_get_block_data_result)< [MerkleBlock`](#class_bitprim_1_1_merkle_block)` > > > `[`FetchMerkleBlockByHeightAsync`](#class_bitprim_1_1_chain_1a51960cb40096565cba29801ecef869ce)`(UInt64 height)` | Given a block height, get the merkle block from the block it identifies, asynchronously.
`public inline async Task< `[`DisposableApiCallResult](#class_bitprim_1_1_disposable_api_call_result)< [GetBlockDataResult`](#class_bitprim_1_1_get_block_data_result)`< CompactBlock > > > `[`FetchCompactBlockByHash`](#class_bitprim_1_1_chain_1a7d2a96a34f4db98b4bb95f0945c8eb91)`(byte [] blockHash)` | Given a block hash, get the compact block from the block it identifies, asynchronously.
`public inline async Task< `[`DisposableApiCallResult](#class_bitprim_1_1_disposable_api_call_result)< [GetBlockDataResult`](#class_bitprim_1_1_get_block_data_result)`< CompactBlock > > > `[`FetchCompactBlockByHeightAsync`](#class_bitprim_1_1_chain_1ab44be34165be4cd968eecd0b8aa0daba)`(UInt64 height)` | Given a block height, get the compact block from the block it identifies, asynchronously.
`public inline async Task< `[`DisposableApiCallResult](#class_bitprim_1_1_disposable_api_call_result)< [GetTxDataResult`](#class_bitprim_1_1_get_tx_data_result)` > > `[`FetchTransactionAsync`](#class_bitprim_1_1_chain_1acd7a013b2d7dfb59a2be96c7e0fbe4ce)`(byte [] txHash,bool requireConfirmed)` | Get a transaction by its hash, asynchronously.
`public inline async Task< `[`ApiCallResult](#class_bitprim_1_1_api_call_result)< [GetTxPositionResult`](#struct_bitprim_1_1_get_tx_position_result)` > > `[`FetchTransactionPositionAsync`](#class_bitprim_1_1_chain_1a5dc1c0c121540d6f3fcdac769e5dfcbb)`(byte [] txHash,bool requireConfirmed)` | Given a transaction hash, it fetches the height and position inside the block, asynchronously.
`public inline async Task< `[`ApiCallResult](#class_bitprim_1_1_api_call_result)< [Point`](#class_bitprim_1_1_point)` > > `[`FetchSpendAsync`](#class_bitprim_1_1_chain_1aa6f96700ac465dfb8899f8199c65a372)`(`[`OutputPoint`](#class_bitprim_1_1_output_point)` outputPoint)` | Fetch the transaction input which spends the indicated output, asynchronously.
`public inline async Task< `[`DisposableApiCallResult`](#class_bitprim_1_1_disposable_api_call_result)`< HistoryCompactList > > `[`FetchHistoryAsync`](#class_bitprim_1_1_chain_1ab8077112761466c2e19eca51d3e5eadf)`(`[`PaymentAddress`](#class_bitprim_1_1_payment_address)` address,UInt64 limit,UInt64 fromHeight)` | Get a list of output points, values, and spends for a given payment address (asynchronously)
`public inline async Task< `[`DisposableApiCallResult`](#class_bitprim_1_1_disposable_api_call_result)`< HashList > > `[`FetchConfirmedTransactionsAsync`](#class_bitprim_1_1_chain_1affd9881e0c675e1e3202b33c697043e8)`(`[`PaymentAddress`](#class_bitprim_1_1_payment_address)` address,UInt64 limit,UInt64 fromHeight)` | Get a list of tx ids for a given payment address (asynchronously). Duplicates are already filtered out.
`public inline async Task< `[`DisposableApiCallResult`](#class_bitprim_1_1_disposable_api_call_result)`< StealthCompactList > > `[`FetchStealthAsync`](#class_bitprim_1_1_chain_1a9a39b99193848b3c051b8b4eb985e692)`(`[`Binary`](#class_bitprim_1_1_binary)` filter,UInt64 fromHeight)` | Get metadata on potential payment transactions by stealth filter. Given a filter and a height in the chain, it queries the chain for transactions matching the given filter.
`public inline async Task< `[`DisposableApiCallResult](#class_bitprim_1_1_disposable_api_call_result)< [HeaderReader`](#class_bitprim_1_1_header_reader)` > > `[`FetchBlockLocatorAsync`](#class_bitprim_1_1_chain_1ab76ad8f4fecec65e9934c38288f23f56)`(BlockIndexList indexes)` | Given a list of indexes, fetch a header reader for them, asynchronously
`public inline async Task< ErrorCode > `[`OrganizeBlockAsync`](#class_bitprim_1_1_chain_1ac98d25baa15b37a77a48becca57c4968)`(`[`Block`](#class_bitprim_1_1_block)` block)` | Given a block, organize it (async).
`public inline async Task< ErrorCode > `[`OrganizeTransactionAsync`](#class_bitprim_1_1_chain_1a23be64a1bbec23574fd616edede37111)`(`[`Transaction`](#class_bitprim_1_1_transaction)` transaction)` | Given a transaction, organize it (async).
`public inline async Task< `[`ApiCallResult`](#class_bitprim_1_1_api_call_result)`< string > > `[`ValidateTransactionAsync`](#class_bitprim_1_1_chain_1a233758a5d970628d399287a851795670)`(`[`Transaction`](#class_bitprim_1_1_transaction)` transaction)` | Determine if a transaction is valid for submission to the blockchain.
`public inline MempoolTransactionList `[`GetMempoolTransactions`](#class_bitprim_1_1_chain_1a44a0cd66999dde4914e1e013c582d731)`(`[`PaymentAddress`](#class_bitprim_1_1_payment_address)` address,bool useTestnetRules)` | 

## Members

#### `{property} IntPtr `[`NativeInstance`](#class_bitprim_1_1_chain_1a6ba45403dfc6b61b59c8849a9bf565f3) 

#### `{property} bool `[`IsStale`](#class_bitprim_1_1_chain_1a8b8851b7dd1cb47efdec3817277faaad) 

Determine if the node is synchronized (i.e. has the latest copy of the blockchain/is at top height)

#### `public inline async Task< `[`ApiCallResult`](#class_bitprim_1_1_api_call_result)`< UInt64 > > `[`FetchBlockHeightAsync`](#class_bitprim_1_1_chain_1a05e73bd15a88afc5005319018e6dda39)`(byte [] blockHash)` 

Given a block hash, it queries the chain asynchronously for the block's height. Return right away and uses a callback to return the result.

#### Parameters
* `blockHash` 32-byte array representation of the block hash. Identifies it univocally.

#### `public inline async Task< `[`ApiCallResult`](#class_bitprim_1_1_api_call_result)`< UInt64 > > `[`FetchLastHeightAsync`](#class_bitprim_1_1_chain_1aa99d17cc65a7b313b93513d92634bbd9)`()` 

Gets the height of the highest block in the local copy of the blockchain, asynchronously.

#### `public inline async Task< `[`DisposableApiCallResult](#class_bitprim_1_1_disposable_api_call_result)< [GetBlockDataResult](#class_bitprim_1_1_get_block_data_result)< [Block`](#class_bitprim_1_1_block)` > > > `[`FetchBlockByHashAsync`](#class_bitprim_1_1_chain_1a4c912cb5da30ad7373f5869f37b66bbc)`(byte [] blockHash)` 

Given a block hash, retrieve the full block it identifies, asynchronously.

#### Parameters
* `blockHash` 32 bytes of the block hash

#### `public inline async Task< `[`DisposableApiCallResult](#class_bitprim_1_1_disposable_api_call_result)< [GetBlockDataResult](#class_bitprim_1_1_get_block_data_result)< [Block`](#class_bitprim_1_1_block)` > > > `[`FetchBlockByHeightAsync`](#class_bitprim_1_1_chain_1a07cf0ef0db61d176403b7107aad8cca0)`(UInt64 height)` 

Given a block height, retrieve the full block it identifies, asynchronously.

#### Parameters
* `height` [Block](#class_bitprim_1_1_block) height

#### `public inline async Task< `[`DisposableApiCallResult](#class_bitprim_1_1_disposable_api_call_result)< [GetBlockHeaderByHashTxSizeResult`](#class_bitprim_1_1_get_block_header_by_hash_tx_size_result)` > > `[`FetchBlockHeaderByHashTxSizesAsync`](#class_bitprim_1_1_chain_1a16fbf9347d382e413596738050e477cc)`(byte [] blockHash)` 

Given a block hash, retrieve block header, tx hashes and serialized block size, asynchronously.

#### Parameters
* `blockHash` 32 bytes of the block hash

#### `public inline async Task< `[`ApiCallResult](#class_bitprim_1_1_api_call_result)< [GetBlockHashTimestampResult`](#class_bitprim_1_1_get_block_hash_timestamp_result)` > > `[`FetchBlockByHeightHashTimestampAsync`](#class_bitprim_1_1_chain_1a0ed827e80a50f6ef1537f4e3323161ec)`(UInt64 height)` 

Given a block height, retrieve only block hash and timestamp, asynchronously.

#### Parameters
* `height` [Block](#class_bitprim_1_1_block) height

#### `public inline async Task< `[`DisposableApiCallResult](#class_bitprim_1_1_disposable_api_call_result)< [GetBlockDataResult](#class_bitprim_1_1_get_block_data_result)< [Header`](#class_bitprim_1_1_header)` > > > `[`FetchBlockHeaderByHashAsync`](#class_bitprim_1_1_chain_1a481afe875fea3bed18fdcc5f34881d24)`(byte [] blockHash)` 

Given a block hash, get the header from the block it identifies, asynchronously.

#### Parameters
* `blockHash` 32 bytes of the block hash

#### `public inline async Task< `[`DisposableApiCallResult](#class_bitprim_1_1_disposable_api_call_result)< [GetBlockDataResult](#class_bitprim_1_1_get_block_data_result)< [Header`](#class_bitprim_1_1_header)` > > > `[`FetchBlockHeaderByHeightAsync`](#class_bitprim_1_1_chain_1af8dde319dada6e5fc337110280e7ecdf)`(UInt64 height)` 

Given a block height, get the header from the block it identifies, asynchronously.

#### Parameters
* `height` [Block](#class_bitprim_1_1_block) height

#### `public inline async Task< `[`DisposableApiCallResult](#class_bitprim_1_1_disposable_api_call_result)< [GetBlockDataResult](#class_bitprim_1_1_get_block_data_result)< [MerkleBlock`](#class_bitprim_1_1_merkle_block)` > > > `[`FetchMerkleBlockByHashAsync`](#class_bitprim_1_1_chain_1a3065a220899aa4e7499e00c82a986800)`(byte [] blockHash)` 

Given a block hash, get the merkle block from the block it identifies, asynchronously.

#### Parameters
* `blockHash` 32 bytes of the block hash

#### `public inline async Task< `[`DisposableApiCallResult](#class_bitprim_1_1_disposable_api_call_result)< [GetBlockDataResult](#class_bitprim_1_1_get_block_data_result)< [MerkleBlock`](#class_bitprim_1_1_merkle_block)` > > > `[`FetchMerkleBlockByHeightAsync`](#class_bitprim_1_1_chain_1a51960cb40096565cba29801ecef869ce)`(UInt64 height)` 

Given a block height, get the merkle block from the block it identifies, asynchronously.

#### Parameters
* `height` Desired block height

#### `public inline async Task< `[`DisposableApiCallResult](#class_bitprim_1_1_disposable_api_call_result)< [GetBlockDataResult`](#class_bitprim_1_1_get_block_data_result)`< CompactBlock > > > `[`FetchCompactBlockByHash`](#class_bitprim_1_1_chain_1a7d2a96a34f4db98b4bb95f0945c8eb91)`(byte [] blockHash)` 

Given a block hash, get the compact block from the block it identifies, asynchronously.

#### Parameters
* `blockHash` 32 bytes of the block hash

#### `public inline async Task< `[`DisposableApiCallResult](#class_bitprim_1_1_disposable_api_call_result)< [GetBlockDataResult`](#class_bitprim_1_1_get_block_data_result)`< CompactBlock > > > `[`FetchCompactBlockByHeightAsync`](#class_bitprim_1_1_chain_1ab44be34165be4cd968eecd0b8aa0daba)`(UInt64 height)` 

Given a block height, get the compact block from the block it identifies, asynchronously.

#### Parameters
* `height` Desired block height

#### `public inline async Task< `[`DisposableApiCallResult](#class_bitprim_1_1_disposable_api_call_result)< [GetTxDataResult`](#class_bitprim_1_1_get_tx_data_result)` > > `[`FetchTransactionAsync`](#class_bitprim_1_1_chain_1acd7a013b2d7dfb59a2be96c7e0fbe4ce)`(byte [] txHash,bool requireConfirmed)` 

Get a transaction by its hash, asynchronously.

#### Parameters
* `txHash` 32 bytes of transaction hash 

* `requireConfirmed` True if the transaction must belong to a block

#### `public inline async Task< `[`ApiCallResult](#class_bitprim_1_1_api_call_result)< [GetTxPositionResult`](#struct_bitprim_1_1_get_tx_position_result)` > > `[`FetchTransactionPositionAsync`](#class_bitprim_1_1_chain_1a5dc1c0c121540d6f3fcdac769e5dfcbb)`(byte [] txHash,bool requireConfirmed)` 

Given a transaction hash, it fetches the height and position inside the block, asynchronously.

#### Parameters
* `txHash` 32 bytes of transaction hash 

* `requireConfirmed` True iif the transaction must belong to a block

#### `public inline async Task< `[`ApiCallResult](#class_bitprim_1_1_api_call_result)< [Point`](#class_bitprim_1_1_point)` > > `[`FetchSpendAsync`](#class_bitprim_1_1_chain_1aa6f96700ac465dfb8899f8199c65a372)`(`[`OutputPoint`](#class_bitprim_1_1_output_point)` outputPoint)` 

Fetch the transaction input which spends the indicated output, asynchronously.

#### Parameters
* `outputPoint` Tx hash and index pair where the output was spent.

#### `public inline async Task< `[`DisposableApiCallResult`](#class_bitprim_1_1_disposable_api_call_result)`< HistoryCompactList > > `[`FetchHistoryAsync`](#class_bitprim_1_1_chain_1ab8077112761466c2e19eca51d3e5eadf)`(`[`PaymentAddress`](#class_bitprim_1_1_payment_address)` address,UInt64 limit,UInt64 fromHeight)` 

Get a list of output points, values, and spends for a given payment address (asynchronously)

#### Parameters
* `address` Bitcoin payment address to search 

* `limit` Maximum amount of results to fetch 

* `fromHeight` Starting point to search for transactions

#### `public inline async Task< `[`DisposableApiCallResult`](#class_bitprim_1_1_disposable_api_call_result)`< HashList > > `[`FetchConfirmedTransactionsAsync`](#class_bitprim_1_1_chain_1affd9881e0c675e1e3202b33c697043e8)`(`[`PaymentAddress`](#class_bitprim_1_1_payment_address)` address,UInt64 limit,UInt64 fromHeight)` 

Get a list of tx ids for a given payment address (asynchronously). Duplicates are already filtered out.

#### Parameters
* `address` Bitcoin payment address to search 

* `limit` Maximum amount of results to fetch 

* `fromHeight` Starting point to search for transactions

#### `public inline async Task< `[`DisposableApiCallResult`](#class_bitprim_1_1_disposable_api_call_result)`< StealthCompactList > > `[`FetchStealthAsync`](#class_bitprim_1_1_chain_1a9a39b99193848b3c051b8b4eb985e692)`(`[`Binary`](#class_bitprim_1_1_binary)` filter,UInt64 fromHeight)` 

Get metadata on potential payment transactions by stealth filter. Given a filter and a height in the chain, it queries the chain for transactions matching the given filter.

#### Parameters
* `filter` Must be at least 8 bits in length. example "10101010" 

* `fromHeight` Starting height in the chain to search for transactions

#### `public inline async Task< `[`DisposableApiCallResult](#class_bitprim_1_1_disposable_api_call_result)< [HeaderReader`](#class_bitprim_1_1_header_reader)` > > `[`FetchBlockLocatorAsync`](#class_bitprim_1_1_chain_1ab76ad8f4fecec65e9934c38288f23f56)`(BlockIndexList indexes)` 

Given a list of indexes, fetch a header reader for them, asynchronously

#### Parameters
* `indexes` [Block](#class_bitprim_1_1_block) indexes

#### `public inline async Task< ErrorCode > `[`OrganizeBlockAsync`](#class_bitprim_1_1_chain_1ac98d25baa15b37a77a48becca57c4968)`(`[`Block`](#class_bitprim_1_1_block)` block)` 

Given a block, organize it (async).

#### Parameters
* `block` The block to organize

#### `public inline async Task< ErrorCode > `[`OrganizeTransactionAsync`](#class_bitprim_1_1_chain_1a23be64a1bbec23574fd616edede37111)`(`[`Transaction`](#class_bitprim_1_1_transaction)` transaction)` 

Given a transaction, organize it (async).

#### Parameters
* `transaction` The transaction to organize.

#### `public inline async Task< `[`ApiCallResult`](#class_bitprim_1_1_api_call_result)`< string > > `[`ValidateTransactionAsync`](#class_bitprim_1_1_chain_1a233758a5d970628d399287a851795670)`(`[`Transaction`](#class_bitprim_1_1_transaction)` transaction)` 

Determine if a transaction is valid for submission to the blockchain.

#### Parameters
* `transaction` [Transaction](#class_bitprim_1_1_transaction) to validate

#### `public inline MempoolTransactionList `[`GetMempoolTransactions`](#class_bitprim_1_1_chain_1a44a0cd66999dde4914e1e013c582d731)`(`[`PaymentAddress`](#class_bitprim_1_1_payment_address)` address,bool useTestnetRules)` 

# class `Bitprim::DisposableApiCallResult` 

```
class Bitprim::DisposableApiCallResult
  : public IDisposable
```  

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`{property} ErrorCode `[`ErrorCode`](#class_bitprim_1_1_disposable_api_call_result_1abd6d0781149b4db77a1ef5ac3c2e167c) | 
`{property} TResultData `[`Result`](#class_bitprim_1_1_disposable_api_call_result_1ab1b9fdc66ec7701386eb7c81118a6dac) | 

## Members

#### `{property} ErrorCode `[`ErrorCode`](#class_bitprim_1_1_disposable_api_call_result_1abd6d0781149b4db77a1ef5ac3c2e167c) 

#### `{property} TResultData `[`Result`](#class_bitprim_1_1_disposable_api_call_result_1ab1b9fdc66ec7701386eb7c81118a6dac) 

# class `Bitprim::Executor` 

```
class Bitprim::Executor
  : public IDisposable
```  

Controls the execution of the [Bitprim](#namespace_bitprim) bitcoin node.

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`{property} bool `[`UseTestnetRules`](#class_bitprim_1_1_executor_1a72721235e276a2022424254285a89859) | Returns true iif the current network is a testnet.
`{property} `[`Chain`](#class_bitprim_1_1_chain)` `[`Chain`](#class_bitprim_1_1_executor_1ac610ccf2aeb37d042c6de111dc4af3d8) | The node's query interface. Will be null until node starts running (i.e. Run or RunWait succeeded)
`{property} NetworkType `[`NetworkType`](#class_bitprim_1_1_executor_1aaa0cd4c024e384cd8d0f99daebada6cd) | The node's network. Won't be valid until node starts running (i.e. Run or RunWait succeeded)
`{property} bool `[`IsStopped`](#class_bitprim_1_1_executor_1aa3d8e0c57065dc536ae997cf3d46340f) | 
`{property} bool `[`IsLoadConfigValid`](#class_bitprim_1_1_executor_1af8b481e884520c67c9d348c32f6adcbb) | 
`public delegate bool `[`BlockHandler`](#class_bitprim_1_1_executor_1aa8f3a08638a1c8a977c780be93c5cdf9)`(ErrorCode e,UInt64 u,BlockList incoming,BlockList outgoing)` | 
`public delegate bool `[`TransactionHandler`](#class_bitprim_1_1_executor_1af552875e00ecb97f9529b6892d5fa9ed)`(ErrorCode e,`[`Transaction`](#class_bitprim_1_1_transaction)` newTx)` | 
`public inline  `[`Executor`](#class_bitprim_1_1_executor_1ac689798a0303fa5e0b289b9601ff4a41)`(string configFile)` | Create executor. Does not init database or start execution yet.
`public inline  `[`Executor`](#class_bitprim_1_1_executor_1a4a0a051ca72a1c4ab9b6fa066bda67a2)`(string configFile,IntPtr stdOut,IntPtr stdErr)` | //TODO See BIT-20 Create executor. Does not init database or start execution yet.
`public inline bool `[`InitChain`](#class_bitprim_1_1_executor_1a92769f0858fea0b489e9fea5fc49ad07)`()` | Initialize the local dabatase structure.
`public inline async Task< int > `[`RunAsync`](#class_bitprim_1_1_executor_1afc33e022d6b52ce8cde9a87e1ab54240)`()` | Starts running the node; blockchain starts synchronizing (downloading). The call returns right away, and the handler is invoked when the node actually starts running.
`public inline async Task< int > `[`InitAndRunAsync`](#class_bitprim_1_1_executor_1a699476f37e539c6e3558a3204aa5a386)`()` | Initialize if necessary and starts running the node; blockchain starts synchronizing (downloading). The call returns right away, and the handler is invoked when the node actually starts running.
`public inline void `[`Stop`](#class_bitprim_1_1_executor_1aac496e7361d58efefee7c4e09784085a)`()` | Stops the node; that includes all activies, such as synchronization and networking.
`public inline void `[`SubscribeToBlockChain`](#class_bitprim_1_1_executor_1a644be84a2244121e0e9a487f63430ed3)`(BlockHandler handler)` | Be notified (called back) when the local copy of the blockchain is reorganized.
`public inline void `[`SubscribeToTransaction`](#class_bitprim_1_1_executor_1a7470933138440e5abdd12a3c26b2dcae)`(TransactionHandler handler)` | Be notified (called back) when the local copy of the blockchain is updated at the transaction level.

## Members

#### `{property} bool `[`UseTestnetRules`](#class_bitprim_1_1_executor_1a72721235e276a2022424254285a89859) 

Returns true iif the current network is a testnet.

#### `{property} `[`Chain`](#class_bitprim_1_1_chain)` `[`Chain`](#class_bitprim_1_1_executor_1ac610ccf2aeb37d042c6de111dc4af3d8) 

The node's query interface. Will be null until node starts running (i.e. Run or RunWait succeeded)

#### `{property} NetworkType `[`NetworkType`](#class_bitprim_1_1_executor_1aaa0cd4c024e384cd8d0f99daebada6cd) 

The node's network. Won't be valid until node starts running (i.e. Run or RunWait succeeded)

#### `{property} bool `[`IsStopped`](#class_bitprim_1_1_executor_1aa3d8e0c57065dc536ae997cf3d46340f) 

#### `{property} bool `[`IsLoadConfigValid`](#class_bitprim_1_1_executor_1af8b481e884520c67c9d348c32f6adcbb) 

#### `public delegate bool `[`BlockHandler`](#class_bitprim_1_1_executor_1aa8f3a08638a1c8a977c780be93c5cdf9)`(ErrorCode e,UInt64 u,BlockList incoming,BlockList outgoing)` 

#### `public delegate bool `[`TransactionHandler`](#class_bitprim_1_1_executor_1af552875e00ecb97f9529b6892d5fa9ed)`(ErrorCode e,`[`Transaction`](#class_bitprim_1_1_transaction)` newTx)` 

#### `public inline  `[`Executor`](#class_bitprim_1_1_executor_1ac689798a0303fa5e0b289b9601ff4a41)`(string configFile)` 

Create executor. Does not init database or start execution yet.

#### Parameters
* `configFile` Path to configuration file.

#### `public inline  `[`Executor`](#class_bitprim_1_1_executor_1a4a0a051ca72a1c4ab9b6fa066bda67a2)`(string configFile,IntPtr stdOut,IntPtr stdErr)` 

//TODO See BIT-20 Create executor. Does not init database or start execution yet.

#### Parameters
* `configFile` Path to configuration file. 

* `stdOut` File descriptor for redirecting standard output. 

* `stdErr` File descriptor for redirecting standard error output. 

Create executor. Does not init database or start execution yet. 

#### Parameters
* `configFile` Path to configuration file. 

* `stdOut` Handle for redirecting standard output. 

* `stdErr` Handle for redirecting standard output.

#### `public inline bool `[`InitChain`](#class_bitprim_1_1_executor_1a92769f0858fea0b489e9fea5fc49ad07)`()` 

Initialize the local dabatase structure.

#### Returns
True iif local chain init succeeded

#### `public inline async Task< int > `[`RunAsync`](#class_bitprim_1_1_executor_1afc33e022d6b52ce8cde9a87e1ab54240)`()` 

Starts running the node; blockchain starts synchronizing (downloading). The call returns right away, and the handler is invoked when the node actually starts running.

#### Returns
Error code (0 = success)

#### `public inline async Task< int > `[`InitAndRunAsync`](#class_bitprim_1_1_executor_1a699476f37e539c6e3558a3204aa5a386)`()` 

Initialize if necessary and starts running the node; blockchain starts synchronizing (downloading). The call returns right away, and the handler is invoked when the node actually starts running.

#### Returns
Error code (0 = success)

#### `public inline void `[`Stop`](#class_bitprim_1_1_executor_1aac496e7361d58efefee7c4e09784085a)`()` 

Stops the node; that includes all activies, such as synchronization and networking.

#### `public inline void `[`SubscribeToBlockChain`](#class_bitprim_1_1_executor_1a644be84a2244121e0e9a487f63430ed3)`(BlockHandler handler)` 

Be notified (called back) when the local copy of the blockchain is reorganized.

#### Parameters
* `handler` Callback which will be called when blocks are added or removed. The callback returns 3 parameters:

* Height (UInt64): The chain height at which reorganization takes place

* Incoming (Blocklist): Incoming blocks (added to the blockchain).

* Outgoing (Blocklist): Outgoing blocks (removed from the blockchain).

#### `public inline void `[`SubscribeToTransaction`](#class_bitprim_1_1_executor_1a7470933138440e5abdd12a3c26b2dcae)`(TransactionHandler handler)` 

Be notified (called back) when the local copy of the blockchain is updated at the transaction level.

#### Parameters
* `handler` Callback which will be called when a transaction is added.

# class `Bitprim::GetBlockDataResult` 

```
class Bitprim::GetBlockDataResult
  : public IDisposable
```  

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`{property} TBlockData `[`BlockData`](#class_bitprim_1_1_get_block_data_result_1a013cfb30f8e30d5be5060e3d4a76e8ae) | 
`public UInt64 `[`BlockHeight`](#class_bitprim_1_1_get_block_data_result_1a3e82b7c4369b77cbce73ee9a3706782c) | 

## Members

#### `{property} TBlockData `[`BlockData`](#class_bitprim_1_1_get_block_data_result_1a013cfb30f8e30d5be5060e3d4a76e8ae) 

#### `public UInt64 `[`BlockHeight`](#class_bitprim_1_1_get_block_data_result_1a3e82b7c4369b77cbce73ee9a3706782c) 

# class `Bitprim::GetBlockHashTimestampResult` 

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`{property} byte [] `[`BlockHash`](#class_bitprim_1_1_get_block_hash_timestamp_result_1a3127c5bd7f9a1933717fbb6776201686) | 
`{property} DateTime `[`BlockTimestamp`](#class_bitprim_1_1_get_block_hash_timestamp_result_1a6c1886de6a464b741711eb3652c06048) | 

## Members

#### `{property} byte [] `[`BlockHash`](#class_bitprim_1_1_get_block_hash_timestamp_result_1a3127c5bd7f9a1933717fbb6776201686) 

#### `{property} DateTime `[`BlockTimestamp`](#class_bitprim_1_1_get_block_hash_timestamp_result_1a6c1886de6a464b741711eb3652c06048) 

# class `Bitprim::GetBlockHeaderByHashTxSizeResult` 

```
class Bitprim::GetBlockHeaderByHashTxSizeResult
  : public IDisposable
```  

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`{property} `[`GetBlockDataResult](#class_bitprim_1_1_get_block_data_result)< [Header`](#class_bitprim_1_1_header)` > `[`Block`](#class_bitprim_1_1_get_block_header_by_hash_tx_size_result_1a97201cdcf7cf4749ef689702548487bb) | 
`{property} HashList `[`TransactionHashes`](#class_bitprim_1_1_get_block_header_by_hash_tx_size_result_1ab1345bebf999bf84b624d0f5e5056e33) | 
`{property} UInt64 `[`SerializedBlockSize`](#class_bitprim_1_1_get_block_header_by_hash_tx_size_result_1a5f31bf3c48d635040732b6a4d2137a9d) | 

## Members

#### `{property} `[`GetBlockDataResult](#class_bitprim_1_1_get_block_data_result)< [Header`](#class_bitprim_1_1_header)` > `[`Block`](#class_bitprim_1_1_get_block_header_by_hash_tx_size_result_1a97201cdcf7cf4749ef689702548487bb) 

#### `{property} HashList `[`TransactionHashes`](#class_bitprim_1_1_get_block_header_by_hash_tx_size_result_1ab1345bebf999bf84b624d0f5e5056e33) 

#### `{property} UInt64 `[`SerializedBlockSize`](#class_bitprim_1_1_get_block_header_by_hash_tx_size_result_1a5f31bf3c48d635040732b6a4d2137a9d) 

# class `Bitprim::GetTxDataResult` 

```
class Bitprim::GetTxDataResult
  : public IDisposable
```  

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`{property} `[`Transaction`](#class_bitprim_1_1_transaction)` `[`Tx`](#class_bitprim_1_1_get_tx_data_result_1a4f036251320b983dd69f1248d551f0ad) | 
`{property} `[`GetTxPositionResult`](#struct_bitprim_1_1_get_tx_position_result)` `[`TxPosition`](#class_bitprim_1_1_get_tx_data_result_1a949a8d7dd542949d78026f7c2aa4ec2d) | 

## Members

#### `{property} `[`Transaction`](#class_bitprim_1_1_transaction)` `[`Tx`](#class_bitprim_1_1_get_tx_data_result_1a4f036251320b983dd69f1248d551f0ad) 

#### `{property} `[`GetTxPositionResult`](#struct_bitprim_1_1_get_tx_position_result)` `[`TxPosition`](#class_bitprim_1_1_get_tx_data_result_1a949a8d7dd542949d78026f7c2aa4ec2d) 

# class `Bitprim::Header` 

```
class Bitprim::Header
  : public IDisposable
```  

Represents a full Bitcoin blockchain block.

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`{property} bool `[`IsValid`](#class_bitprim_1_1_header_1a8018db3ab9a37c742a0cc89cca654973) | Returns true if and only if the header conforms to the Bitcoin protocol format.
`{property} byte [] `[`Hash`](#class_bitprim_1_1_header_1a1d763bfd0a000b5b1d7a7285ffcd61d7) | [Block](#class_bitprim_1_1_block) hash in 32 byte array format.
`{property} byte [] `[`Merkle`](#class_bitprim_1_1_header_1a96282c190970dfc86a35294825d3c3e5) | Merkle root in 32 byte array format.
`{property} byte [] `[`PreviousBlockHash`](#class_bitprim_1_1_header_1aa48ea17b65f4177086ab174233c9ad1a) | Hash belonging to the immediately previous block in the blockchain, as a 32 byte array. This is all zeros for the first block, a.k.a. Genesis.
`{property} string `[`ProofString`](#class_bitprim_1_1_header_1a1756a2bc8e312654ad8f02e917db5045) | Hexadecimal string representation of the block's proof (which is a 256-bit number).
`{property} UInt32 `[`Bits`](#class_bitprim_1_1_header_1afacb1dc4ac2169c218801dc54cad37ca) | Difficulty threshold.
`{property} UInt32 `[`Nonce`](#class_bitprim_1_1_header_1ac6a6f369a44e845082240ddd86f202d9) | The nonce that allowed this block to be added to the blockchain.
`{property} UInt32 `[`Timestamp`](#class_bitprim_1_1_header_1a745d573ec4c70b1a67fca156faca6dfa) | [Block](#class_bitprim_1_1_block) timestamp in UNIX Epoch format (seconds since January 1st 1970) Assume UTC 0.
`{property} UInt32 `[`Version`](#class_bitprim_1_1_header_1a9189d2afec1ba7d21f10aa776d3ac490) | [Header](#class_bitprim_1_1_header) protocol version.

## Members

#### `{property} bool `[`IsValid`](#class_bitprim_1_1_header_1a8018db3ab9a37c742a0cc89cca654973) 

Returns true if and only if the header conforms to the Bitcoin protocol format.

#### `{property} byte [] `[`Hash`](#class_bitprim_1_1_header_1a1d763bfd0a000b5b1d7a7285ffcd61d7) 

[Block](#class_bitprim_1_1_block) hash in 32 byte array format.

#### `{property} byte [] `[`Merkle`](#class_bitprim_1_1_header_1a96282c190970dfc86a35294825d3c3e5) 

Merkle root in 32 byte array format.

#### `{property} byte [] `[`PreviousBlockHash`](#class_bitprim_1_1_header_1aa48ea17b65f4177086ab174233c9ad1a) 

Hash belonging to the immediately previous block in the blockchain, as a 32 byte array. This is all zeros for the first block, a.k.a. Genesis.

#### `{property} string `[`ProofString`](#class_bitprim_1_1_header_1a1756a2bc8e312654ad8f02e917db5045) 

Hexadecimal string representation of the block's proof (which is a 256-bit number).

#### `{property} UInt32 `[`Bits`](#class_bitprim_1_1_header_1afacb1dc4ac2169c218801dc54cad37ca) 

Difficulty threshold.

#### `{property} UInt32 `[`Nonce`](#class_bitprim_1_1_header_1ac6a6f369a44e845082240ddd86f202d9) 

The nonce that allowed this block to be added to the blockchain.

#### `{property} UInt32 `[`Timestamp`](#class_bitprim_1_1_header_1a745d573ec4c70b1a67fca156faca6dfa) 

[Block](#class_bitprim_1_1_block) timestamp in UNIX Epoch format (seconds since January 1st 1970) Assume UTC 0.

#### `{property} UInt32 `[`Version`](#class_bitprim_1_1_header_1a9189d2afec1ba7d21f10aa776d3ac490) 

[Header](#class_bitprim_1_1_header) protocol version.

# class `Bitprim::HeaderReader` 

```
class Bitprim::HeaderReader
  : public IDisposable
```  

Helper for reading the header for each block in a specific set of blocks.

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`{property} bool `[`IsValid`](#class_bitprim_1_1_header_reader_1a3471f7b55cfb7695d79ca8e13cfcf0a0) | The block set is valid iif all its blocks are valid.
`{property} byte [] `[`StopHash`](#class_bitprim_1_1_header_reader_1a98cbc6c314c8ddb5472916b7fbefc4f7) | Stop at this block (include it in the set).
`{property} HashList `[`StartHashes`](#class_bitprim_1_1_header_reader_1a6f8d968aae0e6240dffbc554a2e8ba82) | Define when to start reading: Once these blocks are synced (include the newest one).
`public inline  `[`HeaderReader`](#class_bitprim_1_1_header_reader_1aa4b325abd6a521e1949edea884778052)`()` | Create an empty reader.
`public inline  `[`HeaderReader`](#class_bitprim_1_1_header_reader_1a2eee57e87b2ea5e3f609f949c71a707e)`(HashList start,byte [] stop)` | Create a reader with predefined start hashes and stop hash.
`public inline UInt64 `[`GetSerializedSize`](#class_bitprim_1_1_header_reader_1a77e3422d9b7b76a956924c3611e6e989)`(UInt32 version)` | The sum of the header sizes for this set.
`public inline void `[`Reset`](#class_bitprim_1_1_header_reader_1aa60467a083c4867ec266e611f13c580e)`()` | Go back to first block in the set.

## Members

#### `{property} bool `[`IsValid`](#class_bitprim_1_1_header_reader_1a3471f7b55cfb7695d79ca8e13cfcf0a0) 

The block set is valid iif all its blocks are valid.

#### `{property} byte [] `[`StopHash`](#class_bitprim_1_1_header_reader_1a98cbc6c314c8ddb5472916b7fbefc4f7) 

Stop at this block (include it in the set).

#### `{property} HashList `[`StartHashes`](#class_bitprim_1_1_header_reader_1a6f8d968aae0e6240dffbc554a2e8ba82) 

Define when to start reading: Once these blocks are synced (include the newest one).

#### `public inline  `[`HeaderReader`](#class_bitprim_1_1_header_reader_1aa4b325abd6a521e1949edea884778052)`()` 

Create an empty reader.

#### `public inline  `[`HeaderReader`](#class_bitprim_1_1_header_reader_1a2eee57e87b2ea5e3f609f949c71a707e)`(HashList start,byte [] stop)` 

Create a reader with predefined start hashes and stop hash.

#### Parameters
* `start` When all of these blocks are synced, start reading. 

* `stop` Stop at this block.

#### `public inline UInt64 `[`GetSerializedSize`](#class_bitprim_1_1_header_reader_1a77e3422d9b7b76a956924c3611e6e989)`(UInt32 version)` 

The sum of the header sizes for this set.

#### Parameters
* `version` Protocol version to consider when calculating header size. 

#### Returns
Sum of header sizes.

#### `public inline void `[`Reset`](#class_bitprim_1_1_header_reader_1aa60467a083c4867ec266e611f13c580e)`()` 

Go back to first block in the set.

# class `Bitprim::HistoryCompact` 

```
class Bitprim::HistoryCompact
  : public IDisposable
```  

[Output](#class_bitprim_1_1_output) points, values, and spends for a payment address.

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`{property} `[`Point`](#class_bitprim_1_1_point)` `[`Point`](#class_bitprim_1_1_history_compact_1a5f18863c354bf692f1fe325b311654b0) | The point that identifies the History instance.
`{property} UInt32 `[`Height`](#class_bitprim_1_1_history_compact_1a41e320774dfb5a2ecb0d6c8617087d06) | Height of the block containing the [Point](#class_bitprim_1_1_point).
`{property} UInt64 `[`ValueOrChecksum`](#class_bitprim_1_1_history_compact_1ad00b564aafa4f603347d6e387bc654a6) | Varies depending on point_kind.

## Members

#### `{property} `[`Point`](#class_bitprim_1_1_point)` `[`Point`](#class_bitprim_1_1_history_compact_1a5f18863c354bf692f1fe325b311654b0) 

The point that identifies the History instance.

#### `{property} UInt32 `[`Height`](#class_bitprim_1_1_history_compact_1a41e320774dfb5a2ecb0d6c8617087d06) 

Height of the block containing the [Point](#class_bitprim_1_1_point).

#### `{property} UInt64 `[`ValueOrChecksum`](#class_bitprim_1_1_history_compact_1ad00b564aafa4f603347d6e387bc654a6) 

Varies depending on point_kind.

# class `Bitprim::Input` 

```
class Bitprim::Input
  : public IDisposable
```  

Represents a [Transaction](#class_bitprim_1_1_transaction) input.

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`{property} bool `[`IsFinal`](#class_bitprim_1_1_input_1a51424ae4e6979cced244ba27bf563644) | Returns 1 iif sequence is equal to max_sequence.
`{property} bool `[`IsValid`](#class_bitprim_1_1_input_1aa45cc1562e08b08903f0c49af101edaf) | Returns false if and only if previous outputs or input script are invalid.
`{property} `[`OutputPoint`](#class_bitprim_1_1_output_point)` `[`PreviousOutput`](#class_bitprim_1_1_input_1a047409c5f428227e0aa235a2a8b85687) | Returns a reference to the previous output, as an [OutputPoint](#class_bitprim_1_1_output_point): a transaction hash and index pair.
`{property} `[`Script`](#class_bitprim_1_1_script)` `[`Script`](#class_bitprim_1_1_input_1a33808f7bd1eac8590448bebe1d7ddbde) | The input's script.
`{property} UInt32 `[`Sequence`](#class_bitprim_1_1_input_1ad4a1d451642e545c15a8d842092e5815) | Zero-based index for the input in the transaction's input set.
`{property} IntPtr `[`NativeInstance`](#class_bitprim_1_1_input_1a265f01ce48cb932e89306bae4f9d2835) | 
`public inline  `[`Input`](#class_bitprim_1_1_input_1a978df7845edc1c18e44cc7f9e9ad0ee4)`()` | Create an empty input.
`public inline  `[`Input`](#class_bitprim_1_1_input_1a6e5b9353656c7e4d94f3645e674e0442)`(`[`Output`](#class_bitprim_1_1_output)` previousOutput,`[`Script`](#class_bitprim_1_1_script)` script,UInt32 sequence)` | Create an input from a previous output, a script and a sequence number.
`public inline UInt64 `[`GetSerializedSize`](#class_bitprim_1_1_input_1af185363b5b7723afd29117dc629e55c0)`(bool wire)` | [Input](#class_bitprim_1_1_input) size in bytes.
`public inline UInt64 `[`GetSignatureOperationsCount`](#class_bitprim_1_1_input_1a7f34e170a185bda655ef1df84ec38b92)`(bool bip16Active)` | Total amount of sigops (signature operations) in the input script.

## Members

#### `{property} bool `[`IsFinal`](#class_bitprim_1_1_input_1a51424ae4e6979cced244ba27bf563644) 

Returns 1 iif sequence is equal to max_sequence.

#### `{property} bool `[`IsValid`](#class_bitprim_1_1_input_1aa45cc1562e08b08903f0c49af101edaf) 

Returns false if and only if previous outputs or input script are invalid.

#### `{property} `[`OutputPoint`](#class_bitprim_1_1_output_point)` `[`PreviousOutput`](#class_bitprim_1_1_input_1a047409c5f428227e0aa235a2a8b85687) 

Returns a reference to the previous output, as an [OutputPoint](#class_bitprim_1_1_output_point): a transaction hash and index pair.

#### `{property} `[`Script`](#class_bitprim_1_1_script)` `[`Script`](#class_bitprim_1_1_input_1a33808f7bd1eac8590448bebe1d7ddbde) 

The input's script.

#### `{property} UInt32 `[`Sequence`](#class_bitprim_1_1_input_1ad4a1d451642e545c15a8d842092e5815) 

Zero-based index for the input in the transaction's input set.

#### `{property} IntPtr `[`NativeInstance`](#class_bitprim_1_1_input_1a265f01ce48cb932e89306bae4f9d2835) 

#### `public inline  `[`Input`](#class_bitprim_1_1_input_1a978df7845edc1c18e44cc7f9e9ad0ee4)`()` 

Create an empty input.

#### `public inline  `[`Input`](#class_bitprim_1_1_input_1a6e5b9353656c7e4d94f3645e674e0442)`(`[`Output`](#class_bitprim_1_1_output)` previousOutput,`[`Script`](#class_bitprim_1_1_script)` script,UInt32 sequence)` 

Create an input from a previous output, a script and a sequence number.

#### Parameters
* `previousOutput` The output to spend. 

* `script` [Input](#class_bitprim_1_1_input) script. 

* `sequence` Zero-based, indexes this input in the input set.

#### `public inline UInt64 `[`GetSerializedSize`](#class_bitprim_1_1_input_1af185363b5b7723afd29117dc629e55c0)`(bool wire)` 

[Input](#class_bitprim_1_1_input) size in bytes.

#### Parameters
* `wire` Iif true, consider 4 extra bytes from wire field. 

#### Returns
Size in bytes.

#### `public inline UInt64 `[`GetSignatureOperationsCount`](#class_bitprim_1_1_input_1a7f34e170a185bda655ef1df84ec38b92)`(bool bip16Active)` 

Total amount of sigops (signature operations) in the input script.

#### Parameters
* `bip16Active` Iif true, count BIP 16 active sig ops

#### Returns
Sigops count.

# class `Bitprim::MempoolTransaction` 

Represents an unconfirmed transaction.

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`{property} string `[`Address`](#class_bitprim_1_1_mempool_transaction_1a61e4bbd9d8201c7ac14eb7a1f48350c1) | [Transaction](#class_bitprim_1_1_transaction) output address
`{property} string `[`Hash`](#class_bitprim_1_1_mempool_transaction_1aef304d5e820d9162a034c6efbd96f5e8) | [Transaction](#class_bitprim_1_1_transaction) hash (unique identifier)
`{property} string `[`PreviousOutputHash`](#class_bitprim_1_1_mempool_transaction_1a76cbffed7754634acee9ed314f5915ea) | Previous output transaction hash
`{property} string `[`PreviousOutputIndex`](#class_bitprim_1_1_mempool_transaction_1a5f31bb697115574c6c095145bd6479a2) | Previous output transaction index
`{property} string `[`Satoshis`](#class_bitprim_1_1_mempool_transaction_1a1235a85eaeb1c61f6e6ac09f7bd8dcc3) | Sum of output values in Satoshis
`{property} UInt64 `[`Index`](#class_bitprim_1_1_mempool_transaction_1a60b3549786221cc6e08492d430c0f132) | [Transaction](#class_bitprim_1_1_transaction) index
`{property} UInt64 `[`Timestamp`](#class_bitprim_1_1_mempool_transaction_1aa8aad1f71eae1b4f05594b037f8963af) | [Transaction](#class_bitprim_1_1_transaction) timestamp
`{property} IntPtr `[`NativeInstance`](#class_bitprim_1_1_mempool_transaction_1ac262d612648d499a6cb123667560eece) | 

## Members

#### `{property} string `[`Address`](#class_bitprim_1_1_mempool_transaction_1a61e4bbd9d8201c7ac14eb7a1f48350c1) 

[Transaction](#class_bitprim_1_1_transaction) output address

#### `{property} string `[`Hash`](#class_bitprim_1_1_mempool_transaction_1aef304d5e820d9162a034c6efbd96f5e8) 

[Transaction](#class_bitprim_1_1_transaction) hash (unique identifier)

#### `{property} string `[`PreviousOutputHash`](#class_bitprim_1_1_mempool_transaction_1a76cbffed7754634acee9ed314f5915ea) 

Previous output transaction hash

#### `{property} string `[`PreviousOutputIndex`](#class_bitprim_1_1_mempool_transaction_1a5f31bb697115574c6c095145bd6479a2) 

Previous output transaction index

#### `{property} string `[`Satoshis`](#class_bitprim_1_1_mempool_transaction_1a1235a85eaeb1c61f6e6ac09f7bd8dcc3) 

Sum of output values in Satoshis

#### `{property} UInt64 `[`Index`](#class_bitprim_1_1_mempool_transaction_1a60b3549786221cc6e08492d430c0f132) 

[Transaction](#class_bitprim_1_1_transaction) index

#### `{property} UInt64 `[`Timestamp`](#class_bitprim_1_1_mempool_transaction_1aa8aad1f71eae1b4f05594b037f8963af) 

[Transaction](#class_bitprim_1_1_transaction) timestamp

#### `{property} IntPtr `[`NativeInstance`](#class_bitprim_1_1_mempool_transaction_1ac262d612648d499a6cb123667560eece) 

# class `Bitprim::MerkleBlock` 

```
class Bitprim::MerkleBlock
  : public IDisposable
```  

Merkle tree representation of a blockchain block.

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`{property} bool `[`IsValid`](#class_bitprim_1_1_merkle_block_1af1579794d62800b1e7712c7eeb5400c3) | Returns true if and only if it the block contains txs hashes, and the header is valid.
`{property} `[`Header`](#class_bitprim_1_1_header)` `[`Header`](#class_bitprim_1_1_merkle_block_1a56bf0f704c9ba7e474922b1a2fc18f0b) | The block's header.
`{property} UInt64 `[`HashCount`](#class_bitprim_1_1_merkle_block_1a9d489bfd505f89564069460ae835cca6) | [Transaction](#class_bitprim_1_1_transaction) hashes list element count.
`{property} UInt64 `[`TotalTransactionCount`](#class_bitprim_1_1_merkle_block_1a91fc331d0290c174dd4609d5231e3df6) | Amount of transactions inside the block.
`public inline byte [] `[`GetNthHash`](#class_bitprim_1_1_merkle_block_1a787be0b2fd6fc5f291c0e425ae2c2b67)`(int n)` | Get the Nth transaction hash from the block.
`public inline UInt64 `[`GetSerializedSize`](#class_bitprim_1_1_merkle_block_1af770044cf3e054454d56cc4cd85765d0)`(UInt32 version)` | [Block](#class_bitprim_1_1_block) size in bytes (as a Merkle block, not as a full block).
`public inline void `[`Reset`](#class_bitprim_1_1_merkle_block_1aa98bfea570cfd6816d98559421d3f505)`()` | Delete all the data inside the block.

## Members

#### `{property} bool `[`IsValid`](#class_bitprim_1_1_merkle_block_1af1579794d62800b1e7712c7eeb5400c3) 

Returns true if and only if it the block contains txs hashes, and the header is valid.

#### `{property} `[`Header`](#class_bitprim_1_1_header)` `[`Header`](#class_bitprim_1_1_merkle_block_1a56bf0f704c9ba7e474922b1a2fc18f0b) 

The block's header.

#### `{property} UInt64 `[`HashCount`](#class_bitprim_1_1_merkle_block_1a9d489bfd505f89564069460ae835cca6) 

[Transaction](#class_bitprim_1_1_transaction) hashes list element count.

#### `{property} UInt64 `[`TotalTransactionCount`](#class_bitprim_1_1_merkle_block_1a91fc331d0290c174dd4609d5231e3df6) 

Amount of transactions inside the block.

#### `public inline byte [] `[`GetNthHash`](#class_bitprim_1_1_merkle_block_1a787be0b2fd6fc5f291c0e425ae2c2b67)`(int n)` 

Get the Nth transaction hash from the block.

#### Parameters
* `n` Zerp-based index.

#### Returns
[Transaction](#class_bitprim_1_1_transaction) hash in 32 byte array format.

#### `public inline UInt64 `[`GetSerializedSize`](#class_bitprim_1_1_merkle_block_1af770044cf3e054454d56cc4cd85765d0)`(UInt32 version)` 

[Block](#class_bitprim_1_1_block) size in bytes (as a Merkle block, not as a full block).

#### Parameters
* `version` Protocol version to consider when calculating size. 

#### Returns
Size in bytes.

#### `public inline void `[`Reset`](#class_bitprim_1_1_merkle_block_1aa98bfea570cfd6816d98559421d3f505)`()` 

Delete all the data inside the block.

# class `Bitprim::NativeBuffer` 

```
class Bitprim::NativeBuffer
  : public IDisposable
```  

RAII wrapper for native memory. Guarantees that even if an exception is thrown, platform_free will be used to release it. Also, it prevents the user from forgetting to call platform_free.

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`{property} IntPtr `[`NativePtr`](#class_bitprim_1_1_native_buffer_1af5e2a12866803d63e6ebce17391ed1e7) | 
`public inline  `[`NativeBuffer`](#class_bitprim_1_1_native_buffer_1a2858b61a12dd4a344055291a9ce947ae)`(IntPtr nativePtr)` | 
`public inline byte [] `[`CopyToManagedArray`](#class_bitprim_1_1_native_buffer_1a20edd41586cd1a5582fd4e2ba48cce75)`(int arraySize)` | 

## Members

#### `{property} IntPtr `[`NativePtr`](#class_bitprim_1_1_native_buffer_1af5e2a12866803d63e6ebce17391ed1e7) 

#### `public inline  `[`NativeBuffer`](#class_bitprim_1_1_native_buffer_1a2858b61a12dd4a344055291a9ce947ae)`(IntPtr nativePtr)` 

#### `public inline byte [] `[`CopyToManagedArray`](#class_bitprim_1_1_native_buffer_1a20edd41586cd1a5582fd4e2ba48cce75)`(int arraySize)` 

# class `Bitprim::NativeString` 

```
class Bitprim::NativeString
  : public Bitprim.NativeBuffer
```  

RAII wrapper for native strings. Guarantees that even if an exception is thrown, platform_free will be used to release the native memory. Also, it prevents the user from forgetting to call platform_free.

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public inline  `[`NativeString`](#class_bitprim_1_1_native_string_1a2cf067d18afd3c84006f77ca4089dc0b)`(IntPtr nativePtr)` | 
`public override string `[`ToString`](#class_bitprim_1_1_native_string_1ad8b8bfd580eb2ef8789fcbb2dd72d201)`()` | 

## Members

#### `public inline  `[`NativeString`](#class_bitprim_1_1_native_string_1a2cf067d18afd3c84006f77ca4089dc0b)`(IntPtr nativePtr)` 

#### `public override string `[`ToString`](#class_bitprim_1_1_native_string_1ad8b8bfd580eb2ef8789fcbb2dd72d201)`()` 

# class `Bitprim::NodeSettings` 

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`{property} CurrencyType `[`CurrencyType`](#class_bitprim_1_1_node_settings_1afca824023b908da53cbbfd01b1dca4fc) | 

## Members

#### `{property} CurrencyType `[`CurrencyType`](#class_bitprim_1_1_node_settings_1afca824023b908da53cbbfd01b1dca4fc) 

# class `Bitprim::Output` 

```
class Bitprim::Output
  : public IDisposable
```  

Represents one of the outputs of a [Transaction](#class_bitprim_1_1_transaction).

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`{property} bool `[`IsValid`](#class_bitprim_1_1_output_1a787e7f1f897f2970c666808dc10b2e18) | Returns false if and only if output is not found.
`{property} `[`Script`](#class_bitprim_1_1_script)` `[`Script`](#class_bitprim_1_1_output_1a482ee34dee529ef3751f57b376967099) | [Output](#class_bitprim_1_1_output) script.
`{property} UInt64 `[`Value`](#class_bitprim_1_1_output_1a6d99343413e43c096df4e8b36e04a70d) | Spend, in Satoshis.
`{property} UInt64 `[`SignatureOperationCount`](#class_bitprim_1_1_output_1a82549fe1b06952db62aee4bbfa52dc0f) | The amount of signature operations in the output script.
`{property} IntPtr `[`NativeInstance`](#class_bitprim_1_1_output_1ad4d9c3eb131262fba8e97687f4c08b6a) | 
`public inline  `[`Output`](#class_bitprim_1_1_output_1aaa64429487aec9a987c5b944a9bed5d6)`()` | Create an empty output.
`public inline  `[`Output`](#class_bitprim_1_1_output_1a2550a08df3ed832691624537845c114e)`(UInt64 value,`[`Script`](#class_bitprim_1_1_script)` script)` | Create an output from a value and a script.
`public inline `[`PaymentAddress`](#class_bitprim_1_1_payment_address)` `[`PaymentAddress`](#class_bitprim_1_1_output_1aad82ee12e358b7c75cedfbd7f868b918)`(bool useTestnetRules)` | 
`public inline UInt64 `[`GetSerializedSize`](#class_bitprim_1_1_output_1a4b88b89c3080b561fda08264cc170918)`(bool wire)` | [Output](#class_bitprim_1_1_output) size in bytes.

## Members

#### `{property} bool `[`IsValid`](#class_bitprim_1_1_output_1a787e7f1f897f2970c666808dc10b2e18) 

Returns false if and only if output is not found.

#### `{property} `[`Script`](#class_bitprim_1_1_script)` `[`Script`](#class_bitprim_1_1_output_1a482ee34dee529ef3751f57b376967099) 

[Output](#class_bitprim_1_1_output) script.

#### `{property} UInt64 `[`Value`](#class_bitprim_1_1_output_1a6d99343413e43c096df4e8b36e04a70d) 

Spend, in Satoshis.

#### `{property} UInt64 `[`SignatureOperationCount`](#class_bitprim_1_1_output_1a82549fe1b06952db62aee4bbfa52dc0f) 

The amount of signature operations in the output script.

#### `{property} IntPtr `[`NativeInstance`](#class_bitprim_1_1_output_1ad4d9c3eb131262fba8e97687f4c08b6a) 

#### `public inline  `[`Output`](#class_bitprim_1_1_output_1aaa64429487aec9a987c5b944a9bed5d6)`()` 

Create an empty output.

#### `public inline  `[`Output`](#class_bitprim_1_1_output_1a2550a08df3ed832691624537845c114e)`(UInt64 value,`[`Script`](#class_bitprim_1_1_script)` script)` 

Create an output from a value and a script.

#### Parameters
* `value` In Satoshis. 

* `script` [Output](#class_bitprim_1_1_output) script.

#### `public inline `[`PaymentAddress`](#class_bitprim_1_1_payment_address)` `[`PaymentAddress`](#class_bitprim_1_1_output_1aad82ee12e358b7c75cedfbd7f868b918)`(bool useTestnetRules)` 

#### `public inline UInt64 `[`GetSerializedSize`](#class_bitprim_1_1_output_1a4b88b89c3080b561fda08264cc170918)`(bool wire)` 

[Output](#class_bitprim_1_1_output) size in bytes.

#### Parameters
* `wire` If true, size will include size of 'uint32' for storing spender height. 

#### Returns
Size in bytes.

# class `Bitprim::OutputPoint` 

```
class Bitprim::OutputPoint
  : public IDisposable
```  

[Transaction](#class_bitprim_1_1_transaction) hash and index pair representing one of the transaction outputs.

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`{property} byte [] `[`Hash`](#class_bitprim_1_1_output_point_1a633f597c1dc5978be3fa61442ecf1304) | [Transaction](#class_bitprim_1_1_transaction) hash in 32 byte array format.
`{property} UInt32 `[`Index`](#class_bitprim_1_1_output_point_1a599509fe9e21990c4fa6c3e7ac132e01) | [Transaction](#class_bitprim_1_1_transaction) index (zero-based).
`{property} IntPtr `[`NativeInstance`](#class_bitprim_1_1_output_point_1a0d223bbc27f0813aae961639d04fa0b1) | 
`public inline  `[`OutputPoint`](#class_bitprim_1_1_output_point_1a8a7e0600afba5d8588044c43313ef839)`()` | Create an empty output point.
`public inline  `[`OutputPoint`](#class_bitprim_1_1_output_point_1ac8741426c93c781a0aefc96c97d229dd)`(byte [] pointHash,UInt32 index)` | Create an output point from a hash and index pair.

## Members

#### `{property} byte [] `[`Hash`](#class_bitprim_1_1_output_point_1a633f597c1dc5978be3fa61442ecf1304) 

[Transaction](#class_bitprim_1_1_transaction) hash in 32 byte array format.

#### `{property} UInt32 `[`Index`](#class_bitprim_1_1_output_point_1a599509fe9e21990c4fa6c3e7ac132e01) 

[Transaction](#class_bitprim_1_1_transaction) index (zero-based).

#### `{property} IntPtr `[`NativeInstance`](#class_bitprim_1_1_output_point_1a0d223bbc27f0813aae961639d04fa0b1) 

#### `public inline  `[`OutputPoint`](#class_bitprim_1_1_output_point_1a8a7e0600afba5d8588044c43313ef839)`()` 

Create an empty output point.

#### `public inline  `[`OutputPoint`](#class_bitprim_1_1_output_point_1ac8741426c93c781a0aefc96c97d229dd)`(byte [] pointHash,UInt32 index)` 

Create an output point from a hash and index pair.

#### Parameters
* `pointHash` 
* `index`

# class `Bitprim::PaymentAddress` 

```
class Bitprim::PaymentAddress
  : public IDisposable
```  

Represents a Bitcoin wallet address.

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`{property} bool `[`IsValid`](#class_bitprim_1_1_payment_address_1a820450637d2e497dffc15f6e6905cce6) | Returns true iif this is a valid Base58 address.
`{property} byte `[`Version`](#class_bitprim_1_1_payment_address_1ad785a31e82e3260d29a238856bfee4bd) | Address version.
`{property} string `[`Encoded`](#class_bitprim_1_1_payment_address_1ab01d95e4aa1c7bd59e4817dca4dc0888) | Human readable representation.
`{property} IntPtr `[`NativeInstance`](#class_bitprim_1_1_payment_address_1a7613293266b7839dea0b8c6d86aa8002) | 
`public inline  `[`PaymentAddress`](#class_bitprim_1_1_payment_address_1ac7aba66544c8e97f631bbfa70983162e)`(string hexString)` | Create an address from its hex string representation.

## Members

#### `{property} bool `[`IsValid`](#class_bitprim_1_1_payment_address_1a820450637d2e497dffc15f6e6905cce6) 

Returns true iif this is a valid Base58 address.

#### `{property} byte `[`Version`](#class_bitprim_1_1_payment_address_1ad785a31e82e3260d29a238856bfee4bd) 

Address version.

#### `{property} string `[`Encoded`](#class_bitprim_1_1_payment_address_1ab01d95e4aa1c7bd59e4817dca4dc0888) 

Human readable representation.

#### `{property} IntPtr `[`NativeInstance`](#class_bitprim_1_1_payment_address_1a7613293266b7839dea0b8c6d86aa8002) 

#### `public inline  `[`PaymentAddress`](#class_bitprim_1_1_payment_address_1ac7aba66544c8e97f631bbfa70983162e)`(string hexString)` 

Create an address from its hex string representation.

#### Parameters
* `hexString`

# class `Bitprim::Point` 

Represents one of the transaction inputs. It's a transaction hash and index pair.

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`{property} bool `[`IsValid`](#class_bitprim_1_1_point_1adefc84e6edb7fa3725f2180f544f180b) | Returns true if and only if this point is not null.
`{property} byte [] `[`Hash`](#class_bitprim_1_1_point_1a867ca6d798e69ab40d29cf493cf4143a) | [Transaction](#class_bitprim_1_1_transaction) hash in 32 byte array format.
`{property} UInt32 `[`Index`](#class_bitprim_1_1_point_1a4ede31b4009d9671bd2177c1fbe7104a) | [Input](#class_bitprim_1_1_input) position in the transaction (zero-based).
`{property} UInt64 `[`Checksum`](#class_bitprim_1_1_point_1aaf47ce470cbe1d9c1aea175757cdf623) | This is used with [OutputPoint](#class_bitprim_1_1_output_point) identification within a set of history rows of the same address.
`{property} IntPtr `[`NativeInstance`](#class_bitprim_1_1_point_1a8017dde6032feadab8acc32a7691cdd0) | 

## Members

#### `{property} bool `[`IsValid`](#class_bitprim_1_1_point_1adefc84e6edb7fa3725f2180f544f180b) 

Returns true if and only if this point is not null.

#### `{property} byte [] `[`Hash`](#class_bitprim_1_1_point_1a867ca6d798e69ab40d29cf493cf4143a) 

[Transaction](#class_bitprim_1_1_transaction) hash in 32 byte array format.

#### `{property} UInt32 `[`Index`](#class_bitprim_1_1_point_1a4ede31b4009d9671bd2177c1fbe7104a) 

[Input](#class_bitprim_1_1_input) position in the transaction (zero-based).

#### `{property} UInt64 `[`Checksum`](#class_bitprim_1_1_point_1aaf47ce470cbe1d9c1aea175757cdf623) 

This is used with [OutputPoint](#class_bitprim_1_1_output_point) identification within a set of history rows of the same address.

#### `{property} IntPtr `[`NativeInstance`](#class_bitprim_1_1_point_1a8017dde6032feadab8acc32a7691cdd0) 

# class `Bitprim::Script` 

```
class Bitprim::Script
  : public IDisposable
```  

Represents a transaction script.

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`{property} bool `[`IsValid`](#class_bitprim_1_1_script_1aa6762b4acd4945c1b648ddd55802a430) | All script bytes are valid under some circumstance (e.g. coinbase).
`{property} bool `[`OperationsAreValid`](#class_bitprim_1_1_script_1a3047f3d01ea8e30a429c2004ae20e500) | [Script](#class_bitprim_1_1_script) validity is independent of individual operation validity. Operations are considered invalid if there is a trailing invalid/default op or if a push op has a size mismatch.
`{property} string `[`Type`](#class_bitprim_1_1_script_1ac3c48921a18d3864acbdf6937a8724a6) | [Script](#class_bitprim_1_1_script) type
`{property} UInt64 `[`SatoshiContentSize`](#class_bitprim_1_1_script_1a73ee4ba9eb69e6caae61756fd995427b) | Size in bytes.
`{property} IntPtr `[`NativeInstance`](#class_bitprim_1_1_script_1a1532f7d9458f9766de2fc79a8213d1f9) | 
`public inline byte [] `[`ToData`](#class_bitprim_1_1_script_1a51e7a2f14655e6431b21e39f7abedfa8)`(bool prefix)` | Raw script data
`public inline string `[`ToString`](#class_bitprim_1_1_script_1a7230eca6520c7b466e50ba9cdacf52c4)`(UInt32 activeForks)` | Translate operations in the script to a string.
`public inline UInt64 `[`GetEmbeddedSigOps`](#class_bitprim_1_1_script_1a41f6fc1d3554e6e0736eeb0e5622b89f)`(`[`Script`](#class_bitprim_1_1_script)` prevOutScript)` | Count the sigops in the embedded script using BIP16 rules.
`public inline UInt64 `[`GetSigOps`](#class_bitprim_1_1_script_1a9d37fa88a73f37692b612697fb327066)`(bool embedded)` | Amount of signature operations in the script.

## Members

#### `{property} bool `[`IsValid`](#class_bitprim_1_1_script_1aa6762b4acd4945c1b648ddd55802a430) 

All script bytes are valid under some circumstance (e.g. coinbase).

#### `{property} bool `[`OperationsAreValid`](#class_bitprim_1_1_script_1a3047f3d01ea8e30a429c2004ae20e500) 

[Script](#class_bitprim_1_1_script) validity is independent of individual operation validity. Operations are considered invalid if there is a trailing invalid/default op or if a push op has a size mismatch.

#### `{property} string `[`Type`](#class_bitprim_1_1_script_1ac3c48921a18d3864acbdf6937a8724a6) 

[Script](#class_bitprim_1_1_script) type

#### `{property} UInt64 `[`SatoshiContentSize`](#class_bitprim_1_1_script_1a73ee4ba9eb69e6caae61756fd995427b) 

Size in bytes.

#### `{property} IntPtr `[`NativeInstance`](#class_bitprim_1_1_script_1a1532f7d9458f9766de2fc79a8213d1f9) 

#### `public inline byte [] `[`ToData`](#class_bitprim_1_1_script_1a51e7a2f14655e6431b21e39f7abedfa8)`(bool prefix)` 

Raw script data

#### Parameters
* `prefix` Tells whether to include script size in data 

#### Returns
Byte array with script data

#### `public inline string `[`ToString`](#class_bitprim_1_1_script_1a7230eca6520c7b466e50ba9cdacf52c4)`(UInt32 activeForks)` 

Translate operations in the script to a string.

#### Parameters
* `activeForks` Tells which rule is active. 

#### Returns
Human readable script.

#### `public inline UInt64 `[`GetEmbeddedSigOps`](#class_bitprim_1_1_script_1a41f6fc1d3554e6e0736eeb0e5622b89f)`(`[`Script`](#class_bitprim_1_1_script)` prevOutScript)` 

Count the sigops in the embedded script using BIP16 rules.

#### Parameters
* `prevOutScript` Reference to previous output script. 

#### Returns
Embedded sigops count.

#### `public inline UInt64 `[`GetSigOps`](#class_bitprim_1_1_script_1a9d37fa88a73f37692b612697fb327066)`(bool embedded)` 

Amount of signature operations in the script.

#### Parameters
* `embedded` Iif true, consider this an embedded script. 

#### Returns
Sigops count.

# class `Bitprim::StealthCompact` 

```
class Bitprim::StealthCompact
  : public IDisposable
```  

Stealth payment related data.

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`{property} byte [] `[`EphemeralPublicKeyHash`](#class_bitprim_1_1_stealth_compact_1a7e981961a1a1fa41520c08cddcb8e1a7) | 33 bytes. Includes the sign byte (0x02).
`{property} byte [] `[`PublicKeyHash`](#class_bitprim_1_1_stealth_compact_1a4b079e4ca2dd42c7dfcecedf58d1c1c1) | Public key hash in 32 bytes array format.
`{property} byte [] `[`TransactionHash`](#class_bitprim_1_1_stealth_compact_1acccf8d9a07b8463f074f4d1c872d3425) | [Transaction](#class_bitprim_1_1_transaction) hash in 32 byte array format.

## Members

#### `{property} byte [] `[`EphemeralPublicKeyHash`](#class_bitprim_1_1_stealth_compact_1a7e981961a1a1fa41520c08cddcb8e1a7) 

33 bytes. Includes the sign byte (0x02).

#### `{property} byte [] `[`PublicKeyHash`](#class_bitprim_1_1_stealth_compact_1a4b079e4ca2dd42c7dfcecedf58d1c1c1) 

Public key hash in 32 bytes array format.

#### `{property} byte [] `[`TransactionHash`](#class_bitprim_1_1_stealth_compact_1acccf8d9a07b8463f074f4d1c872d3425) 

[Transaction](#class_bitprim_1_1_transaction) hash in 32 byte array format.

# class `Bitprim::TaskHelper` 

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------

## Members

# class `Bitprim::Transaction` 

```
class Bitprim::Transaction
  : public IDisposable
```  

Represents a Bitcoin transaction.

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`{property} bool `[`IsCoinbase`](#class_bitprim_1_1_transaction_1ae3a362e097393cbf8c8087107ac202e5) | Returns true if and only if this is a coinbase transaction (i.e. generates new coins).
`{property} bool `[`IsLocktimeConflict`](#class_bitprim_1_1_transaction_1ad7b30b6fa7c3ddea8e0ab1541810ae7f) | Returns true if and only if the transaction is locked and every input is final, false otherwise.
`{property} bool `[`IsMissingPreviousOutputs`](#class_bitprim_1_1_transaction_1af10e0b3b68b2a6d2dac82c67fa0c1e23) | Returns true if and only if at least one of the previous outputs is invalid, false otherwise.
`{property} bool `[`IsNullNonCoinbase`](#class_bitprim_1_1_transaction_1a49c7429cd339e138f983102fb530a96a) | Return true if and only if the transaction is not coinbase and has a null previous output, false otherwise.
`{property} bool `[`IsOversizeCoinbase`](#class_bitprim_1_1_transaction_1a7ebc78d891b9f5e4d01e0acb6a2214d5) | Returns true if the transaction is coinbase and has an invalid script size on its first input.
`{property} bool `[`IsOverspent`](#class_bitprim_1_1_transaction_1a5cccf30e1c82353fe678c393eb80df71) | Returns true if transaction is not a coinbase, and the sum of its outputs is higher than the sum of its inputs, false otherwise.
`{property} bool `[`IsValid`](#class_bitprim_1_1_transaction_1a29b8a68de9c1828a6b540f5dc02508da) | Returns true if and only if this transaction is valid according to the protocol.
`{property} byte [] `[`Hash`](#class_bitprim_1_1_transaction_1a54d13bfb55819222e4f302e1f8de063c) | [Transaction](#class_bitprim_1_1_transaction) hash in 32 byte array format.
`{property} InputList `[`Inputs`](#class_bitprim_1_1_transaction_1a33d098c55beee1bb9d7ff598ace272bc) | A list with all the transaction inputs.
`{property} OutputList `[`Outputs`](#class_bitprim_1_1_transaction_1a8f7202ac3b2839b02ea07197d88e0cfb) | A list with all the transaction outputs.
`{property} UInt32 `[`Locktime`](#class_bitprim_1_1_transaction_1a9049d57c642ab63763e906539db8f04a) | [Transaction](#class_bitprim_1_1_transaction) locktime.
`{property} UInt32 `[`Version`](#class_bitprim_1_1_transaction_1ae76b215e44e8e0a225dcca697b21002d) | [Transaction](#class_bitprim_1_1_transaction) protocol version.
`{property} UInt64 `[`Fees`](#class_bitprim_1_1_transaction_1a27c37d65dff9cae8fed5e6a684e641b7) | Fees to pay to the winning miner.
`{property} UInt64 `[`SignatureOperations`](#class_bitprim_1_1_transaction_1a9de1208d6409d511b3fa1b74d7020539) | Amount of signature operations in the transaction.
`{property} UInt64 `[`TotalInputValue`](#class_bitprim_1_1_transaction_1a291ada37f6535b154a7123ca3eb534ef) | Sum of every input value in the transaction.
`{property} UInt64 `[`TotalOutputValue`](#class_bitprim_1_1_transaction_1a48315105df2e9ddf66ded983200e0511) | Sum of every output value in the transaction.
`{property} IntPtr `[`NativeInstance`](#class_bitprim_1_1_transaction_1ae4213b4c3e5e4ab28371604d9f0a53cb) | 
`public inline  `[`Transaction`](#class_bitprim_1_1_transaction_1ab20ffd365084f400febcf58a9f2b7111)`()` | Create an empty tramsaction.
`public inline  `[`Transaction`](#class_bitprim_1_1_transaction_1abf686e7c063404e2ae28dc5e4b2bf5d4)`(UInt32 version,string hexString)` | Create a transaction from its binary hex representation.
`public inline  `[`Transaction`](#class_bitprim_1_1_transaction_1afd4417823dd268d17b2c1ded794a0183)`(UInt32 version,UInt32 locktime,InputList inputs,OutputList outputs)` | Create a transaction from its version, locktime, inputs and outputs (all its data).
`public inline byte [] `[`GetHashBySigHashType`](#class_bitprim_1_1_transaction_1aa6278991258a52cd285eb6c4d6fe4582)`(UInt32 sigHashType)` | 32 bytes transaction hash + 4 bytes signature hash type
`public inline bool `[`IsDoubleSpend`](#class_bitprim_1_1_transaction_1a5397d59e47283d0e7c204810a98b6f4e)`(bool includeUnconfirmed)` | Returns true if at least one of the previous outputs was already spent, false otherwise.
`public inline bool `[`IsFinal`](#class_bitprim_1_1_transaction_1ad014d272c29cbd0c464a215d022c4601)`(UInt64 blockHeight,UInt32 blockTime)` | Returns true if and only if the transaction is final, false otherwise.
`public inline bool `[`IsImmature`](#class_bitprim_1_1_transaction_1a4edf429fbd5515110dbdc4e426e0af02)`(UInt64 targetHeight)` | Returns true if and only if at least one of the inputs is not mature, false otherwise.
`public inline byte [] `[`ToData`](#class_bitprim_1_1_transaction_1a67c3525ef1013453c1bc85902edb2fc7)`(bool wire)` | Raw transaction data.
`public inline UInt64 `[`GetSerializedSize`](#class_bitprim_1_1_transaction_1ad10eaadf7083d1cc1dec7f89a4c482af)`(bool wire)` | [Transaction](#class_bitprim_1_1_transaction) size in bytes.
`public inline UInt64 `[`GetSignatureOperationsBip16Active`](#class_bitprim_1_1_transaction_1aff789aa4471796ddff33b26617188de9)`(bool bip16Active)` | Amount of signature operations in the transactions.

## Members

#### `{property} bool `[`IsCoinbase`](#class_bitprim_1_1_transaction_1ae3a362e097393cbf8c8087107ac202e5) 

Returns true if and only if this is a coinbase transaction (i.e. generates new coins).

#### `{property} bool `[`IsLocktimeConflict`](#class_bitprim_1_1_transaction_1ad7b30b6fa7c3ddea8e0ab1541810ae7f) 

Returns true if and only if the transaction is locked and every input is final, false otherwise.

#### `{property} bool `[`IsMissingPreviousOutputs`](#class_bitprim_1_1_transaction_1af10e0b3b68b2a6d2dac82c67fa0c1e23) 

Returns true if and only if at least one of the previous outputs is invalid, false otherwise.

#### `{property} bool `[`IsNullNonCoinbase`](#class_bitprim_1_1_transaction_1a49c7429cd339e138f983102fb530a96a) 

Return true if and only if the transaction is not coinbase and has a null previous output, false otherwise.

#### `{property} bool `[`IsOversizeCoinbase`](#class_bitprim_1_1_transaction_1a7ebc78d891b9f5e4d01e0acb6a2214d5) 

Returns true if the transaction is coinbase and has an invalid script size on its first input.

#### `{property} bool `[`IsOverspent`](#class_bitprim_1_1_transaction_1a5cccf30e1c82353fe678c393eb80df71) 

Returns true if transaction is not a coinbase, and the sum of its outputs is higher than the sum of its inputs, false otherwise.

#### `{property} bool `[`IsValid`](#class_bitprim_1_1_transaction_1a29b8a68de9c1828a6b540f5dc02508da) 

Returns true if and only if this transaction is valid according to the protocol.

#### `{property} byte [] `[`Hash`](#class_bitprim_1_1_transaction_1a54d13bfb55819222e4f302e1f8de063c) 

[Transaction](#class_bitprim_1_1_transaction) hash in 32 byte array format.

#### `{property} InputList `[`Inputs`](#class_bitprim_1_1_transaction_1a33d098c55beee1bb9d7ff598ace272bc) 

A list with all the transaction inputs.

#### `{property} OutputList `[`Outputs`](#class_bitprim_1_1_transaction_1a8f7202ac3b2839b02ea07197d88e0cfb) 

A list with all the transaction outputs.

#### `{property} UInt32 `[`Locktime`](#class_bitprim_1_1_transaction_1a9049d57c642ab63763e906539db8f04a) 

[Transaction](#class_bitprim_1_1_transaction) locktime.

#### `{property} UInt32 `[`Version`](#class_bitprim_1_1_transaction_1ae76b215e44e8e0a225dcca697b21002d) 

[Transaction](#class_bitprim_1_1_transaction) protocol version.

#### `{property} UInt64 `[`Fees`](#class_bitprim_1_1_transaction_1a27c37d65dff9cae8fed5e6a684e641b7) 

Fees to pay to the winning miner.

#### `{property} UInt64 `[`SignatureOperations`](#class_bitprim_1_1_transaction_1a9de1208d6409d511b3fa1b74d7020539) 

Amount of signature operations in the transaction.

#### `{property} UInt64 `[`TotalInputValue`](#class_bitprim_1_1_transaction_1a291ada37f6535b154a7123ca3eb534ef) 

Sum of every input value in the transaction.

#### `{property} UInt64 `[`TotalOutputValue`](#class_bitprim_1_1_transaction_1a48315105df2e9ddf66ded983200e0511) 

Sum of every output value in the transaction.

#### `{property} IntPtr `[`NativeInstance`](#class_bitprim_1_1_transaction_1ae4213b4c3e5e4ab28371604d9f0a53cb) 

#### `public inline  `[`Transaction`](#class_bitprim_1_1_transaction_1ab20ffd365084f400febcf58a9f2b7111)`()` 

Create an empty tramsaction.

#### `public inline  `[`Transaction`](#class_bitprim_1_1_transaction_1abf686e7c063404e2ae28dc5e4b2bf5d4)`(UInt32 version,string hexString)` 

Create a transaction from its binary hex representation.

#### Parameters
* `version` [Transaction](#class_bitprim_1_1_transaction) protocol version. 

* `hexString` Raw transaction in hex

#### `public inline  `[`Transaction`](#class_bitprim_1_1_transaction_1afd4417823dd268d17b2c1ded794a0183)`(UInt32 version,UInt32 locktime,InputList inputs,OutputList outputs)` 

Create a transaction from its version, locktime, inputs and outputs (all its data).

#### Parameters
* `version` [Transaction](#class_bitprim_1_1_transaction) protocol version. 

* `locktime` [Transaction](#class_bitprim_1_1_transaction) locktime. 

* `inputs` A list with all the transaction inputs. 

* `outputs` A list with all the transaction outputs.

#### `public inline byte [] `[`GetHashBySigHashType`](#class_bitprim_1_1_transaction_1aa6278991258a52cd285eb6c4d6fe4582)`(UInt32 sigHashType)` 

32 bytes transaction hash + 4 bytes signature hash type

#### Parameters
* `sigHashType` Sighash type. 

#### Returns
Hash and sighash type.

#### `public inline bool `[`IsDoubleSpend`](#class_bitprim_1_1_transaction_1a5397d59e47283d0e7c204810a98b6f4e)`(bool includeUnconfirmed)` 

Returns true if at least one of the previous outputs was already spent, false otherwise.

#### Parameters
* `includeUnconfirmed` Iif true, consider unconfirmed transactions. 

#### Returns
True if and only if transaction is double spend.

#### `public inline bool `[`IsFinal`](#class_bitprim_1_1_transaction_1ad014d272c29cbd0c464a215d022c4601)`(UInt64 blockHeight,UInt32 blockTime)` 

Returns true if and only if the transaction is final, false otherwise.

#### Parameters
* `blockHeight` 
* `blockTime` 

#### Returns

#### `public inline bool `[`IsImmature`](#class_bitprim_1_1_transaction_1a4edf429fbd5515110dbdc4e426e0af02)`(UInt64 targetHeight)` 

Returns true if and only if at least one of the inputs is not mature, false otherwise.

#### Parameters
* `targetHeight` 

#### Returns

#### `public inline byte [] `[`ToData`](#class_bitprim_1_1_transaction_1a67c3525ef1013453c1bc85902edb2fc7)`(bool wire)` 

Raw transaction data.

#### Parameters
* `wire` Iif true, include data size at the beginning.

#### Returns
Byte array with transaction data.

#### `public inline UInt64 `[`GetSerializedSize`](#class_bitprim_1_1_transaction_1ad10eaadf7083d1cc1dec7f89a4c482af)`(bool wire)` 

[Transaction](#class_bitprim_1_1_transaction) size in bytes.

#### Parameters
* `wire` If and only if true, size will include size of 'uint32' for storing spender output height 

#### Returns
Size in bytes.

#### `public inline UInt64 `[`GetSignatureOperationsBip16Active`](#class_bitprim_1_1_transaction_1aff789aa4471796ddff33b26617188de9)`(bool bip16Active)` 

Amount of signature operations in the transactions.

#### Parameters
* `bip16Active` True if and only if BIP16 is active, false otherwise. 

#### Returns

# class `Bitprim::Validations` 

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------

## Members

# struct `Bitprim::GetTxPositionResult` 

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`{property} UInt64 `[`Index`](#struct_bitprim_1_1_get_tx_position_result_1abf0a3a30f1926f1d5ca78805f807ccfb) | 
`{property} UInt64 `[`BlockHeight`](#struct_bitprim_1_1_get_tx_position_result_1a52fbd7cf6e6cb4f5e706be3a6a379cc1) | 

## Members

#### `{property} UInt64 `[`Index`](#struct_bitprim_1_1_get_tx_position_result_1abf0a3a30f1926f1d5ca78805f807ccfb) 

#### `{property} UInt64 `[`BlockHeight`](#struct_bitprim_1_1_get_tx_position_result_1a52fbd7cf6e6cb4f5e706be3a6a379cc1) 

# namespace `Bitprim::Logging` 

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`enum `[`LogLevel`](#namespace_bitprim_1_1_logging_1a89a90f71ddc112bc62c596aeb14d42a0)            | The log level.
`public delegate bool `[`Logger`](#namespace_bitprim_1_1_logging_1a87f15f0754f0a1275273f4caff520307)`(`[`LogLevel`](#namespace_bitprim_1_1_logging_1a89a90f71ddc112bc62c596aeb14d42a0)` logLevel,Func< string > messageFunc,Exception exception,params object [] formatParameters)`            | 
`class `[`Bitprim::Logging::LogExtensions`](#class_bitprim_1_1_logging_1_1_log_extensions) | 
`class `[`Bitprim::Logging::LoggerExecutionWrapper`](#class_bitprim_1_1_logging_1_1_logger_execution_wrapper) | 
`class `[`Bitprim::Logging::LogProvider`](#class_bitprim_1_1_logging_1_1_log_provider) | Provides a mechanism to create instances of ILog objects.

## Members

#### `enum `[`LogLevel`](#namespace_bitprim_1_1_logging_1a89a90f71ddc112bc62c596aeb14d42a0) 

 Values                         | Descriptions                                
--------------------------------|---------------------------------------------
Trace            | 
Debug            | 
Info            | 
Warn            | 
Error            | 
Fatal            | 

The log level.

#### `public delegate bool `[`Logger`](#namespace_bitprim_1_1_logging_1a87f15f0754f0a1275273f4caff520307)`(`[`LogLevel`](#namespace_bitprim_1_1_logging_1a89a90f71ddc112bc62c596aeb14d42a0)` logLevel,Func< string > messageFunc,Exception exception,params object [] formatParameters)` 

# class `Bitprim::Logging::LogExtensions` 

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------

## Members

# class `Bitprim::Logging::LoggerExecutionWrapper` 

```
class Bitprim::Logging::LoggerExecutionWrapper
  : public Bitprim.Logging.ILog
```  

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public inline bool `[`Log`](#class_bitprim_1_1_logging_1_1_logger_execution_wrapper_1a0b2e71f3abfbc89712dc665c303f4499)`(`[`LogLevel`](#namespace_bitprim_1_1_logging_1a89a90f71ddc112bc62c596aeb14d42a0)` logLevel,Func< string > messageFunc,Exception exception,params object [] formatParameters)` | 

## Members

#### `public inline bool `[`Log`](#class_bitprim_1_1_logging_1_1_logger_execution_wrapper_1a0b2e71f3abfbc89712dc665c303f4499)`(`[`LogLevel`](#namespace_bitprim_1_1_logging_1a89a90f71ddc112bc62c596aeb14d42a0)` logLevel,Func< string > messageFunc,Exception exception,params object [] formatParameters)` 

# class `Bitprim::Logging::LogProvider` 

Provides a mechanism to create instances of ILog objects.

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`{property} bool `[`IsDisabled`](#class_bitprim_1_1_logging_1_1_log_provider_1a8f9e9127793e0e036e4b54c590f3aa02) | Gets or sets a value indicating whether this is logging is disabled.
`{property} Action< `[`ILogProvider`](#interface_bitprim_1_1_logging_1_1_i_log_provider)` > `[`OnCurrentLogProviderSet`](#class_bitprim_1_1_logging_1_1_log_provider_1abb503a9dc6980810e845968c7dd3e6ac) | Sets an action that is invoked when a consumer of your library has called SetCurrentLogProvider. It is important that hook into this if you are using child libraries (especially ilmerged ones) that are using LibLog (or other logging abstraction) so you adapt and delegate to them. SetCurrentLogProvider

## Members

#### `{property} bool `[`IsDisabled`](#class_bitprim_1_1_logging_1_1_log_provider_1a8f9e9127793e0e036e4b54c590f3aa02) 

Gets or sets a value indicating whether this is logging is disabled.

`true` if logging is disabled; otherwise, `false`.

#### `{property} Action< `[`ILogProvider`](#interface_bitprim_1_1_logging_1_1_i_log_provider)` > `[`OnCurrentLogProviderSet`](#class_bitprim_1_1_logging_1_1_log_provider_1abb503a9dc6980810e845968c7dd3e6ac) 

Sets an action that is invoked when a consumer of your library has called SetCurrentLogProvider. It is important that hook into this if you are using child libraries (especially ilmerged ones) that are using LibLog (or other logging abstraction) so you adapt and delegate to them. SetCurrentLogProvider

# namespace `Bitprim::Logging::LogProviders` 

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`class `[`Bitprim::Logging::LogProviders::DisposableAction`](#class_bitprim_1_1_logging_1_1_log_providers_1_1_disposable_action) | 
`class `[`Bitprim::Logging::LogProviders::Log4NetLogProvider`](#class_bitprim_1_1_logging_1_1_log_providers_1_1_log4_net_log_provider) | 
`class `[`Bitprim::Logging::LogProviders::LogMessageFormatter`](#class_bitprim_1_1_logging_1_1_log_providers_1_1_log_message_formatter) | 
`class `[`Bitprim::Logging::LogProviders::LogProviderBase`](#class_bitprim_1_1_logging_1_1_log_providers_1_1_log_provider_base) | 
`class `[`Bitprim::Logging::LogProviders::LoupeLogProvider`](#class_bitprim_1_1_logging_1_1_log_providers_1_1_loupe_log_provider) | 
`class `[`Bitprim::Logging::LogProviders::NLogLogProvider`](#class_bitprim_1_1_logging_1_1_log_providers_1_1_n_log_log_provider) | 
`class `[`Bitprim::Logging::LogProviders::SerilogLogProvider`](#class_bitprim_1_1_logging_1_1_log_providers_1_1_serilog_log_provider) | 
`class `[`Bitprim::Logging::LogProviders::TraceEventTypeValues`](#class_bitprim_1_1_logging_1_1_log_providers_1_1_trace_event_type_values) | 
`class `[`Bitprim::Logging::LogProviders::TypeExtensions`](#class_bitprim_1_1_logging_1_1_log_providers_1_1_type_extensions) | 

# class `Bitprim::Logging::LogProviders::DisposableAction` 

```
class Bitprim::Logging::LogProviders::DisposableAction
  : public IDisposable
```  

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public  `[`DisposableAction`](#class_bitprim_1_1_logging_1_1_log_providers_1_1_disposable_action_1a0cb08e5ff6f32f072c09875bfa375ce0)`(Action onDispose)` | 

## Members

#### `public  `[`DisposableAction`](#class_bitprim_1_1_logging_1_1_log_providers_1_1_disposable_action_1a0cb08e5ff6f32f072c09875bfa375ce0)`(Action onDispose)` 

# class `Bitprim::Logging::LogProviders::Log4NetLogProvider` 

```
class Bitprim::Logging::LogProviders::Log4NetLogProvider
  : public Bitprim.Logging.LogProviders.LogProviderBase
```  

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`{property} bool `[`ProviderIsAvailableOverride`](#class_bitprim_1_1_logging_1_1_log_providers_1_1_log4_net_log_provider_1aa458d2a476f77b6fb6d532c4a87d0c27) | 
`public inline  `[`Log4NetLogProvider`](#class_bitprim_1_1_logging_1_1_log_providers_1_1_log4_net_log_provider_1aca8cffb0f4e1da0ad92125372dd5a2fd)`()` | 
`public override Logger `[`GetLogger`](#class_bitprim_1_1_logging_1_1_log_providers_1_1_log4_net_log_provider_1a50249194a29487e2e742815117973a69)`(string name)` | 
`protected inline override OpenNdc `[`GetOpenNdcMethod`](#class_bitprim_1_1_logging_1_1_log_providers_1_1_log4_net_log_provider_1a2dc9fde760ec81288f6cd9c01bc0ee33)`()` | 
`protected inline override OpenMdc `[`GetOpenMdcMethod`](#class_bitprim_1_1_logging_1_1_log_providers_1_1_log4_net_log_provider_1a5ea5b2d9325107a7e2cc716b541372da)`()` | 

## Members

#### `{property} bool `[`ProviderIsAvailableOverride`](#class_bitprim_1_1_logging_1_1_log_providers_1_1_log4_net_log_provider_1aa458d2a476f77b6fb6d532c4a87d0c27) 

#### `public inline  `[`Log4NetLogProvider`](#class_bitprim_1_1_logging_1_1_log_providers_1_1_log4_net_log_provider_1aca8cffb0f4e1da0ad92125372dd5a2fd)`()` 

#### `public override Logger `[`GetLogger`](#class_bitprim_1_1_logging_1_1_log_providers_1_1_log4_net_log_provider_1a50249194a29487e2e742815117973a69)`(string name)` 

#### `protected inline override OpenNdc `[`GetOpenNdcMethod`](#class_bitprim_1_1_logging_1_1_log_providers_1_1_log4_net_log_provider_1a2dc9fde760ec81288f6cd9c01bc0ee33)`()` 

#### `protected inline override OpenMdc `[`GetOpenMdcMethod`](#class_bitprim_1_1_logging_1_1_log_providers_1_1_log4_net_log_provider_1a5ea5b2d9325107a7e2cc716b541372da)`()` 

# class `Bitprim::Logging::LogProviders::LogMessageFormatter` 

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------

## Members

# class `Bitprim::Logging::LogProviders::LogProviderBase` 

```
class Bitprim::Logging::LogProviders::LogProviderBase
  : public Bitprim.Logging.ILogProvider
```  

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public abstract Logger `[`GetLogger`](#class_bitprim_1_1_logging_1_1_log_providers_1_1_log_provider_base_1a54c03de723dde7ab216559577bd616c2)`(string name)` | 
`public IDisposable `[`OpenNestedContext`](#class_bitprim_1_1_logging_1_1_log_providers_1_1_log_provider_base_1a703cb2b34b4e1c174fd4f44021f92276)`(string message)` | 
`public IDisposable `[`OpenMappedContext`](#class_bitprim_1_1_logging_1_1_log_providers_1_1_log_provider_base_1a880f73a34ab257553907729284d00961)`(string key,object value,bool destructure)` | 
`protected delegate IDisposable `[`OpenNdc`](#class_bitprim_1_1_logging_1_1_log_providers_1_1_log_provider_base_1a77ae5122ca397e98a55fd09c6a53793f)`(string message)` | 
`protected delegate IDisposable `[`OpenMdc`](#class_bitprim_1_1_logging_1_1_log_providers_1_1_log_provider_base_1a34c42e08bc3d9734b71544d97bd604a9)`(string key,object value,bool destructure)` | 
`protected inline  `[`LogProviderBase`](#class_bitprim_1_1_logging_1_1_log_providers_1_1_log_provider_base_1a7260f77fe92b7609581ac905a441d228)`()` | 
`protected virtual OpenNdc `[`GetOpenNdcMethod`](#class_bitprim_1_1_logging_1_1_log_providers_1_1_log_provider_base_1ac036d5f314ac108e86a94cd59f8b61ea)`()` | 
`protected virtual OpenMdc `[`GetOpenMdcMethod`](#class_bitprim_1_1_logging_1_1_log_providers_1_1_log_provider_base_1aca9325f22a202a0c3786f5fd89e35be7)`()` | 

## Members

#### `public abstract Logger `[`GetLogger`](#class_bitprim_1_1_logging_1_1_log_providers_1_1_log_provider_base_1a54c03de723dde7ab216559577bd616c2)`(string name)` 

#### `public IDisposable `[`OpenNestedContext`](#class_bitprim_1_1_logging_1_1_log_providers_1_1_log_provider_base_1a703cb2b34b4e1c174fd4f44021f92276)`(string message)` 

#### `public IDisposable `[`OpenMappedContext`](#class_bitprim_1_1_logging_1_1_log_providers_1_1_log_provider_base_1a880f73a34ab257553907729284d00961)`(string key,object value,bool destructure)` 

#### `protected delegate IDisposable `[`OpenNdc`](#class_bitprim_1_1_logging_1_1_log_providers_1_1_log_provider_base_1a77ae5122ca397e98a55fd09c6a53793f)`(string message)` 

#### `protected delegate IDisposable `[`OpenMdc`](#class_bitprim_1_1_logging_1_1_log_providers_1_1_log_provider_base_1a34c42e08bc3d9734b71544d97bd604a9)`(string key,object value,bool destructure)` 

#### `protected inline  `[`LogProviderBase`](#class_bitprim_1_1_logging_1_1_log_providers_1_1_log_provider_base_1a7260f77fe92b7609581ac905a441d228)`()` 

#### `protected virtual OpenNdc `[`GetOpenNdcMethod`](#class_bitprim_1_1_logging_1_1_log_providers_1_1_log_provider_base_1ac036d5f314ac108e86a94cd59f8b61ea)`()` 

#### `protected virtual OpenMdc `[`GetOpenMdcMethod`](#class_bitprim_1_1_logging_1_1_log_providers_1_1_log_provider_base_1aca9325f22a202a0c3786f5fd89e35be7)`()` 

# class `Bitprim::Logging::LogProviders::LoupeLogProvider` 

```
class Bitprim::Logging::LogProviders::LoupeLogProvider
  : public Bitprim.Logging.LogProviders.LogProviderBase
```  

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`{property} bool `[`ProviderIsAvailableOverride`](#class_bitprim_1_1_logging_1_1_log_providers_1_1_loupe_log_provider_1a63ff65b7c9de0c68d8312a07f1bb06ff) | Gets or sets a value indicating whether [provider is available override]. Used in tests.
`public inline  `[`LoupeLogProvider`](#class_bitprim_1_1_logging_1_1_log_providers_1_1_loupe_log_provider_1a3e3ce702a91a2ca75debb45998c83fa0)`()` | 
`public override Logger `[`GetLogger`](#class_bitprim_1_1_logging_1_1_log_providers_1_1_loupe_log_provider_1a8a7f8d51aa46620e00123299660d046c)`(string name)` | 

## Members

#### `{property} bool `[`ProviderIsAvailableOverride`](#class_bitprim_1_1_logging_1_1_log_providers_1_1_loupe_log_provider_1a63ff65b7c9de0c68d8312a07f1bb06ff) 

Gets or sets a value indicating whether [provider is available override]. Used in tests.

`true` if [provider is available override]; otherwise, `false`.

#### `public inline  `[`LoupeLogProvider`](#class_bitprim_1_1_logging_1_1_log_providers_1_1_loupe_log_provider_1a3e3ce702a91a2ca75debb45998c83fa0)`()` 

#### `public override Logger `[`GetLogger`](#class_bitprim_1_1_logging_1_1_log_providers_1_1_loupe_log_provider_1a8a7f8d51aa46620e00123299660d046c)`(string name)` 

# class `Bitprim::Logging::LogProviders::NLogLogProvider` 

```
class Bitprim::Logging::LogProviders::NLogLogProvider
  : public Bitprim.Logging.LogProviders.LogProviderBase
```  

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`{property} bool `[`ProviderIsAvailableOverride`](#class_bitprim_1_1_logging_1_1_log_providers_1_1_n_log_log_provider_1ac063ccdf79f8f39276748bd4d930e8d0) | 
`public inline  `[`NLogLogProvider`](#class_bitprim_1_1_logging_1_1_log_providers_1_1_n_log_log_provider_1a93ac90dfcc094ae42b35b7e963bd2fc7)`()` | 
`public override Logger `[`GetLogger`](#class_bitprim_1_1_logging_1_1_log_providers_1_1_n_log_log_provider_1af2114403f160959501ba353a684b628a)`(string name)` | 
`protected inline override OpenNdc `[`GetOpenNdcMethod`](#class_bitprim_1_1_logging_1_1_log_providers_1_1_n_log_log_provider_1a2de35597cae00eec9bf6ebdc9f50febe)`()` | 
`protected inline override OpenMdc `[`GetOpenMdcMethod`](#class_bitprim_1_1_logging_1_1_log_providers_1_1_n_log_log_provider_1a216c686b33156c4ac9e76e53dec346ee)`()` | 

## Members

#### `{property} bool `[`ProviderIsAvailableOverride`](#class_bitprim_1_1_logging_1_1_log_providers_1_1_n_log_log_provider_1ac063ccdf79f8f39276748bd4d930e8d0) 

#### `public inline  `[`NLogLogProvider`](#class_bitprim_1_1_logging_1_1_log_providers_1_1_n_log_log_provider_1a93ac90dfcc094ae42b35b7e963bd2fc7)`()` 

#### `public override Logger `[`GetLogger`](#class_bitprim_1_1_logging_1_1_log_providers_1_1_n_log_log_provider_1af2114403f160959501ba353a684b628a)`(string name)` 

#### `protected inline override OpenNdc `[`GetOpenNdcMethod`](#class_bitprim_1_1_logging_1_1_log_providers_1_1_n_log_log_provider_1a2de35597cae00eec9bf6ebdc9f50febe)`()` 

#### `protected inline override OpenMdc `[`GetOpenMdcMethod`](#class_bitprim_1_1_logging_1_1_log_providers_1_1_n_log_log_provider_1a216c686b33156c4ac9e76e53dec346ee)`()` 

# class `Bitprim::Logging::LogProviders::SerilogLogProvider` 

```
class Bitprim::Logging::LogProviders::SerilogLogProvider
  : public Bitprim.Logging.LogProviders.LogProviderBase
```  

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`{property} bool `[`ProviderIsAvailableOverride`](#class_bitprim_1_1_logging_1_1_log_providers_1_1_serilog_log_provider_1a825f601a067b4bd285b183d943da8a4c) | 
`public inline  `[`SerilogLogProvider`](#class_bitprim_1_1_logging_1_1_log_providers_1_1_serilog_log_provider_1ad57e5f1c761277bc013a40ed0f507085)`()` | 
`public override Logger `[`GetLogger`](#class_bitprim_1_1_logging_1_1_log_providers_1_1_serilog_log_provider_1adbe0c0f7a6dfed7e1d4f08335ab36bb8)`(string name)` | 
`protected override OpenNdc `[`GetOpenNdcMethod`](#class_bitprim_1_1_logging_1_1_log_providers_1_1_serilog_log_provider_1acd484c6e37b677b2f0362ed2451e1181)`()` | 
`protected override OpenMdc `[`GetOpenMdcMethod`](#class_bitprim_1_1_logging_1_1_log_providers_1_1_serilog_log_provider_1a6134cfb88fa2f26a89b4651721f2f9c8)`()` | 

## Members

#### `{property} bool `[`ProviderIsAvailableOverride`](#class_bitprim_1_1_logging_1_1_log_providers_1_1_serilog_log_provider_1a825f601a067b4bd285b183d943da8a4c) 

#### `public inline  `[`SerilogLogProvider`](#class_bitprim_1_1_logging_1_1_log_providers_1_1_serilog_log_provider_1ad57e5f1c761277bc013a40ed0f507085)`()` 

#### `public override Logger `[`GetLogger`](#class_bitprim_1_1_logging_1_1_log_providers_1_1_serilog_log_provider_1adbe0c0f7a6dfed7e1d4f08335ab36bb8)`(string name)` 

#### `protected override OpenNdc `[`GetOpenNdcMethod`](#class_bitprim_1_1_logging_1_1_log_providers_1_1_serilog_log_provider_1acd484c6e37b677b2f0362ed2451e1181)`()` 

#### `protected override OpenMdc `[`GetOpenMdcMethod`](#class_bitprim_1_1_logging_1_1_log_providers_1_1_serilog_log_provider_1a6134cfb88fa2f26a89b4651721f2f9c8)`()` 

# class `Bitprim::Logging::LogProviders::TraceEventTypeValues` 

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------

## Members

# class `Bitprim::Logging::LogProviders::TypeExtensions` 

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------

## Members

# class `Bitprim::Logging::LoggerExecutionWrapper::CallSiteExtension` 

```
class Bitprim::Logging::LoggerExecutionWrapper::CallSiteExtension
  : public Bitprim.Logging.LoggerExecutionWrapper.ICallSiteExtension
```  

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------

## Members

# class `Constants` 

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------

## Members

# class `Bitprim::Logging::LogProviders::Log4NetLogProvider::Log4NetLogger` 

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public inline bool `[`Log`](#class_bitprim_1_1_logging_1_1_log_providers_1_1_log4_net_log_provider_1_1_log4_net_logger_1ab64407ffab569fd99e360ae012d27ee4)`(`[`LogLevel`](#namespace_bitprim_1_1_logging_1a89a90f71ddc112bc62c596aeb14d42a0)` logLevel,Func< string > messageFunc,Exception exception,params object [] formatParameters)` | 

## Members

#### `public inline bool `[`Log`](#class_bitprim_1_1_logging_1_1_log_providers_1_1_log4_net_log_provider_1_1_log4_net_logger_1ab64407ffab569fd99e360ae012d27ee4)`(`[`LogLevel`](#namespace_bitprim_1_1_logging_1a89a90f71ddc112bc62c596aeb14d42a0)` logLevel,Func< string > messageFunc,Exception exception,params object [] formatParameters)` 

# class `Bitprim::Logging::LogProviders::LoupeLogProvider::LoupeLogger` 

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public inline bool `[`Log`](#class_bitprim_1_1_logging_1_1_log_providers_1_1_loupe_log_provider_1_1_loupe_logger_1a7430036e2428619f354edbff2e10552b)`(`[`LogLevel`](#namespace_bitprim_1_1_logging_1a89a90f71ddc112bc62c596aeb14d42a0)` logLevel,Func< string > messageFunc,Exception exception,params object [] formatParameters)` | 

## Members

#### `public inline bool `[`Log`](#class_bitprim_1_1_logging_1_1_log_providers_1_1_loupe_log_provider_1_1_loupe_logger_1a7430036e2428619f354edbff2e10552b)`(`[`LogLevel`](#namespace_bitprim_1_1_logging_1a89a90f71ddc112bc62c596aeb14d42a0)` logLevel,Func< string > messageFunc,Exception exception,params object [] formatParameters)` 

# class `Bitprim::Logging::LogProviders::NLogLogProvider::NLogLogger` 

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public inline bool `[`Log`](#class_bitprim_1_1_logging_1_1_log_providers_1_1_n_log_log_provider_1_1_n_log_logger_1a5bcaa10d1fa4fe93d68e297a8e3132a6)`(`[`LogLevel`](#namespace_bitprim_1_1_logging_1a89a90f71ddc112bc62c596aeb14d42a0)` logLevel,Func< string > messageFunc,Exception exception,params object [] formatParameters)` | 

## Members

#### `public inline bool `[`Log`](#class_bitprim_1_1_logging_1_1_log_providers_1_1_n_log_log_provider_1_1_n_log_logger_1a5bcaa10d1fa4fe93d68e297a8e3132a6)`(`[`LogLevel`](#namespace_bitprim_1_1_logging_1a89a90f71ddc112bc62c596aeb14d42a0)` logLevel,Func< string > messageFunc,Exception exception,params object [] formatParameters)` 

# class `Bitprim::Logging::LogProvider::NoOpLogger` 

```
class Bitprim::Logging::LogProvider::NoOpLogger
  : public Bitprim.Logging.ILog
```  

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public inline bool `[`Log`](#class_bitprim_1_1_logging_1_1_log_provider_1_1_no_op_logger_1af9f2b6a1bb4da4922d5d46992cb3feee)`(`[`LogLevel`](#namespace_bitprim_1_1_logging_1a89a90f71ddc112bc62c596aeb14d42a0)` logLevel,Func< string > messageFunc,Exception exception,params object [] formatParameters)` | 

## Members

#### `public inline bool `[`Log`](#class_bitprim_1_1_logging_1_1_log_provider_1_1_no_op_logger_1af9f2b6a1bb4da4922d5d46992cb3feee)`(`[`LogLevel`](#namespace_bitprim_1_1_logging_1a89a90f71ddc112bc62c596aeb14d42a0)` logLevel,Func< string > messageFunc,Exception exception,params object [] formatParameters)` 

# class `Bitprim::Logging::LogProviders::SerilogLogProvider::SerilogLogger` 

## Summary

 Members                        | Descriptions                                
--------------------------------|---------------------------------------------
`public inline bool `[`Log`](#class_bitprim_1_1_logging_1_1_log_providers_1_1_serilog_log_provider_1_1_serilog_logger_1afa133fc2dabc0cccdd32ef0c7df2ab11)`(`[`LogLevel`](#namespace_bitprim_1_1_logging_1a89a90f71ddc112bc62c596aeb14d42a0)` logLevel,Func< string > messageFunc,Exception exception,params object [] formatParameters)` | 

## Members

#### `public inline bool `[`Log`](#class_bitprim_1_1_logging_1_1_log_providers_1_1_serilog_log_provider_1_1_serilog_logger_1afa133fc2dabc0cccdd32ef0c7df2ab11)`(`[`LogLevel`](#namespace_bitprim_1_1_logging_1a89a90f71ddc112bc62c596aeb14d42a0)` logLevel,Func< string > messageFunc,Exception exception,params object [] formatParameters)` 

Generated by [Moxygen](https://sourcey.com/moxygen)