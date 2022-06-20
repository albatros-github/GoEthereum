# GoEthereum

go ethereum (geth) is a blockchain node infrastructure

## 1. install last version and check periodically (no auto-update, manuually requiered): 

https://geth.ethereum.org/docs/install-and-build/installing-geth


### 1.1 edit and add path to geth to $PATH to ~/.profile

nano ~/.profile
//add line
export PATH="/path/to/geth:$PATH"

save file and then execute
. ~/.profile

## 2. INIT BLOCKCHAIN NODE FOR PUBLIC BLOCKCHAIN ONLY:

### 2.1 run for first time to sync node
geth

-if run alone attems at first a fast sync, if abruptly interrupt, restarts as full sync (can take a week) and exist the light sync for tests

### 2.2 after sync you can attach to the JavaScript RCP interface to interact with the node

//Path appears in the logs of the first sync, with the "chinID" (reserved: 1 for mainnet, 2 and 3 for test network)
geth attach ipc:/path/to/geth.ipc   

~/.ethereum dir has the blocks in "chaindata" dir and the private keys in "keystore" dir

## 3. INIT BLOCKCHAIN NODE FOR PRIVATE BLOCKCHAIN:

### 3.1 create an empty rootDir, and inside it, create a dir called "chaindata"

### 3.2 create genesis.json file (one in the repo)

### 3.3 create private blockchain

geth --datadir=./chaindata init ./genesis.json

## 4. start geth node RCP interface and identify IPC endpoint opened url=/... in logs:

geth --datadir=./chaindata --nodiscover

## 5. attach to the JavaScript RCP interface to interact with the node

//Path appears in the logs of the first sync, with the "chinID" (reserved: 1 for mainnet, 2 and 3 for test network)

geth attach ipc:/path/to/geth.ipc   

