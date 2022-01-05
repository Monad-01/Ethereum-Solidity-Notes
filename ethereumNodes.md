# Introduction to Ethereum

## What is Ethereum in a nutshell

- The Ethereum Blockchain is an immutable public database that stores records of all the transactions that have ever taken place. This ensures that if someone were to try to change something (Let's say illegally forge money to their name), we will be able to know if there has been tampering with the blockchain, and it will be able to resist any of those changes through standard network checks.

- Ethereum builds on Bitcoin's innovation, with its own improvements  

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

- Thousands of nodes that communicate with each other make up the ethereum blockchain. Most of the  clients on the mainnet run *Geth* on Linux. *Geth* (Go Ethereum), was programmed in Go programming language and is one of the original implementations of the Ethereum protocol.

### How do we communicate with the Ethereum Network?

- As stated above, ***Geth*** has been one of the main ways users have been able to communicate with one another in the Ethereum mainnet.  However, due to Linux being Linux, there have been other implementations that have allowed users to communicate with the network.

- Web3.js a collection of libraries that allows webapplications to interact with an Ethereum node. It's the official JavaScript API developed by the core Ethereum team. It is one of the of