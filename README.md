# simple-ledger

Imagine you are running a multi-national drug smuggling operation and you need to keep a ledger of payoffs to the authorities...

You can't trust anybody to keep this electronically on a centralised service so you decide to write this information to the Blockchain.

Only one person, the chief accountant, can make entries and "owns" the smart contract (and has the relevant skills to make direct transactions via his wallet of choice).

The rest of the cartel want to see the ledger entries (via their mobile devices or at their desktops) to ensure their guys are getting the correct amounts.

The cartel are very cocky and are happy with the public nature of the Blockchain transactions as they use a two letter code for all their dodgy counterparts.

## Smart Contract

A contract called [SimpleLedger](https://github.com/andygray/simple-ledger/blob/master/contracts/SimpleLedger.sol) has one function `recordEntry` that can be called by the `owner` of the contract to commit new entries to the ledger.

The ledger is held as a simple `mapping (bytes2 => int256)` data structure, for example, `"AG" -> 2543`

### Test-chain Deployments 

[Ropsten @ 0x0C3dc5ec9106CF7c5702430e727De76786fb3C9e](https://ropsten.etherscan.io/address/0x0C3dc5ec9106CF7c5702430e727De76786fb3C9e)

## Read-only Dapp

*Remember reads on a Blockchain are free*

[index.html](https://github.com/andygray/simple-ledger/blob/master/index.html) is a one pager that connects to a hosted node provided by [Infura](https://infura.io/) and uses [ethers.js](https://github.com/ethers-io/ethers.js/) a JavaScript helper library to interact with the Ethereum Blockchain.

In our application the contract specifics are configured and then calls to the [SimpleLedger](https://github.com/andygray/simple-ledger/blob/master/contracts/SimpleLedger.sol) contract return entries that can be displayed.

[JQuery](http://jquery.com/) is used solely to process the results and manipulate the page DOM and display information from the Blockchain.

### Hosted Deployment

*Firebase is used only for hosting, hence the config files but no remote centralised database is used*

[https://simple-ledger-36f80.firebaseapp.com/](https://simple-ledger-36f80.firebaseapp.com/)



