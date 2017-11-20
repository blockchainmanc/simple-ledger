# simple-ledger

Imagine you are running a multi-national drug smuggling operation and you need to keep a ledger of payoffs to the authorities...

You can't trust anybody to keep this electronically on a centralised service so you decide to write this information to the Blockchain.

Only one person, the chief accountant, can make entries and "owns" the smart contract (and has the relevant skills to make direct transactions via his wallet of choice).

The rest of the cartel want to see the ledger entries to ensure their guys are getting the correct amounts.

The cartel are very confident and are happy with the public nature of the Blockchain transactions as they use a two letter code for all their dodgy counterparts.

## Smart Contract

Called [SimpleLedger]()

[Ropsten @ 0x0C3dc5ec9106CF7c5702430e727De76786fb3C9e](https://ropsten.etherscan.io/address/0x0C3dc5ec9106CF7c5702430e727De76786fb3C9e)

## Read-only Dapp

[simple_ledger.html]() connects to a hosted node provided by Infura and uses [ether.js]() a helper library to interact with the Ethereum Blockchain.

[JQuery]() is used solely to process the results and manipulate the page DOM and display information from the Blockchain.



