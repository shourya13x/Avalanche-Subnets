# Advanced Avalanche Smart Contracts

This repository contains Solidity smart contracts demonstrating advanced functionalities of ERC-20 tokens and a vault system for managing token deposits and withdrawals.

## Description

The repository includes two main smart contracts:

1. **ERC20.sol**: Implements a basic ERC-20 token named "CrazyToken" with standard functionalities such as minting, burning, transferring tokens, and approving allowances.

2. **Vault.sol**: A vault contract that allows users to deposit ERC-20 tokens and mint corresponding shares. Users can also withdraw their tokens by burning shares. The vault manages the token balance and total supply to ensure proportional distribution of shares.

### Key Features

#### ERC20.sol

- **Minting Tokens**: Allows the creation of new tokens, increasing the total supply.
- **Burning Tokens**: Enables destruction of tokens, reducing the total supply.
- **Transferring Tokens**: Facilitates the transfer of tokens between addresses.
- **Approving Allowances**: Grants permission to another address to spend tokens on behalf of the owner.
- **Transferring from an Allowance**: Allows approved addresses to transfer tokens within the set allowance.

#### Vault.sol

- **Depositing Tokens**: Users can deposit ERC-20 tokens and receive vault shares in return.
- **Withdrawing Tokens**: Users can withdraw their deposited tokens by burning vault shares.
- **Minting Shares**: The vault mints shares proportional to the deposited token amount.
- **Burning Shares**: The vault burns shares proportional to the withdrawn token amount.

## Getting Started

### Prerequisites

- [Remix Ethereum](https://remix.ethereum.org/): An online IDE for Solidity development and deployment.
- MetaMask: A browser extension for Ethereum wallet and transactions.

### Deploying the Contracts

1. **Open Remix IDE**: Navigate to [Remix Ethereum](https://remix.ethereum.org/).
2. **Create New Files**: Create new Solidity files (e.g., `ERC20.sol` and `Vault.sol`) and paste the respective contract code.
3. **Compile the Contracts**:
   - Click on the "Solidity Compiler" tab in the left sidebar.
   - Select a compatible compiler version (e.g., `0.8.17`).
   - Click "Compile ERC20.sol" and "Compile Vault.sol".
4. **Deploy the Contracts**:
   - Go to the "Deploy & Run Transactions" tab in the left sidebar.
   - Select the `ERC20` contract from the dropdown menu and deploy it.
   - Copy the deployed `ERC20` contract address.
   - Select the `Vault` contract, paste the `ERC20` contract address into the constructor parameter, and deploy it.
   - Confirm transactions in MetaMask.

### Interacting with the Contracts

After deploying the contracts, interact with their functions using Remix interface:

#### ERC20.sol

- **Minting Tokens**: Call the `mint` function to create new tokens (only available to the owner).
- **Transferring Tokens**: Use the `transfer` function to send tokens to another address.
- **Approving Allowances**: Call the `approve` function to set an allowance for another address.
- **Transferring from Allowance**: Use the `transferFrom` function to transfer tokens within the set allowance.
- **Burning Tokens**: Call the `burn` function to destroy tokens from your balance.

#### Vault.sol

- **Depositing Tokens**: Call the `deposit` function to deposit tokens and mint shares.
- **Withdrawing Tokens**: Use the `withdraw` function to burn shares and withdraw tokens.
- **Checking Balance**: Use the `balanceOf` function to check the balance of shares.
- **Checking Total Supply**: Call the `totalSupply` function to view the total supply of shares.

## License

This project is licensed under the MIT License. See the LICENSE.md file for details.