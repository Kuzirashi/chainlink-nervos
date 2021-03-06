# Chainlink Oracles on Nervos Layer 2

This project is a simple implementation of some of the Chainlink contracts on Nervos. This repository is using Ether.js + Hardhat + Typechain + TypeScript.

Existing aggregators / feeds:
- CKB / USD
- ETH / USD
- DAI / ETH

Feed Registry address on Nervos Layer 2 testnet: `0x1363bdCE312532F864e84924D54c7dA5eDB5B1BC`

Documentation: https://docs.chain.link/docs/feed-registry/

Solidity interface: https://github.com/smartcontractkit/chainlink/blob/7289ac78fceeb995fec8f74415bb282a3ad43b66/contracts/src/v0.7/interfaces/FeedRegistryInterface.sol

Denominations can be found in: DeployOracles.ts file.

## Install & build

```
yarn
```

Build:

```
yarn build

// Contracts only
yarn compile

// TypeScript only
yarn build:types && yarn build:ts
```

## Start

Before usage you need to provide correct values for:
```
const USER_ONE_PRIVATE_KEY = 'YOUR_PRIVATE_KEY';
const ETH_MAINNET_RPC = 'YOUR_ETH_MAINNET_RPC_EG_INFURA';
const COINAPI_KEY = 'YOUR_COINAPI_KEY'; // https://www.coinapi.io/
```

in DeployOracles.ts

```
yarn start
```