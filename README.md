# Avalanche Subnets

This GitHub repository contains two Solidity smart contracts: `ERC20.sol` and `Vault.sol`. These contracts are designed to create and manage a simple ERC-20 token and a vault for managing deposits and withdrawals of that token. Below, you'll find more information about these contracts and how to use them.

## ERC20.sol

`ERC20.sol` is an ERC-20 token implementation with basic functionalities. Here's an overview of its features:

- **Token Name:** Solidity by Example
- **Token Symbol:** SOLBYEX
- **Decimals:** 18
- **Total Supply:** The total supply of the token is initially set to 0 and can be increased by minting new tokens and decreased by burning tokens.

### Functions

1. `transfer(address recipient, uint amount) external`: Transfer tokens from the sender's address to the specified recipient.

2. `approve(address spender, uint amount) external`: Approve a spender to spend a certain amount of tokens on behalf of the sender.

3. `transferFrom(address sender, address recipient, uint amount) external`: Transfer tokens from a sender to a recipient, with the allowance mechanism.

4. `mint(uint amount) external`: Mint new tokens and add them to the sender's balance. Increases the total supply.

5. `burn(uint amount) external`: Burn tokens from the sender's balance, reducing the total supply.

### Events

- `Transfer(address indexed from, address indexed to, uint value)`: Triggered when tokens are transferred.
- `Approval(address indexed owner, address indexed spender, uint value)`: Triggered when an approval is granted to a spender.

## Vault.sol

`Vault.sol` is a smart contract that acts as a vault for managing deposits and withdrawals of an ERC-20 token. It uses the ERC-20 interface to interact with the token contract. Here's a brief summary of its features:

- **Token Interaction:** It uses an ERC-20 token interface to interact with the token contract, allowing users to deposit and withdraw the token.

- **Shares:** The vault keeps track of shares for each user, allowing users to deposit and withdraw token amounts based on their share of the total supply.

### Functions

1. `deposit(uint _amount) external`: Deposit ERC-20 tokens into the vault, receiving shares in return. Shares are calculated based on the proportion of tokens deposited compared to the total supply in the vault.

2. `withdraw(uint _shares) external`: Withdraw ERC-20 tokens from the vault by burning the specified number of shares. Shares are redeemed for an equivalent amount of tokens.
