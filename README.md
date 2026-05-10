# Awesome Sentrix [![Awesome](https://awesome.re/badge-flat.svg)](https://awesome.re)

A curated list of official resources, developer tools, infrastructure, applications, and guides for **Sentrix Chain**.

**Sentrix Chain** is a Rust-based, EVM-compatible Layer-1 blockchain focused on protocol engineering, validator infrastructure, RPC compatibility, staking, and developer tooling.

> This list focuses on official and actively maintained Sentrix resources. Alpha or in-development projects are marked clearly.

## Contents

- [Start Here](#start-here)
- [Official Links](#official-links)
- [Networks](#networks)
- [Core Protocol](#core-protocol)
- [Developer Tools](#developer-tools)
- [Smart Contracts](#smart-contracts)
- [Infrastructure](#infrastructure)
- [Applications](#applications)
- [Wallets](#wallets)
- [Tutorials](#tutorials)
- [Status Notes](#status-notes)
- [Contributing](#contributing)

## Start Here

- [Sentrix Chain Core](https://github.com/sentrix-labs/sentrix) - Rust-based EVM-compatible Layer-1 blockchain implementation.
- [dApp Starter](https://github.com/SentrisCloud/dapp-starter) - Minimal starter project for deploying Solidity contracts on Sentrix Chain.
- [TypeScript SDK](https://github.com/SentrisCloud/sdk-ts) - TypeScript SDK for EVM, native REST, and BFT/WebSocket interactions.
- [SentrixScan](https://scan.sentrixchain.com) - Block explorer for Sentrix Chain.
- [Sentrix Faucet](https://faucet.sentrixchain.com) - Faucet for requesting SRX on supported networks.

## Official Links

- [Website](https://sentrixchain.com) - Official Sentrix Chain website.
- [Sentrix Labs GitHub](https://github.com/sentrix-labs) - Core protocol and official chain repositories.
- [SentrisCloud GitHub](https://github.com/SentrisCloud) - User-facing apps, tooling, and ecosystem infrastructure.
- [SentrisCloud](https://sentriscloud.com) - Ecosystem application hub.
- [X / Twitter](https://x.com/sentrixchain) - Official Sentrix Chain updates.

## Networks

### Mainnet

- Network Name: `Sentrix Mainnet`
- Chain ID: `7119`
- Currency Symbol: `SRX`
- Explorer: [scan.sentrixchain.com](https://scan.sentrixchain.com)

### Testnet

- Network Name: `Sentrix Testnet`
- Chain ID: `7120`
- Currency Symbol: `SRX`
- Explorer: [scan.sentrixchain.com](https://scan.sentrixchain.com)
- Faucet: [faucet.sentrixchain.com](https://faucet.sentrixchain.com)

## Core Protocol

- [Sentrix Core Node](https://github.com/sentrix-labs/sentrix) - Core Rust implementation of Sentrix Chain.
- [Whitepaper](https://github.com/sentrix-labs/whitepaper) - Sentrix Chain whitepaper and protocol narrative.
- [Canonical Contracts](https://github.com/sentrix-labs/canonical-contracts) - Official EVM contracts including WSRX, Multicall3, SentrixSafe, and TokenFactory.
- [Sentrix DEX Contracts](https://github.com/sentrix-labs/sentrix-dex) - Native AMM / DEX contracts for the Sentrix ecosystem.
- [Brand Kit](https://github.com/sentrix-labs/brand-kit) - Official logos, icons, banners, and brand assets.

## Developer Tools

- [dApp Starter](https://github.com/SentrisCloud/dapp-starter) - End-to-end starter for deploying and interacting with contracts on Sentrix.
- [TypeScript SDK](https://github.com/SentrisCloud/sdk-ts) - SDK for interacting with Sentrix EVM, native APIs, and BFT channels.
- [Indexer](https://github.com/SentrisCloud/indexer) - Postgres-backed REST indexer for blocks, transactions, logs, tokens, and native chain data. `Phase 1 / scaffold`

## Smart Contracts

- [Canonical Contracts](https://github.com/sentrix-labs/canonical-contracts) - WSRX, Multicall3, SentrixSafe, and TokenFactory.
- [Sentrix DEX](https://github.com/sentrix-labs/sentrix-dex) - AMM and liquidity infrastructure for SRX ecosystem markets.
- [dApp Starter Contracts](https://github.com/SentrisCloud/dapp-starter/tree/main/contracts) - Example Solidity contracts for deployment on Sentrix.

## Infrastructure

- [SentrixScan](https://scan.sentrixchain.com) - Sentrix block explorer.
- [Sentrix Faucet](https://faucet.sentrixchain.com) - SRX faucet for supported networks.
- [Indexer](https://github.com/SentrisCloud/indexer) - Indexer infrastructure for explorer and application data.
- [SentrisCloud Frontend](https://github.com/SentrisCloud/frontend) - Monorepo for explorer, faucet, wallet, DEX, launchpad, airdrop, and websites.

## Applications

- [SentrixScan](https://scan.sentrixchain.com) - Explorer for Sentrix mainnet and testnet.
- [Sentrix Faucet](https://faucet.sentrixchain.com) - Faucet for requesting SRX.
- [Solux Web Wallet](https://solux.sentriscloud.com) - Self-custody web wallet for Sentrix.
- [CoinBlast](https://coinblast.sentriscloud.com) - Memecoin launchpad for Sentrix. `Alpha`
- [Sentrix DEX](https://dex.sentrixchain.com) - AMM / DEX interface for Sentrix. `Early`
- [Sentrix Airdrop](https://airdrop.sentrixchain.com) - Airdrop eligibility and claim interface. `Early`

## Wallets

- [Solux Web Wallet](https://solux.sentriscloud.com) - Browser-based self-custody wallet.
- Solux Mobile - Native mobile wallet for iOS and Android. `In development`
- MetaMask - Sentrix supports Ethereum-compatible wallet flows through EVM RPC.

## Tutorials

Official tutorials should be added here as they become available.

Recommended tutorial topics:

- Add Sentrix to MetaMask
- Get testnet SRX from the faucet
- Deploy a Solidity contract on Sentrix
- Read Sentrix blocks with viem
- Send an SRX transaction with ethers.js
- Run a Sentrix node
- Run a Sentrix validator
- Verify contracts with Sourcify

## Status Notes

- CoinBlast is currently marked as `Alpha`.
- Sentrix DEX is currently marked as `Early`.
- Solux Mobile is `In development`.
- The indexer is `Phase 1 / scaffold`.
- Some older app repositories under `sentrix-labs` are archived because they were consolidated into `SentrisCloud/frontend`.

## Contributing

Contributions are welcome.

Good contributions include:

- Sentrix tutorials
- RPC examples
- SDK examples
- validator guides
- dApp templates
- wallet integration notes
- explorer/indexer improvements
- corrections for outdated or broken links

Please read [CONTRIBUTING.md](CONTRIBUTING.md) before opening a pull request.
