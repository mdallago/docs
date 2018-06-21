## Extensible Blockchain Protocol \(EBP\) Technical Specification

###### Version 0.1, 2017-10-27

####  Introduction

This document describes the requirements for Extensible Blockchain Protocol.

This proposal is a first step towards making the bitcoin protocol easier to modify.

The Extensible Blockchain Protocol \(EBP\) will allow nodes to dynamically modify the maximum acceptable block size, based on a consensus among the users of the network.



#### Motivation

Historically, deploying updates on the bitcoin protocol has been a very slow process, as it forces all nodes to upgrade before the improvements are usable.

To allow new proposals to be applied more dynamically on the protocol, the consensus rules should be adaptable as follows: When the majority of the network's nodes update to support a proposal, the minority that did not update in time can follow and operate on the chain that is being generated.

When a block using a new update is mined, the updated nodes will follow the new chain without problems. The non-updated nodes do not know if this chain is going to be the one that most of the network will accept, so they'll download the new blocks without immediately using them.  
  
Two possibilities exist:

* The “non-updated” chain keeps growing. This means that the updated consensus rules were not accepted by the majority of the community, since a large part of the nodes and miners are still mining and following the "non-updated" chain.

* The "non-updated" chain stops growing, or generates very slow blocks and it is outgrown by the new chain. This means that the proposal was accepted by the community and that all nodes should follow that new chain.

If the update was accepted by the majority of the community, the old nodes will update their consensus rules, validate the block, and set the new chain as their active chain.

The Extensible Blockchain Protocol is the first step in the creation of the new consensus, because it modifies the rule that verifies the maximum block size, and updates it as the network requires.



#### Definitions

_**EBP block**_: A block that has a size that is not currently accepted by the node.

_**EBP chain**_: A fork containing at least one EBP block.

_**EBP threshold**_: Extra work required for the EBP chain to become the active chain on non-updated nodes. It is equal to eleven times the work of the top block of the active chain.

####  Specification

This section describes the behavior of a non-updated node when it receives an EBP block.

##### Flag the blocks

When the node receives a block that exceeds the \`maximum block size\` defined by its consensus rules, the node flags it as an \`EBP\` block \(instead of discarding the block\).

The rest of the block validation should be postponed until the consensus rules are updated to accept the EBP block. Any fork that contains at least one EBP block is considered an EBP chain and should be treated as such.

##### EBP Chain Work required

To prevent attacks, the required work to accept an EBP chain as valid is greater than the required for a "normal" block. This ensure that the EBP chain has the support of the majority of the network and that the node will only update its consensus rules when necessary.

Whenever a non-updated node receives a block that builds on top of an EBP chain, the node will compare the accumulated work of the EBP chain to the accumulated work of the active chain plus the EBP threshold. If it's greater it will try to validate the EBP chain.

The value of the EBP threshold is equal to eleven times the work of the top block on the active chain.

##### Update consensus rules

When the EBP chainwork exceeds the node’s currently active chainwork plus the EBP threshold, it’s safe to connect the EBP chain to our active chain.

In order to be able to set the EBP chain as the active one, the node should update its consensus rules to be able to validate the new chain.

The updated maximum block size is equal to the minimum power of 2 which is greater than the biggest block size on the EBP chain. So if the nodes current maximum block size is equal to 8Mb and the EBP chain largest block is 10Mb in size, the node will update its consensus rules to accept 16Mb blocks.

##### Validate the blocks

Once the consensus rules have been updated, the node can fully validate the EBP chain and connect it as valid.

**Store the updated consensus rules**

The updated maximum block size should be stored for future executions, and loaded when the node is starting.

  


