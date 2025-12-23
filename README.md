https://eth-mainnet.g.alchemy.com/v2/lSem2bdXGaejluyxuqaYvI0Sltzb3gNZ# hello-world-tutorial

This is the example code repository for the Alchemy Hello World tutorial series (parts 1, 2, 3).

curl --request POST \
     --url https://eth-mainnet.g.alchemy.com/v2/lSem2bdXGaejluyxuqaYvI0Sltzb3gNZ \
     --header 'accept: application/json' \
     --header 'content-type: application/json' \
     --data '
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_getBlockByNumber",
  "params": [
	  "finalized",
	  false
  ]
}
'node demo-script.js
demo-script.js
- [Part 1 Docs](https://docs.alchemy.com/alchemy/tutorials/hello-world-smart-contract)
- [Part 2 Docs](https://docs.alchemy.com/alchemy/tutorials/hello-world-smart-contract/interacting-with-a-smart-contract)
- [Part 3 Docs](https://docs.alchemy.com/alchemy/tutorials/hello-world-smart-contract/submitting-your-smart-contract-to-etherscan)
mkdir alchemy-demo
cd alchemy-demo
npm init --yes
touch demo-script.js
## Setup

You can clone this repo and get going right away.

Just make sure to:
- run `npm install` to set up all the dependencies (hardhat, ethers, etc.)curl --request POST \
     --url https://eth-mainnet.g.alchemy.com/v2/lSem2bdXGaejluyxuqaYvI0Sltzb3gNZ \
     --header 'accept: application/json' \
     --header 'content-type: application/json' \
     --data '
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_getBlockByNumber",
  "params": [
	  "finalized",
	  false
  ]
}node demo-script.js
mkdir alchemy-demo
cd alchemy-demo
npm init --yes
touch demo-script.js
'
- rename `.env-example` to `.env` and then fill in the environment variables with your own info
- set up an Alchemy account [here](https://alchemy.com/?a=641a319005)
- set up a [Metamask](https://metamask.io/download.html) wallet with [fake testnet ether](https://faucet.dimensions.network/)

And then you should be able to:
- run `npx hardhat run scripts/deploy.js` to deploy the contract to the Ropsten testnet
- run `npx hardhat run scripts/interact.js` to read and write a new message to the smart contract on Ropsten
- run `npx hardhat verify --network ropsten <your deplooyment address> 'Hello World!'` to verify your contract on Etherscan