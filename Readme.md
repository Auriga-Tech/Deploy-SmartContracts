# Deploy a Smart Contract

## Prerequisite 

- Install Meta Mask Extension
- Create a wallet address with Metamask
- Check a wallet's balance
- Add balance to the wallet (using test tokens)
- Install Ganache for Local Development

## Using WEB3.py library 
<hr>

- cd Web3
- make .env using help of .env.sample
- create virtual enviroment 
- python3 -m venv env
- source env/bin/activate
- add rpc url (for polygon or etherium), chain_id, version of contract, name of contract, privatekey
- then run the script 
- python deploy.py

## Using Brownie Library
<hr>

- Install Node and npm
- sudo npm install -g ganache-cli
- cd brownie-lib
- brownie bake token (Not Required)
- cd token
- brownie compile
- brownie test
- brownie run token

## Using Hyperledger-Fabric
<hr>

## Prerequisite
- CURL
- Docker
- Docker-Compose
- Go
- Node.js and NPM
- Python 2.7
- git config --global core.autocrlf false
- git config --global core.longpaths true


## Setup
    curl -sSL http://bit.ly/2ysbOFE | bash -s
    cd fabric-samples/test-network
    ./network.sh down
    ./network.sh up
    docker ps -a

### Creating Channel
    ./network.sh up createChannel -c mychannel -ca

### Deploying Smart Contract
    ./network.sh deployCC -ccn basic -ccp ../asset-transfer-basic/chaincode-typescript/ -ccl typescript


### Follow This for creating and running application  
- https://hyperledger-fabric.readthedocs.io/en/latest/write_first_app.html#prepare-the-sample-application