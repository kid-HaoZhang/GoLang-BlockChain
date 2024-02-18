# Golang-based Blockchain

This Go-based blockchain prototype is an imitation of Bitcoin and includes several key features. I build this for getting a solid foundation for understanding how blockchains work. 

## Features

1. Basic Blockchain Structure:
A simple blockchain with blocks linked together using cryptographic hashes.
Each block contains a list of transactions.
2. Proof of Work (PoW):
Implemented PoW consensus mechanism to secure the network.
Miners compete to find a nonce that satisfies the difficulty target.
3. Transactions:
Transactions are the heart of the blockchain.
Each transaction includes inputs (references to previous outputs) and outputs (newly created coins).
4. Address (Wallets):
Wallets generate public-private key pairs.
Addresses are derived from public keys and are used to send/receive coins.
5. Simplified Payment Verification (SPV):
SPV nodes can verify transactions without downloading the entire blockchain.
This rely on Merkle Trees to efficiently validate data.
6. Blockchain Data Storage:
Utilizes LevelDB for efficient storage of blockchain data.
Blocks, UTXO set, and other relevant information are stored.
7. Distributed Network:
Nodes communicate over a network (we use different port on a single machine to simulate different node) to share blocks and transactions

## Getting Started
### Installation

1. Make sure you have Go installed.
2. Running the Blockchain:
   
### Compile and run the main Go file.

You can specify different ports for nodes to simulate a distributed network.
Interacting with the Blockchain:
Use the command line interface (CLI) to create blockchain, create wallets, send transactions, and mine blocks.
First export NODE_ID=1000(This value stands for the port of the server)
Example commands:
$ ./blockchain createwallet NODE_ID
$ ./blockchain createblockchain -address NODE_ID
$ ./blockchain send -from NODE_ID -to WALLET_1 -amount 10 -mine(-mine flag means that the block will be immediately mined by the same node.)
$ ./blockchain startnode
$ ./blockchain getbalance -address WALLET_1

Use ./blockchain --help to find out more

Contributing
Feel free to contribute to this project by submitting pull requests or reporting issues.