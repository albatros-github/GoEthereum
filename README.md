# GoEthereum

go ethereum (geth) is a blockchain node infrastructure

## 1. install last version and check periodically (no auto-update, manuually requiered): 

https://geth.ethereum.org/docs/install-and-build/installing-geth

## 2. run for first time to sync node:

geth

-if run alone attems at first a fast sync, if abruptly interrupt, restarts as full sync (can take a week) and exist the light sync for tests

## 3. after sync you can attach to the JavaScript RCP interface to interact with the node

//Path appears in the logs of the first sync, with the "chinID" (reserved: 1 for mainnet, 2 and 3 for test network)
geth attach ipc:/path/to/geth.ipc   

~/.ethereum dir has the blocks in "chaindata" dir and the private keys in "keystore" dir
