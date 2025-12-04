# MyToken (MTK)

## Overview
MyToken is a simple ERC-20-style learning token created on Ethereum using Solidity and Remix IDE.  
It demonstrates how balances, transfers, allowances, and events work in a fungible token.

## Token Details
- **Name**: MyToken
- **Symbol**: MTK
- **Decimals**: 18
- **Total Supply**: 1,000,000 MTK (minted to the deployer address)

## Features
- Fixed total supply configured in the constructor.
- `balanceOf` tracking for every address.
- `transfer` for sending tokens between addresses.
- `approve` and `transferFrom` for delegated transfers using allowances.
- `Transfer` and `Approval` events for transparency.
- Helper view functions: `getTotalSupply` and `getTokenInfo`.

## How to Deploy (Remix)

1. Open Remix at https://remix.ethereum.org.
2. Create a new file called `MyToken.sol` and paste the contract code.
3. In the **Solidity compiler** tab, select version 0.8.x and compile the contract.
4. Open the **Deploy & Run Transactions** tab.
5. Set **Environment** to `Remix VM (Prague)`.
6. Make sure the `MyToken` contract is selected in the **Contract** dropdown.
7. In the constructor field `_totalSupply`, enter `1000000000000000000000000` for 1,000,000 tokens with 18 decimals.
8. Click **Deploy**. The deployed contract will appear under **Deployed Contracts**.



## How to Use

### Read token data
- `name() -> string` : Returns the token name.
- `symbol() -> string` : Returns the token symbol.
- `decimals() -> uint8` : Returns the decimals value.
- `totalSupply() -> uint256` or `getTotalSupply()` : Returns total supply.
- `getTokenInfo() -> (string, string, uint8, uint256)` : Returns name, symbol, decimals, totalSupply.

### Check balances
- `balanceOf(address account) -> uint256`  
  Returns the token balance for `account`.

### Transfer tokens
- `transfer(address to, uint256 amount) -> bool`  
  Sends `amount` tokens from the caller to `to` if the caller has enough balance.

### Approve spending
- `approve(address spender, uint256 amount) -> bool`  
  Sets how many tokens `spender` is allowed to spend from the caller’s balance.

### Transfer on behalf
- `transferFrom(address from, address to, uint256 amount) -> bool`  
  Moves tokens from `from` to `to` using the caller’s allowance, and decreases the allowance.







