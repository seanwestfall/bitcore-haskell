# bitcore-haskell

This is a bitcoin node written in haskell.

It's based off of these implementations:
* https://github.com/bitcoin/bitcoin
* https://github.com/bitcoinfs/bitcoinfs
* https://github.com/btcsuite/btcd
* https://github.com/coinbase/toshi

An explanation of all the parts of a bitcoin node/client can be found here:

https://bitcointalk.org/index.php?topic=41718.0

![Work in Progress](/work-in-progress.jpg)

Initialization and Startup
        Upon startup, the client performs various initilization routines
        including starting multiple threads to handle concurrent operations.

## The main functional sections of a Bitcoin node are:
* Node Discovery: The client uses various techniques find out about other bitcoin nodes that may exist.

* Node Connectivity: The client initiates and maintains connections to other nodes.

* Sockets and Messages: The client processes messages from other nodes and sends messages to other nodes using socket connections.
    
* Block Exchange: Nodes advertise their inventory of blocks to each other and exchange blocks to build block chains.

* Transaction Exchange: Nodes exchange and relay transactions with each other. The client associates transactions with bitcoin addresses in the local wallet.

* Wallet Services: The client can create transactions using the local wallet. The client associates transactions with bitcoin addresses in the local wallet. The client provides a service for managing the local wallet.

* RPC Interface: The client offers an JSON-RPC interface over HTTP over sockets to perform various operational functions and to manage the local wallet.

* User Interface: The user interface used to control messaging and transactions.
