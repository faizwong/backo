# Backo - Decentralized Crowdfunding Membership Platform
Backo is a decentralized crowdfunding membership platform that rewards contributors with custom ERC20 tokens.

Learn more about Backo [here](docs/about.md).

Watch a video demonstration [here](https://youtu.be/c2jcrlDq5Bk).

Application demo [here](https://backo.netlify.app).

## Setup
### Build and run project locally
Backo smart contracts are developed using Truffle. The frontend client is using React. The following steps assume you have Node, npm/yarn, truffle and ganache-cli installed.

#### Install all the dependencies of the project
```
yarn install
```

#### Run a local blockchain
```
ganache-cli --blockTime 15
```
Specifying the blockTime is important as Backo smart contracts contain time-dependent logic

#### Compile smart contracts
```
truffle compile
```

#### Run migrations
```
truffle migrate --reset --network development
```

#### Start local frontend client server
```
yarn start
```

### Testing

Tests can be run with the command
```
truffle test
```
It is recommended to adjust the `minBlocksPerRound` constant in the `Backo.sol` contract to a lower number (e.g: 50). Advancing too many blocks may cause the tests to be slow.


## Project Directory
```
backo
├── docs
├── migrations
├── public
├── src
│   ├── build
│   └── contracts
├── test
├── package.json
└── truffle-config.js
```

* docs: Documentations
* migrations: Migration scripts
* public: React public folder
* src: React code
* build: Smart contract build artifacts
* contracts: Smart contract code
* test: Smart contract tests
* `package.json`: Project metadata
* `truffle-config.js`: Truffle configuration
