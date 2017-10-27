### Hyperledger Iroha

Hyperledger Iroha is a blockchain framework, and one of the Hyperledger projects hosted by The Linux Foundation. Hyperledger Iroha was initially contributed by Soramitsu, Hitachi, NTT Data, and Colu. Hyperledger Iroha is designed to be simple and easy to incorporate into infrastructure projects requiring distributed ledger technology. Hyperledger Iroha features a simple construction, modern, domain-driven C++ design, emphasis on mobile application development, and the YAC consensus algorithm.

### Architecture Overview

Before diving into the key components of Hyperledger Iroha, it is important to get an overarching look at this framework. The diagram below shows a layered architectural view of the different components that make up Hyperledger Iroha. The four layers are: API, Peer Interaction, Chain Business Logic, and Storage.

<Iroha architecture>

The components are:

Model classes are system entities.
Torii (gate) provides the input and output interfaces for clients. It is a single gRPC server that is used by clients to interact with peers through the network. The client's RPC call is non-blocking, making Torii an asynchronous server. Both commands (transactions) and queries (read access) are performed through this interface.
Network encompasses interaction with the network of peers.
Consensus is in charge of peers agreeing on chain content in the network. The consensus mechanism used by Iroha is YAC (Yet Another Consensus), which is a practical byzantine fault-tolerant algorithm based on voting for block hash.
Simulator generates a temporary snapshot of storage to validate transactions by executing them against this snapshot and forming a verified proposal, which consists only of valid transactions.
Validator classes check business rules and validity (correct format) of transactions or queries. There are two distinct types of validation that occur in Hyperledger Iroha:

- Stateless validation is a quicker form of validation, that performs schema and signature checks of the transaction.

- Stateful validation is a slower form of validation, that checks the permissions and the current world state view, which is the latest and most actual state of the chain, to see if desired business rules and policies are possible. For example, does an account have enough funds to transfer?
Synchronizer helps to synchronize new peers in the system or temporarily disconnected peers.
Ametsuchi is the ledger block storage which consists of a block index (currently Redis), block store (currently flat files), and a world state view component (currently PostgreSQL).

### Joining the Hyperledger Iroha Community on GitHub

Hyperledger Iroha is an open source project where ideas and code can be publicly discussed, created, and reviewed. There are many ways to join the Hyperledger Iroha community, and we will share with you some of the ways to get involved, either from a technical standpoint, or from an ideas/issues creation perspective.

GitHub Logo

You can get involved with the Hyperledger Iroha community on GitHub. All code available on GitHub is forkable and viewable:

https://github.com/hyperledger/iroha
https://github.com/hyperledger/iroha-ios
https://github.com/hyperledger/iroha-android
https://github.com/hyperledger/iroha-javascript
https://github.com/hyperledger/iroha-python
https://github.com/hyperledger/iroha-scala
https://github.com/hyperledger/iroha-dotnet
https://github.com/hyperledger/iroha-api.

You can join the live conversations on Rocket.Chat (which is an alternative to Slack), using your Linux Foundation ID:

https://chat.hyperledger.org/channel/iroha
https://chat.hyperledger.org/channel/iroha-smartcontracts.
Another option is to join the mailing list(s) for technical discussions and announcements: https://lists.hyperledger.org/mailman/listinfo/hyperledger-iroha.
