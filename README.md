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
- [Bridges](#bridges)
- [Applications](#applications)
- [Wallets](#wallets)
- [Running a Node](#running-a-node)
- [Tutorials](#tutorials)
- [Security](#security)
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
- [Telegram — @SentrixChain](https://t.me/SentrixChain) - Sentrix Chain channel.
- [Telegram — @SentrixCommunity](https://t.me/SentrixCommunity) - Sentrix community chat.

## Networks

### Mainnet

- Network Name: `Sentrix Chain`
- Chain ID: `7119`
- Currency Symbol: `SRX`
- RPC URL: `https://rpc.sentrixchain.com`
- gRPC: `grpc.sentrixchain.com:443` (service `sentrix.v1.Sentrix`)
- Explorer: [scan.sentrixchain.com](https://scan.sentrixchain.com)

### Testnet

- Network Name: `Sentrix Testnet`
- Chain ID: `7120`
- Currency Symbol: `SRX`
- RPC URL: `https://testnet-rpc.sentrixchain.com`
- gRPC: `grpc-testnet.sentrixchain.com:443` (service `sentrix.v1.Sentrix`)
- Explorer: [scan-testnet.sentrixchain.com](https://scan-testnet.sentrixchain.com)
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
- [Rust SDK](https://github.com/SentrisCloud/sdk-rs) - Typed Rust clients for native REST, EVM (alloy), gRPC (tonic), and secp256k1 wallet/signing. `Early`
- [Sentrix gRPC-Web Client](https://github.com/SentrisCloud/sentrix-grpc-wasm) - Rust + WASM gRPC-Web client packaged via wasm-pack, for browser dApps. `Early`
- [Token List](https://github.com/sentrix-labs/token-list) - Canonical Uniswap-token-list-v1 registry for Sentrix mainnet (7119) and testnet (7120).
- [Indexer](https://github.com/SentrisCloud/indexer) - Postgres-backed REST indexer for blocks, transactions, logs, tokens, and native chain data. `Phase 1 / scaffold`

## Smart Contracts

- [Canonical Contracts](https://github.com/sentrix-labs/canonical-contracts) - WSRX, Multicall3, SentrixSafe, and TokenFactory.
- [Sentrix DEX](https://github.com/sentrix-labs/sentrix-dex) - AMM and liquidity infrastructure for SRX ecosystem markets.
- [Token List](https://github.com/sentrix-labs/token-list) - Uniswap-token-list-v1 registry of recognized tokens on Sentrix Chain.
- [dApp Starter Contracts](https://github.com/SentrisCloud/dapp-starter/tree/main/contracts) - Example Solidity contracts for deployment on Sentrix.

## Infrastructure

- [SentrixScan](https://scan.sentrixchain.com) - Sentrix block explorer.
- [Obsidian Engine (Explorer V2)](https://github.com/SentrisCloud/sentrix-explorer-v2) - Rust + WASM block explorer. Coexists with SentrixScan on a separate domain. `Early`
- [Sentrix Faucet](https://faucet.sentrixchain.com) - SRX faucet for supported networks.
- [Indexer](https://github.com/SentrisCloud/indexer) - Indexer infrastructure for explorer and application data.
- [SentrisCloud Frontend](https://github.com/SentrisCloud/frontend) - Monorepo for explorer, faucet, wallet, DEX, launchpad, airdrop, and websites.

## Bridges

- [Sentrix Bridge](https://github.com/sentrix-labs/sentrix-bridge) - Hyperlane v3 bridge for SRX. Uses WSRX wrap + HypERC20Collateral to move value across networks.

### Routes

| Direction | Stack | Status |
| --- | --- | --- |
| Sentrix Testnet → Sepolia | Hyperlane v3 | Beta — manual relay, NoopIsm |

## Applications

- [SentrixScan](https://scan.sentrixchain.com) - Explorer for Sentrix mainnet and testnet.
- [Sentrix Faucet](https://faucet.sentrixchain.com) - Faucet for requesting SRX.
- [Solux Web Wallet](https://solux.sentriscloud.com) - Self-custody web wallet for Sentrix.
- [CoinBlast](https://coinblast.sentriscloud.com) - Memecoin launchpad for Sentrix. `Alpha`
- [Sentrix DEX](https://dex.sentrixchain.com) - AMM / DEX interface for Sentrix. `Early`
- [Sentrix Airdrop](https://airdrop.sentrixchain.com) - Airdrop eligibility and claim interface. `Early`

## Wallets

- [Solux Web Wallet](https://solux.sentriscloud.com) - Browser-based self-custody wallet.
- [Solux Mobile](https://github.com/SentrisCloud/solux) - Flutter mobile wallet for iOS and Android, self-custody and EVM-compatible. `In development`
- MetaMask - Sentrix supports Ethereum-compatible wallet flows through EVM RPC.

## Running a Node

Sentrix Chain validators are signer-only and run behind a firewall. Public RPC, JSON-RPC, and gRPC traffic is served by fullnodes that sit in front of the validator set.

Operational guidance lives in the core repos:

- [Sentrix Core Node](https://github.com/sentrix-labs/sentrix) - Build, configuration, runtime setup, and validator/fullnode roles.
- [Canonical Contracts](https://github.com/sentrix-labs/canonical-contracts) - Genesis-time contracts deployed alongside the chain.

A consolidated operator handbook is planned — progress is tracked in [#16](https://github.com/sentrix-labs/awesome-sentrix/issues/16).

## Tutorials

### Add Sentrix to MetaMask

Sentrix Chain is EVM-compatible, so mainnet and testnet both add as custom networks in MetaMask. Open **Settings → Networks → Add a network → Add a network manually** and use the values below.

#### Sentrix Chain (mainnet)

| Field | Value |
| --- | --- |
| Network name | `Sentrix Chain` |
| New RPC URL | `https://rpc.sentrixchain.com` |
| Chain ID | `7119` |
| Currency symbol | `SRX` |
| Block explorer URL | `https://scan.sentrixchain.com` |

#### Sentrix Testnet

| Field | Value |
| --- | --- |
| Network name | `Sentrix Testnet` |
| New RPC URL | `https://testnet-rpc.sentrixchain.com` |
| Chain ID | `7120` |
| Currency symbol | `SRX` |
| Block explorer URL | `https://scan-testnet.sentrixchain.com` |
| Faucet | `https://faucet.sentrixchain.com` |

Use the [Sentrix Faucet](https://faucet.sentrixchain.com) to request testnet SRX after adding Sentrix Testnet.

### Foundry config

Drop the RPC endpoints into `foundry.toml`:

```toml
[rpc_endpoints]
sentrix = "https://rpc.sentrixchain.com"
sentrix_testnet = "https://testnet-rpc.sentrixchain.com"
```

Sentrix uses Sourcify for contract verification at `https://verify.sentrixchain.com`. After deploying, verify with:

```bash
forge verify-contract \
  <ADDRESS> \
  src/MyContract.sol:MyContract \
  --chain-id 7119 \
  --verifier sourcify \
  --verifier-url https://verify.sentrixchain.com
```

Use `--chain-id 7120` for testnet.

### Hardhat config

Add the networks to `hardhat.config.ts`:

```ts
networks: {
  sentrix: {
    url: "https://rpc.sentrixchain.com",
    chainId: 7119,
    accounts: [process.env.PRIVATE_KEY!],
  },
  sentrixTestnet: {
    url: "https://testnet-rpc.sentrixchain.com",
    chainId: 7120,
    accounts: [process.env.PRIVATE_KEY!],
  },
},
```

For Sourcify verification, see the [`hardhat-verify`](https://hardhat.org/hardhat-runner/plugins/nomicfoundation-hardhat-verify) plugin and point the Sourcify URL at `https://verify.sentrixchain.com`.

Recommended tutorial topics:

- Get testnet SRX from the faucet
- Deploy a Solidity contract on Sentrix
- Read Sentrix blocks with viem
- Send an SRX transaction with ethers.js
- Run a Sentrix node
- Run a Sentrix validator
- Verify contracts with Sourcify

## Security

Report vulnerabilities privately.

- Protocol issues (chain, contracts, bridge, SDKs): [security@sentrixchain.com](mailto:security@sentrixchain.com) or a [private GitHub Security Advisory](https://github.com/sentrix-labs/sentrix/security/advisories/new).
- Application issues (explorer, wallet, faucet, launchpad): [security@sentriscloud.com](mailto:security@sentriscloud.com).
- Network or validator abuse: [abuse@sentrixchain.com](mailto:abuse@sentrixchain.com).

Core repos ship a `SECURITY.md` with the disclosure timeline, severity tiers, scope, and safe-harbor terms. See [`sentrix-labs/sentrix/SECURITY.md`](https://github.com/sentrix-labs/sentrix/blob/main/SECURITY.md) for the canonical example.

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
