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

### **Behind the Scenes of a Transaction**

- So whenever we create a transaction on Metamask, it is validated locally, and then it is sent to an Ethereum node to which it communicates with. That node broadcasts the transaction to the whole Ethereum Network, and now we can track the transaction with it's transaction id or hash.

---

## GAS GAS GAS

- **Gas** is the unit that measure the amount of computational effort, required to execute specific operations. Like a car needs gasoline to function, the Ethereum platform needs its gas to work.
  
- **Any transaction that modifies the blockchain in any way costs gas**. Any basic operation or data storage costs gas. This is why gas is so important to understand when learning about the Ethereum blockchain.

- The person that generates the transaction needs to pay the gas fees for it. They pay for the gas using ETH.

- Gas fees also help keep the Ethereum Network secure because it prevents a hacker from attacking the network with a DoS attack because they have to pay money for each basic operation.

- Each operation has a fixed amount of gas it costs to cast. 

### Why are there *"Gas Wars"*?

One thing a new person entering crypto usually thinks about is, why are the Gas Prices this high? Do I really need to pay 100/200/300 Gwei per unit of gas? The *short answer* is no, you are not forced to pay that much for gas. You could make a transaction where you only pay 10 Gwei per unit of gas.

The *real answer* is that your transaction will not only fail, it won't be included within the new block. This is because miners will sort and then select the transactions that are waiting to be mined by their gas price. The higher the gas price, the more likely miners in the network will **select your transaction to be added to the block**.

>There is a limit to the number of transaction that can be included in a new block, and that limit is based on the gas price, which is dynamically set  by the network.

Now using that information, what is stopping a whale from minting multiple times on an NFT drop or making multiple transactions within an application? ***It's the Gas.***

Whales will try to fight each other in sought out digital collections by literally paying thousands of dollars worth in ETH to just make sure their transactions go through the blockchain. Other *normal users* will have to wait till the gas wars end or spend equally as much as the whales to confirm their transactions thus coining the term ***"Gas Wars***.

***BE SURE TO ADD OP CODES FOR GAS TRANSACTIONS***

---

## Ethereum Transactions

Transactions are the heart of the Ethereum Blockchain. Interacting with the Ethereum Blockchain means executing transactions that update the blockchain state.

- The term "transaction" is used in Ethereum to refer to the signed data package that stores a message to be sent from an EOA to another account on the blockchain.

- Any transaction requires a fee to be paid (gas).

- Contracts have the ability to send "messages" to other contracts.

- **An EOA produces a transaction and a contract produces a message.**

### **Life Cycle of an Ethereum Transaction**

1. The client constructs the raw transaction object

2. The client signs the transaction with the private key and validates it locally

3. The transaction is broadcasted to the network by the Ethereum Client and a transaction ID (txid) is returned
      - The Ethereum wallets connects to an Ethereum node, that will broadcast the signed transaction to its peers, and then those nodes will broadcast it to their other peers, and so on until it is broadcasted to the entire network.
  
4. The transaction is added to the transaction pool and waits there to be validated by the miner. A minder node accepts the transaction. Ethereum Network has a mix of minder nodes and non-miner nodes.
      - Once again, the transactions in the pool are sorted by gas price. And the miners will always prioritize the transactions with the higher gas price.
  
5. Miner finds a valid block by solving the PoW puzzle (or PoS) and adds the new block to the existing blockchain. The number of transactions in the block depends on the block gas limit.

6. The miner node broadcasts the new block to all other nodes. All nodes execute the transactions from the new block, but only the miner gets paid. (block reward + transactions fee - gas).