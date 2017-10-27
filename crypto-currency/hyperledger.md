### 

### Hyperledger Sawtooth

[Hyperledger Sawtooth](https://www.hyperledger.org/projects/sawtooth), contributed by Intel, is a blockchain framework that utilizes a modular platform for building, deploying, and running distributed ledgers. Distributed ledger solutions built with Hyperledger Sawtooth can utilize various consensus algorithms based on the size of the network. By default, it uses the Proof of Elapsed Time (PoET) consensus algorithm, which provides the scalability of the Bitcoin blockchain without the high energy consumption. PoET allows for a highly scalable network of validator nodes. Hyperledger Sawtooth is designed for versatility, with support for both permissioned and permissionless deployments.

### Hyperledger Fabric

[Hyperledger Fabric](https://www.hyperledger.org/projects/fabric) was the first proposal for a codebase, combining previous work done by Digital Asset Holdings, Blockstream's libconsensus, and IBM's OpenBlockchain. Hyperledger Fabric provides a modular architecture, which allows components such as consensus and membership services to be plug-and-play. Hyperledger Fabric is revolutionary in allowing entities to conduct confidential transactions without passing information through a central authority. This is accomplished through different channels that run within the network, as well as the division of labor that characterizes the different nodes within the network. Lastly, it is important to remember that, unlike Bitcoin, which is a public chain, Hyperledger Fabric supports permissioned deployments.

### Hyperledger Indy

[Hyperledger Indy](https://www.hyperledger.org/projects) is a distributed ledger purpose-built for decentralized identity. Hyperledger Indy's goal is to achieve this by developing a set of

"(...) decentralized identity specs and artifacts that are independent of any particular ledger and will enable interoperability across any DLT that supports them."

Further information about the history of the project can be found at https://sovrin.org/.

### Hyperledger Burrow v0.16.1

Formally known as eris-db, Hyperledger Burrow was released in December 2014. Currently under incubation, Hyperledger Burrow is a permissionable smart contract machine that provides a modular blockchain client with a permissioned smart contract interpreter built- in part to the specification of the Ethereum Virtual Machine (EVM). It is the only available Apache-licensed EVM implementation.

Following are the major components of Burrow:

The Gateway provides interfaces for systems integration and user interfaces
The Smart contract application engine facilitates integration of complex business logic
The Consensus Engine serves the dual purpose of: 
a. Maintaining the networking stack between the nodes, and,
b. Ordering transactions
The Application Blockchain Interface (ABCI) provides interface specification for the consensus engine and smart contract application engine to connect.
You can learn more about Hyperledger Burrow at https://monax.io/platform/db/.

### Hyperledger Cello

For businesses that want to deploy Blockchain-as-a-Service, Hyperledger Cello provides a toolkit that fulfills this need. Particularly for lean businesses and small enterprises, who want to reduce or eliminate the effort required in creating, managing, and terminating blockchains, Hyperledger Cello allows blockchains deployment to the cloud. Operators can create and manage such blockchains through a dashboard, and users (typically, chaincode developers) can obtain a blockchain instance immediately.

### Hyperledger Explorer

[Hyperledger Explorer](https://www.hyperledger.org/projects/explorer) is a tool for visualizing blockchain operations. It is the first ever blockchain explorer for permissioned ledgers, allowing anyone to explore the distributed ledger projects being created by Hyperledger's members from the inside, without compromising their privacy. The project was contributed by DTCC, Intel, and IBM.

Designed to create a user-friendly web application, Hyperledger Explorer can view, invoke, deploy, or query:

Blocks
Transactions and associated data
Network information (name, status, list of nodes)
Smart contracts (chain codes and transaction families)
Other relevant information stored in the ledger.
The ability to visualize data is of critical importance, in order to extract business value from it. Hyperledger Explorer provides this much needed functionality. Key components include a web server, a web UI, web sockets, a database, a security repository, and a blockchain implementation.

### Hyperledger Composer

[Hyperledger Composer](https://www.hyperledger.org/projects/composer) provides a suite of tools for building blockchain business networks. These tools allow you to:

Model your business blockchain network
Generate REST APIs for interacting with your blockchain network
Generate a skeleton Angular application.
Built in Javascript, Hyperledger Composer provides an easy-to-use set of components that developers can quickly learn and implement. The project was contributed by Oxchains and IBM.