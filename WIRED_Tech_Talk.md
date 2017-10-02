# Blockchain Tech Talk

## How do you make a (crypto)currency?
 
- transaction method needs to be atomic
- secure
- ideally non-centeralised (no one point of failure/1 bank you rely on) means need a distributed system
- store money (wallet)


## What is the blockchain?

- pretty much just a datastructure
- a list of records, grouped into blocks computed individually
- blocks linked in a chain
- blocks can be traced throughout the chain to the first
- don't need to be hosted on a centralised server, anyone can download the blockchain and append new blocks
- solves "double spending" (via blockchain calculations)

### Applications

- Token/ticketing systems
- financial derivatives + currency
- identity and reputation system
file storage
- decentralised organisations
- cloud computing
- P2P gambling :rage:
- prediction markets
- decentralised marketspace

### History

- bitcoin is the first use of a blockchain (apart form testing)
- other coins such as ethereum have also been created

### Basic Theory

- blocks hashed based on stored information
- internal information also includes hash of previous block. So medelling with internal ledge can be detected easily
- if there are multiple inconsistent hashes the nodes on the network will assume the majority hash is correct and use that chain (don't quite get this).
- uses `Merkel Tree` pretty much a normal tree but only leaf nodes contain data and parent nodes have hashes of them with the root node having the hash of the entire blockchain.

## Ethereum

Adaptation of bitcoin, distributed computing system where you can make side :money_with_wings:.

### Ethereum whitepaper

- distributed computing platofrm
- provides a scripting lagnauge to erform computatins on remote nodes
- cryptocurrecny called `ether`, `ethereum` is the network

### Way it works

I want to do a hard computational task i.e. compute prime numbers put until 1,000,000. Write the code, give 'rewards' for each step and them give it to the network. Work can be distributed over clients which get `x` reward you specified.

### Transactions/Mining

Part of the transfered amount is the `processing fee` which is proportional to `computational steps` required.

More complex stuff to deal with spam and dodgy things as well.

### State Transitions

Each block contains state
- immutable and can only be updated with transactions
- time cant be more than 2 hours in the future
- nonce
- previous hash of the prev block
- list of transactions
- state is what each node thinks is going on at this point
- a node is a computer

Can trace from `genesis block` (first block) to current by doing all the transactions.

### Magic Stuff

- hashing function is `double-SHA256`
- target is about ~2^187 (network decides this, number from ethereum whitepaper)
- SHa256 is meant to be unpredictable pseudorandom function, only way to re-created a valid block is trail and error, will take around half the target time. 
- creating a new block allows the creator a complimentary `5 ether transaction` and all the `gas` in the block.

### Mining on laptops
- probs won't get anywhere
- use a mining pool


### InterPlanetry File System (IPFS)

- distributed file system similar to bitTorrent that uses blockchain to store file locations
- attempting to 'distrupted' the internet by replacing http (but is built upon it i think)
- is content addressable
- can be seem as a bitTorrent swarm exchanging objects within one git directory
- internet on your phones like in silicon valley
https://github.com/ipfs/ipfs

### Problems

- What happens when the blockchain becomes super big and you need a datacenter to store it making it centeralised again.
- bitcoin hashing algorithm is not 100% unique and specalized a6 hardware can be used


