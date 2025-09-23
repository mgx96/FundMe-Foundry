![Solidity](https://img.shields.io/badge/Solidity-0.8.30-blue)  
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)  
![Status](https://img.shields.io/badge/Status-Deployed-brightgreen)  

# FundMe Smart Contract  

A decentralized crowdfunding contract where users can fund in ETH, with contributions validated against a **minimum USD threshold** using Chainlink price feeds. The contract allows only the owner to withdraw all funds.  

## Features  

- Minimum funding of **$5 USD** (via Chainlink oracles)  
- Multiple contributors tracking  
- Owner-only withdrawals  
- Gas optimizations with `constant` and `immutable` variables  
- Comprehensive unit and integration testing with **Foundry**  
- Deployment and interaction scripts  

## Contracts  

- `FundMe.sol`: Core contract for funding and withdrawals  
- `PriceConverter.sol`: Library for ETH-USD conversions via Chainlink feeds  
- `HelperConfig.sol`: Network configuration helper for deployments  
- `FundMe.t.sol`: Script to unit test the main functions in the FundMe contract
- `Interactions.s.sol`: Script to fund the contract and to withdraw contract balance  
- `InteractionsTest.t.sol`: Integration test script 
- `Mocks/MockV3Aggregator.sol`: Mock price feed for local testing  

## How to Use  

1. Clone the repository:  
   ```bash
   git clone https://github.com/mgx96/FundMe-Foundry.git
   cd fundme-smart-contract

2. Install dependencies:
   ```bash
   forge install

3. Run tests:
   ```bash
   forge test -vvv

4. Deploy to sepolia
   ```bash
   make deploy-sepolia

## Deployment

**Network**: Ethereum Sepolia Testnet  
**Contract Address**: [`0xf769df2010bE87381eb3d41E6213a3080AA9e8F2`](https://sepolia.etherscan.io/address/0xf769df2010bE87381eb3d41E6213a3080AA9e8F2)  
**Verified on Etherscan**: ✅

## License

MIT
