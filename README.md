# UPGRADEABLE SMART CONTRACTS

This is a Upgradeable Smart Contract workshop from Patrick Alpha's fcc. Another implementation of Upgradeable Smart Contracts from Chainlink Spring Hackathon 2022 was created [here](https://github.com/JMariadlcs/upgradeable-smart-contracts).

The workshop followed to complete this repo is [this one](https://github.com/PatrickAlphaC/hardhat-upgrades-fcc).

The repo that we are going to implement is like [this one](https://www.youtube.com/watch?v=gyMwXuJrbJQ&t=15996s).

-   [Proxies by Openzeppeling](https://github.com/OpenZeppelin/openzeppelin-contracts/tree/master/contracts/proxy) are going to be used.
-   [Delegate by call example](https://solidity-by-example.org/delegatecall).

## CREATE SIMILAR PROJECT FROM SCRATCH

-   Install yarn and start hardhat project:

```bash
yarn
yarn add --dev hardhat
yarn hardhat
```

-   Install ALL the dependencies:

```bash
yarn add --dev @nomiclabs/hardhat-waffle@^2.0.0 ethereum-waffle@^3.0.0 chai@^4.2.0 @nomiclabs/hardhat-ethers@^2.0.0 ethers@^5.0.0 @nomiclabs/hardhat-etherscan@^3.0.0 dotenv@^16.0.0 eslint@^7.29.0 eslint-config-prettier@^8.3.0 eslint-config-standard@^16.0.3 eslint-plugin-import@^2.23.4 eslint-plugin-node@^11.1.0 eslint-plugin-prettier@^3.4.0 eslint-plugin-promise@^5.1.0 hardhat-gas-reporter@^1.0.4 prettier@^2.3.2 prettier-plugin-solidity@^1.0.0-beta.13 solhint@^3.3.6 solidity-coverage@^0.7.16 @nomiclabs/hardhat-ethers@npm:hardhat-deploy-ethers ethers @chainlink/contracts hardhat-deploy hardhat-shorthand @aave/protocol-v2
```

-   Install OpenZeppelin dependencies (contracts):

```bash
yarn add --dev @openzeppelin/contracts
```

## HOW TO COMPILE

```bash
yarn hardhat compile
```

or

```bash
npx hardhat compile
```

## HOW TOT DEPLOY

If you want to use [Hardhat shorthand](https://hardhat.org/guides/shorthand):

```bash
yarn global add hardhat-shorthand
```

-   Deploy to local network (Harhat by default):

```bash
hh compile
hh deploy
```

-   Deploy to a TESTNET (Rinkeby):
    You can not deploy all scripts at the same time because you can deploy [mint.js](https://github.com/JMariadlcs/nfts-fullrepo/blob/main/deploy/04-mint.js) script without firtly add randomNFT to ConsumerBase.

To deploy every script expect [mint.js](https://github.com/JMariadlcs/nfts-fullrepo/blob/main/deploy/04-mint.js):

```bash
yarn hardhat deploy --network rinkeby --tags main
```

## HOW TO TEST

Two types of tests are created for this project:

1. "Unit tests" inside [unit](https://github.com/JMariadlcs/nfts-fullrepo/tree/main/test/unit): used to test functions separately

To execute tests **unit tests** (on development chain):

```bash
yarn hardhat test
```

and to see test coverage:

```bash
yarn hardhat coverage
```

## RESOURCES

-   [Proxies by Openzeppeling](https://github.com/OpenZeppelin/openzeppelin-contracts/tree/master/contracts/proxy) are going to be used.
-   [Delegate by call example](https://solidity-by-example.org/delegatecall)
