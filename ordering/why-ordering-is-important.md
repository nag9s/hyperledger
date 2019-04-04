[https://www.edureka.co/community/2694/how-is-ordering-of-transactions-done-in-block-in-hyperledger](https://www.edureka.co/community/2694/how-is-ordering-of-transactions-done-in-block-in-hyperledger)



I have read that in bitcoin blockchain a node/peer orders transaction and announces this block to other miners. Once the other miner agree that block is valid it is part of blockchain.

But, in hyperledger the mining is done differently. How do they maintain the order of the blocks in such case?



Consensus is the key concept for validating the order of transactions in a block, on a blockchain network. The ordering is critical because many types of network transactions have dependency on one or more prior transactions.

In current version of hyperledger there is a leader who is responsible for ordering transactions before they are executed by other peers. A peer communicates and maintain the blockchain state and the ledger.

Such peers receive ordered state updates from the consensus service and apply them to locally held state. Peers connect to the channel and may send and receive messgaes on the channel.

The channel outputs the same messages to all connected peers and outputs them to all peers in the same logical order. The communicted messages are called the candidate transactions and are included later in the block.

