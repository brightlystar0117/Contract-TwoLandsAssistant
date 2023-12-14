# TwoLandsV2CH Token

## Overview

TwoLandsV2CH is an Ethereum-based ERC-20 token with additional features for managing transfers, taxation, and anti-sniper protections. The token is designed to provide a flexible and secure environment for decentralized finance (DeFi) applications.

## Token Features

### 1. ERC-20 Standard

TwoLandsV2CH adheres to the ERC-20 standard, enabling compatibility with various decentralized exchanges (DEX) and wallets.

### 2. Taxation System

The token implements a taxation system on transfers. The tax percentage can be adjusted by the governor address, providing a mechanism for adapting to changing market conditions. The destination for taxed tokens can also be updated, allowing for flexibility in managing collected taxes.

### 3. Maximum Percentage Holding

The token introduces a maximum percentage holding mechanism to prevent individual addresses from accumulating an excessive amount of the total supply. This feature aims to promote a more distributed ownership structure.

### 4. Maximum Transfer Percentage

To prevent large and potentially disruptive transfers, the token implements a maximum transfer percentage. This limits the amount of tokens that can be transferred in a single transaction.

### 5. Blacklist Mechanism

The contract includes a blacklist mechanism, allowing the governor to temporarily blacklist addresses for a specified duration (initially 7 days). This feature can be useful for addressing potential security concerns or preventing malicious activity.

### 6. Initial Liquidity Requirement

Before trading is enabled, the contract ensures that initial liquidity has been provided. This requirement aims to create a more stable trading environment.

### 7. Anti-Sniper Protections

To prevent sniper attacks and promote fair trading, the token incorporates anti-sniper features. A cooldown period is implemented, restricting the frequency of trades for a given address. Additionally, a bot protection toggle allows the governor to enable or disable specific anti-bot measures.

## Contract Functions

### `enableTrading()`

The `enableTrading()` function allows the governor to enable trading once the initial liquidity has been provided. This function marks the transition to an active trading state.

### `toggleBotProtection(bool _state)`

The `toggleBotProtection()` function enables or disables bot protection features. When enabled, these features help prevent bot-driven attacks or manipulative trading practices.

## Contract Deployment

The contract is deployed with an initial supply, and the governor address is set during deployment. The governor address has the authority to adjust taxation parameters, update the tax destination, manage liquidity-related functions, and toggle various features.

## Disclaimer

This token and its features are subject to the governance decisions made by the governor address. Users and developers are encouraged to review the contract code and documentation to understand its behavior and implications fully. Additionally, the provided anti-sniper features serve as examples, and developers are encouraged to explore and propose alternative ideas for enhancing the contract's security and functionality.
