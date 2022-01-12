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

---

## What are Ethereum Nodes

- Ethereum is a peer-to-peer network of computers named Ethereum Nodes or Clients. Anyone can run an Ethereum node. There are no special prerequisites to run them.

- An Ethereum node runs a VM named EVM and runs applications (EVM bytecode) based on a global consensus mechanism. This EVM has its own microkernal, stack, memory, and storage.

- Thousands of nodes that communicate with each other make up the ethereum blockchain. Most of the  clients on the mainnet run *Geth* on Linux. *Geth* (Go Ethereum), was programmed in Go programming language and is one of the original implementations of the Ethereum protocol.
  
- There are also 3 Types of Nodes:
  - Full nodes: Stores locally a copy of the entire blockchain, participates in the block validation and verifies all blocks and states
  
  - Light nodes: Stores only the header chain and requests everything else, and can verify the validity of the data against the states in the block headers.
    - These light node clients are useful for low capacity devices which cannot afford to store gigabytes of blocking data.

  - Archive nodes: Stores everything kept in the full node and builds an archive of historical states.
    - It requires terabytes of disk space, which makes archive nodes less attractive for the average users.

- There are new clients for Ethereum 2.0 that run the Beacon and the Shard Chains and support the new proof-of-stake consensus mechanism.
  
- There are also many different Ethereum Networks: Main Net, Test Nets (Rinkeby, Kovan), and other Private Ethereum Blockchains.
  
### **How do we communicate with the Ethereum Network?**

- As stated above, ***Geth*** has been one of the main ways users have been able to communicate with one another in the Ethereum mainnet.  However, due to Linux being Linux, there have been other implementations that have allowed users to communicate with the network.

- Web3.js a collection of libraries that allows Web Applications to interact with an Ethereum node. It's the official JavaScript API developed by the core Ethereum team. It is going to be the main way we can communicate with the blockchain from a normal website.

- Wallets also are pieces of software that we use to communicate with the Ethereum mainnet. The wallet has access to the private key, which controls the Ethereum account and can interact with Ethereum Decentralized Applications.  

---

## What Are Ethereum Accounts

There are two types of Ethereum Accounts

1. Externally Owned Account (EOA)
   - Controlled by a private key and identified by an unique address
   - It holds an ETH balance and has no associated code
   - Used for holding, sending, and receiving ETH and for interacting with smart contracts (deployment, calling functions, etc).
   - Examples of an EOA are wallets like Metamask or MEW (MyEtherWallet).  <br><br>

2. Contract Account (CA)
   - Controlled by the contract code
   - Has a unique address but doesn't have a public or a private key
   - It's an autonomous agent and it's code execution is triggered by receiving a transaction or a message (call) from another contract of an EOA
   - It holds an ETH balance like an EOA
   - **NOTE: SINCE A CONTRACT ACCOUNT USES NETWORK STORAGE, CREATING A CONTRACT ACCOUNT COSTS GAS**

### **Components of an Ethereum Account**

1. Nonce: Counter that indicates the number of transactions sent from the account (it ensures that the same transaction isn't submitted twice)  

2. Balance  

3. Account Address

4. Account Private & Public Key (Only for EOA)

5. Code (Only for the contract account). This is the immutable EVM bytecode that gets triggered when transactions are made with the contract account

6. Storage (Only for the contract account, empty by default).  

### **Components of an Ethereum Address**

- An EOA Address is derived from the last 20 bytes (160 bits) of the public key that are Keccak-256 hashed. It's represented in a hexadecimal format, which is often indicated explicitly by appending 0x to the address.

  ***Example:*** *0xCC88135038293JN302N33N2N239b2b102...*

- The address for an Ethereum Contract is deterministically computed from the address of its creator (sender) and how many transactions the creator has sent (nonce).

- There is a lower-case address version and partial upper-case version that also contains a checksum.

***Maybe add something about the private key here. I forgot tbh...
