# Introduction to Ethereum

## What is Ethereum in a nutshell

- The Ethereum Blockchain is an immutable public database that stores records of all the transactions that have ever taken place. This ensures that if someone were to try to change something (Let's say illegally forge money to their name), we will be able to know if there has been tampering with the blockchain, and it will be able to resist any of those changes through standard network checks.

- Ethereum builds on Bitcoin's innovation, with its own improvements.  

- Ethereum allows you to send ___Ether___ to run smart contracts which are decentralized applications

  - *Note*: The name of the blockchain is Ethereum. The name of the cryptocurrency is Ether or Eth. <br><br>

- In summary, Ethereum is used to send digital money called Eth ***OR*** run decentralized applications called smart contracts.

- Ethereum is:
  - Decentralized
    - No central company or entity could shut down the Ethereum applications
  - Immutable
    - In the case of classical applications, data is stored in an SQL database, anybody that has rights can run SQL statements such as update or delete and modify the data.
    - However on Ethereum, anybody can send transactions to the blockchain. And when those transactions are confirmed, they cannot be reverted.
  - Unstoppable
    - Once a smart contract (An agreement translated into code) is deployed on the Ethereum blockchain, it runs forever and cannot be stopped
  - Censorship-free
    - No third-party can interfere and stop anyone else from using the Ethereum network.
  - More private than web2
    - No need to provide identity to have a wallet and transfer money or run smart contracts

--------------------

## What are Ethereum Nodes

- Ethereum is a peer-to-peer network of computers named Ethereum Nodes or Clients. Anyone can run an Ethereum node. There are no special prerequisites to run them.

- An Ethereum node runs a VM named EVM and runs applications (EVM bytecode) based on a gobal consensus mechanism. This EVM has its own micorkernal, stack, memory, and storage.

- Thousands of nodes that communicate with each other make up the ethereum blockchain. Most of the  clients on the mainnet run *Geth* on Linux. *Geth* (Go Ethereum), was programmed in Go programming language and is one of the original implementations of the Ethereum protocol.
  
- There are also 3 Types of Nodes:
  - Full nodes: Stores locally a copy of the entire blockchain, participates in the block validation and veriifies all blocks and states
  
  - Light nodes: Stores only the header chain and requests everything else, and cvan verify the validity of the data against the states in the block headers.
    - These light node clients are useful for low capacity devices which cannot afford to store gigabytes of blocking data.

  - Archive nodes: Stores everything kept in the full node and builts an archive of historical states.
    - It requires terabytes of disk space, which makes archive nodes less attractive for the average users.

- There are new clients for Ethereum 2.0 that run the Beacon and the Shard Chains and support the new proof-of-stake consensus mechanism.
  
- There are also many different Ethereum Networks: Main Net, Test Nets (Rinkeby, Kovan), and other Private Ethereum Blockchains.
  
### **How do we communicate with the Ethereum Network?**

- As stated above, ***Geth*** has been one of the main ways users have been able to communicate with one another in the Ethereum mainnet.  However, due to Linux being Linux, there have been other implementations that have allowed users to communicate with the network.

- Web3.js a collection of libraries that allows webapplications to interact with an Ethereum node. It's the official JavaScript API developed by the core Ethereum team. It is going to be the main way we can communicate with the blockchain from a normal website.

- Wallets also are pieces of software that we use to communicate with the Ethereum mainnet. The wallet has access to the private key, which controls the Ethereum account and can interact with Ethereum Decentralized Applications.  

---

## What Are Ethereum Accounts

There are two types of Ethereum Accounts

1. Externally Owned Account (EOA)
   - Controlled by a private key and identified by an unique address
   - It holds an ETH balance and has no associated code
   - Used for holding, sending, and receiving EWTH and for interacting with smart contracts (deployment, calling functions, etc). <br><br>

2. Contract Account (CA)
   - Controlled by the contract code
   - Has a unique address but doesn't have a public or a private key
   - It's an autonomous agent and it's code execution is triggered by receiving a transaction or a message (call) from another contract of an EOA
   - It holds an ETH balance like an EOA
