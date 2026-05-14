<p align="center">
  <a href="https://sentrixchain.com">
    <img src="https://cdn.jsdelivr.net/gh/sentrix-labs/brand-kit@master/png-transparent/sentrix-256.png" alt="Sentrix Chain" width="128">
  </a>
</p>

<h1 align="center">Awesome Sentrix</h1>

<p align="center">
  <a href="https://awesome.re"><img src="https://awesome.re/badge-flat.svg" alt="Awesome"></a>
  <a href="https://github.com/sentrix-labs/awesome-sentrix/commits/main"><img src="https://img.shields.io/github/last-commit/sentrix-labs/awesome-sentrix?label=updated&color=8A5A11" alt="Last commit"></a>
  <a href="https://github.com/sentrix-labs/awesome-sentrix/actions/workflows/gitleaks.yml"><img src="https://img.shields.io/github/actions/workflow/status/sentrix-labs/awesome-sentrix/gitleaks.yml?branch=main&label=secret-scan" alt="Secret scan"></a>
  <a href="https://github.com/sentrix-labs/awesome-sentrix/actions/workflows/link-check.yml"><img src="https://img.shields.io/github/actions/workflow/status/sentrix-labs/awesome-sentrix/link-check.yml?branch=main&label=links" alt="Link check"></a>
  <a href="LICENSE"><img src="https://img.shields.io/badge/license-CC0--1.0-lightgrey" alt="License"></a>
</p>

<p align="center">
  <b>A curated list for <a href="https://sentrixchain.com">Sentrix Chain</a></b><br>
  Rust-based, EVM-compatible Layer-1. Resources, tooling, infrastructure, apps, and guides — both first-party and community-built.
</p>

<p align="center">
  <a href="https://sentrixchain.com">Website</a> ·
  <a href="https://scan.sentrixchain.com">Explorer</a> ·
  <a href="https://faucet.sentrixchain.com">Faucet</a> ·
  <a href="https://github.com/sentrix-labs/whitepaper">Whitepaper</a> ·
  <a href="https://t.me/SentrixChain">Telegram</a> ·
  <a href="https://discord.gg/sentrixchain">Discord</a> ·
  <a href="https://x.com/sentrixchain">X</a>
</p>

<p align="center">
  <sub>Read this in <a href="README.id.md">Bahasa Indonesia</a></sub>
</p>

---

> This list welcomes both first-party and community projects that are publicly accessible, actively maintained, and directly relevant to Sentrix Chain. Alpha or in-development projects are marked clearly. **Building on Sentrix?** Submit your project via PR — see [Contributing](#contributing).

## Who is this for

| You are… | Start at |
| --- | --- |
| 🛠️ **A Solidity developer** building dApps on Sentrix | [Developer Tools](#developer-tools) → [Tutorials](#tutorials) → [dApp Starter](https://github.com/SentrisCloud/dapp-starter) |
| 🦀 **A Rust developer** integrating with Sentrix nodes | [Rust SDK](https://github.com/SentrisCloud/sdk-rs) → [gRPC endpoints](#networks) |
| 🖧 **A node operator** running a validator or fullnode | [Running a Node](#running-a-node) |
| 👛 **A user** trying out the chain | [Add Sentrix to MetaMask](#add-sentrix-to-metamask) → [Faucet](https://faucet.sentrixchain.com) → [Solux wallet](https://solux.sentriscloud.com) |
| 🔒 **A security researcher** looking for in-scope targets | [Security](#security) |

## Contents

**Quickstart** — [Who is this for](#who-is-this-for) · [Start Here](#start-here) · [Official Links](#official-links) · [Networks](#networks)

**Build** — [Core Protocol](#core-protocol) · [Developer Tools](#developer-tools) · [Client Libraries](#client-libraries) · [Templates](#templates) · [Indexers](#indexers) · [Smart Contracts](#smart-contracts) · [Tokenomics](#tokenomics)

**Ecosystem** — [Infrastructure](#infrastructure) · [Bridges](#bridges) · [Applications](#applications) · [Wallets](#wallets)

**Operate** — [Running a Node](#running-a-node) · [Monitoring and Observability](#monitoring-and-observability) · [Governance](#governance)

**Reference** — [API Reference](#api-reference) · [Documentation](#documentation) · [Roadmap](#roadmap) · [Tutorials](#tutorials)

**Community** — [Grants and Ecosystem](#grants-and-ecosystem) · [Security](#security) · [Audits](#audits) · [Status Notes](#status-notes) · [FAQ](#faq) · [Glossary](#glossary) · [Contributing](#contributing)

---

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
- [Discord](https://discord.gg/sentrixchain) - Sentrix Discord server.

## Networks

> **One-click add to MetaMask:** [chainlist.org/?search=sentrix](https://chainlist.org/?search=sentrix) — auto-configures the network using the entries below. Sentrix Chain is registered with [`ethereum-lists/chains`](https://github.com/ethereum-lists/chains/blob/master/_data/chains/eip155-7119.json), so it also flows into viem, wagmi, RainbowKit, Web3Modal, and RabbyKit chain pickers automatically.

JSON-RPC URLs accept POSTs at the bare host (e.g. `https://rpc.sentrixchain.com`) or at the canonical `/rpc` path. The bare host also serves a self-documenting endpoint manifest as `GET /`. Native namespaces: `eth_`, `net_`, `web3_`, and `sentrix_` (validators, BFT, staking, delegations, finality).

### Mainnet

- Network Name: `Sentrix Chain`
- Chain ID: `7119`
- Currency Symbol: `SRX`
- JSON-RPC: `https://rpc.sentrixchain.com` (also `https://rpc.sentrixchain.com/rpc`)
- WebSocket: `wss://rpc.sentrixchain.com/ws` (`eth_subscribe` + `sentrix_subscribe` channels — `sentrix_finalized`, `sentrix_validatorSet`, `sentrix_tokenOps`, `sentrix_stakingOps`, `sentrix_jail`)
- Native REST API: `https://api.sentrixchain.com` (60+ endpoints — `/chain/info`, `/chain/blocks`, `/validators`, `/staking/validators`, `/tokens`, `/accounts/{address}`, `/transactions`, `/mempool`, `/epoch/current`)
- Live status: [`https://api.sentrixchain.com/sentrix_status`](https://api.sentrixchain.com/sentrix_status)
- gRPC: `grpc.sentrixchain.com:443` (service `sentrix.v1.Sentrix`)
- Explorer: [scan.sentrixchain.com](https://scan.sentrixchain.com) — built-in node explorer also at [`rpc.sentrixchain.com/explorer`](https://rpc.sentrixchain.com/explorer)

### Testnet

- Network Name: `Sentrix Testnet`
- Chain ID: `7120`
- Currency Symbol: `SRX`
- JSON-RPC: `https://testnet-rpc.sentrixchain.com` (also `https://testnet-rpc.sentrixchain.com/rpc`)
- WebSocket: `wss://testnet-rpc.sentrixchain.com/ws`
- Native REST API: `https://testnet-api.sentrixchain.com`
- Live status: [`https://testnet-api.sentrixchain.com/sentrix_status`](https://testnet-api.sentrixchain.com/sentrix_status)
- gRPC: `grpc-testnet.sentrixchain.com:443` (service `sentrix.v1.Sentrix`)
- Explorer: [scan-testnet.sentrixchain.com](https://scan-testnet.sentrixchain.com)
- Faucet: [faucet.sentrixchain.com](https://faucet.sentrixchain.com)

---

## Core Protocol

- [Sentrix Core Node](https://github.com/sentrix-labs/sentrix) - Core Rust implementation of the Sentrix Layer-1 Blockchain.
- [Whitepaper](https://github.com/sentrix-labs/whitepaper) - Sentrix Chain whitepaper and protocol narrative.
- [Canonical Contracts](https://github.com/sentrix-labs/canonical-contracts) - Official EVM contracts including WSRX, Multicall3, SentrixSafe, and TokenFactory.
- [Sentrix DEX Contracts](https://github.com/sentrix-labs/sentrix-dex) - Native AMM / DEX contracts for the Sentrix ecosystem.
- [Brand Kit](https://github.com/sentrix-labs/brand-kit) - Official logos, icons, banners, and brand assets.

## Developer Tools

General-purpose developer tools live here. Language-specific SDKs are in [Client Libraries](#client-libraries), Solidity starters in [Templates](#templates), and indexing infrastructure in [Indexers](#indexers).

- [Token List](https://github.com/sentrix-labs/token-list) - Canonical Uniswap-token-list-v1 registry for Sentrix mainnet (`7119`) and testnet (`7120`).
- [Brand Kit](https://github.com/sentrix-labs/brand-kit) - Logos, icons, marks for dApp UIs that integrate Sentrix.

## Client Libraries

### TypeScript

- [sdk-ts](https://github.com/SentrisCloud/sdk-ts) - Typed wrappers around the EVM JSON-RPC, native REST, and WebSocket subscription helpers.

### Rust

- [sdk-rs](https://github.com/SentrisCloud/sdk-rs) - Typed clients for native REST, EVM (via alloy), gRPC (via tonic), and secp256k1 wallet/signing. `Early`

### WebAssembly (browser)

- [sentrix-grpc-wasm](https://github.com/SentrisCloud/sentrix-grpc-wasm) - Rust + WebAssembly gRPC-Web client packaged via wasm-pack — usable from any browser dApp without a Node middleman. `Early`

## Templates

- [dApp Starter](https://github.com/SentrisCloud/dapp-starter) - Minimal Hardhat + viem dApp starter. Deploy ERC-20, wrap SRX, verify against Sourcify. End-to-end example for both networks.
- [dApp Starter Contracts](https://github.com/SentrisCloud/dapp-starter/tree/main/contracts) - Example Solidity contracts for deployment on Sentrix.

## Indexers

- [indexer-rs](https://github.com/SentrisCloud/indexer-rs) - Rust indexer (newer). Pipelined parallel backfill. Currently mainnet primary; testnet still on TS.
- [Indexer](https://github.com/SentrisCloud/indexer) - Postgres-backed REST indexer for blocks, transactions, logs, tokens, and native chain data. Etherscan-API-compatible. `Phase 1 / scaffold`

## Smart Contracts

- [Canonical Contracts](https://github.com/sentrix-labs/canonical-contracts) - WSRX, Multicall3, SentrixSafe, and TokenFactory.
- [Sentrix DEX](https://github.com/sentrix-labs/sentrix-dex) - AMM and liquidity infrastructure for SRX ecosystem markets.

### Deployed canonical addresses

Verified live (`eth_getCode` non-empty on the listed chain). Full source-of-truth at [`canonical-contracts/docs/ADDRESSES.md`](https://github.com/sentrix-labs/canonical-contracts/blob/main/docs/ADDRESSES.md).

| Contract | Mainnet (`7119`) | Testnet (`7120`) |
| --- | --- | --- |
| WSRX | `0x4693b113e523A196d9579333c4ab8358e2656553` | `0x85d5E7694AF31C2Edd0a7e66b7c6c92C59fF949A` |
| Multicall3 | `0xFd4b34b5763f54a580a0d9f7997A2A993ef9ceE9` | `0x7900826De548425c6BE56caEbD4760AB0155Cd54` |
| TokenFactory | `0xc753199b723649ab92c6db8A45F158921CFDEe49` | `0x7A2992af0d4979aDD076347666023d66d29276Fc` |
| SentrixSafe | `0x6272dC0C842F05542f9fF7B5443E93C0642a3b26` | `0xc9D7a61D7C2F428F6A055916488041fD00532110` |

## Tokenomics

SRX has a hard cap of **315,000,000** post the tokenomics-v2 fork (mainnet activation `h=640800`, 2026-04-26). The economic shape mirrors Bitcoin's halving curve, scaled for Sentrix's 1-second blocks.

| Field | Value |
| --- | --- |
| Hard cap | 315,000,000 SRX |
| Premine | 63,000,000 SRX (20%) — Founder 21M, Ecosystem 21M, Early Validator 10.5M, Reserve 10.5M |
| Block rewards | up to 252,000,000 SRX (80%) |
| Initial reward | 1 SRX per block |
| Halving | every 126,000,000 blocks (~4 years at 1-second blocks, BTC parity) |
| Smallest unit | `sentri` (1 SRX = 10⁸ sentri, u64 internal) |
| Fee model | 50% burn / 50% validator |
| Live circulating | [`api.sentrixchain.com/chain/info`](https://api.sentrixchain.com/chain/info) returns `circulating_supply_srx` |

Full breakdown of native coin mechanics, staking, reward escrow, token standards, and airdrop rules:

- [SRX coin spec](https://github.com/sentrix-labs/sentrix/blob/main/docs/tokenomics/SRX.md)
- [Tokenomics overview](https://github.com/sentrix-labs/sentrix/blob/main/docs/tokenomics/OVERVIEW.md)
- [Staking](https://github.com/sentrix-labs/sentrix/blob/main/docs/tokenomics/STAKING.md)
- [Token standards](https://github.com/sentrix-labs/sentrix/blob/main/docs/tokenomics/TOKEN_STANDARDS.md)
- [Reward escrow](https://github.com/sentrix-labs/sentrix/blob/main/docs/tokenomics/REWARD_ESCROW.md)
- [Airdrop mechanics](https://github.com/sentrix-labs/sentrix/blob/main/docs/tokenomics/AIRDROP_MECHANICS.md)

---

## Infrastructure

- [SentrixScan](https://scan.sentrixchain.com) - Sentrix block explorer.
- [Obsidian Engine (Explorer V2)](https://github.com/SentrisCloud/sentrix-explorer-v2) - Rust + WebAssembly block explorer. Coexists with SentrixScan on a separate domain. `Early`
- [Sentrix Faucet](https://faucet.sentrixchain.com) - SRX faucet for supported networks.
- [Indexer](https://github.com/SentrisCloud/indexer) - Indexer infrastructure for explorer and application data.
- [SentrisCloud Frontend](https://github.com/SentrisCloud/frontend) - Monorepo for explorer, faucet, wallet, DEX, launchpad, airdrop, and websites.

## Bridges

- [Sentrix Bridge](https://github.com/sentrix-labs/sentrix-bridge) - Hyperlane v3 + LayerZero V2 bridge stack for SRX. Uses WSRX wrap + HypERC20Collateral path; HypNative path also functional after sentrix#580 close (2026-05-13). Also hosts the watcher + status API below.
- [Bridge Watcher](https://github.com/sentrix-labs/sentrix-bridge/tree/main/watcher-rs) - Rust CLI that monitors route safety, NoopIsm exposure, MultisigIsm validator config, WSRX 1:1 collateral invariant, RPC health, stuck messages.
- [Bridge Status API](https://bridge-api.sentrixchain.com) - HTTP status API for bridge state. Endpoints: `/health`, `/status`, `/routes`, `/messages`, `/unsafe-config`, `/fresh-user-flow`, `/readiness`. Source at [`api-rs/`](https://github.com/sentrix-labs/sentrix-bridge/tree/main/api-rs).

### Routes

| Direction | Stack | Status |
| --- | --- | --- |
| Sentrix Testnet → Sepolia | Hyperlane v3 | Beta — manual relay, NoopIsm (testnet/demo only) |
| Sentrix Testnet ↔ <other testnets> | Hyperlane v3 | Planned — see [`docs/multichain-roadmap.md`](https://github.com/sentrix-labs/sentrix-bridge/blob/main/docs/multichain-roadmap.md) |

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

---

## Running a Node

### Validator vs fullnode

Sentrix Chain separates two roles:

- **Validator** — signs blocks. Runs behind a firewall, exposes nothing public, and talks libp2p to other validators (and optionally to a private fullnode for relay).
- **Fullnode** — relays the public JSON-RPC, WSS, native REST, and gRPC traffic that dApps and explorers hit. Sits in front of the validator set, on its own host where practical.

The recommended shape is one validator per host plus a dedicated fullnode for public traffic. Validator hosts should never serve public RPC.

### Hardware minimums

| Resource | Minimum |
| --- | --- |
| OS | Ubuntu 22.04 / 24.04 (x86_64 or aarch64) |
| RAM | 8 GiB |
| Swap | 8 GiB (persistent — `chain.db` is memory-mapped, swap must cover it) |
| Disk | 60 GiB |
| Rust toolchain | 1.95+ (handled by installer) |

### Install

```bash
curl -fsSL https://raw.githubusercontent.com/sentrix-labs/sentrix/main/scripts/install-validator.sh | bash
```

The script handles pre-flight checks, apt deps, Rust via `rustup`, source clone + `cargo build --release -p sentrix-node`, keystore generation, systemd unit, and start. Idempotent — re-runs repair rather than clobber.

After the node is healthy, check it locally:

```bash
curl http://localhost:8545/health
```

### Become a validator

Sentrix is permissioned-onboarding for now: anyone can run the binary, but joining the active set is co-signed by the chain admin.

1. Run the installer above and wait until the node is fully synced.
2. Email **`validators@sentrixchain.com`** with:
   - Validator address + pubkey (printed by the installer)
   - Intended self-stake — minimum **15,000 SRX**
   - Ops contact (email or Telegram for incident coordination)
3. An activation height comes back. After that height your validator appears in [`/staking/validators`](https://api.sentrixchain.com/staking/validators) and at [scan.sentrixchain.com/validators](https://scan.sentrixchain.com/validators).

### Service management

The installer drops a systemd unit. Common operator commands:

```bash
sudo systemctl status sentrix
sudo journalctl -u sentrix -f --since "1 hour ago"
sudo systemctl restart sentrix
```

### Healthchecks (local)

Hit your node's bind address (default `localhost:8545`):

| Endpoint | What it returns |
| --- | --- |
| `GET /health` | 200 OK if the process is responsive |
| `GET /sentrix_status` | latest height, sync state, active validator count |
| `GET /metrics` | Prometheus-format metrics |

### Inspect from anywhere

Public surfaces work without a local node:

```bash
curl https://api.sentrixchain.com/sentrix_status      # mainnet height, sync, validator count
curl https://api.sentrixchain.com/staking/validators  # active validator set
curl https://api.sentrixchain.com/epoch/current       # current epoch
curl https://api.sentrixchain.com/mempool             # mempool snapshot
```

### Operator handbook

The deep operator material lives in `sentrix/docs/operations/`:

| Topic | Document |
| --- | --- |
| Full runbook | [VALIDATOR_GUIDE.md](https://github.com/sentrix-labs/sentrix/blob/main/docs/operations/VALIDATOR_GUIDE.md) |
| Step-by-step join | [VALIDATOR_ONBOARDING.md](https://github.com/sentrix-labs/sentrix/blob/main/docs/operations/VALIDATOR_ONBOARDING.md) |
| What to watch | [MONITORING.md](https://github.com/sentrix-labs/sentrix/blob/main/docs/operations/MONITORING.md) |
| Prometheus + dashboards | [OBSERVABILITY.md](https://github.com/sentrix-labs/sentrix/blob/main/docs/operations/OBSERVABILITY.md) |
| Incident response | [EMERGENCY_ROLLBACK.md](https://github.com/sentrix-labs/sentrix/blob/main/docs/operations/EMERGENCY_ROLLBACK.md) |
| Testnet-specific recovery | [TESTNET_RECOVERY.md](https://github.com/sentrix-labs/sentrix/blob/main/docs/operations/TESTNET_RECOVERY.md) |
| Network reference | [NETWORKS.md](https://github.com/sentrix-labs/sentrix/blob/main/docs/operations/NETWORKS.md) |
| WSS subscriptions | [WEBSOCKET_SUBSCRIPTIONS.md](https://github.com/sentrix-labs/sentrix/blob/main/docs/operations/WEBSOCKET_SUBSCRIPTIONS.md) |

For incident coordination and onboarding questions, email **`validators@sentrixchain.com`**. Closes [#16](https://github.com/sentrix-labs/awesome-sentrix/issues/16).

## Monitoring and Observability

Sentrix nodes ship Prometheus metrics and structured status endpoints out of the box. Public surfaces are also available for off-host monitoring.

### Local (on the node)

| Endpoint | What it returns |
| --- | --- |
| `GET /health` | 200 OK if the process is responsive. |
| `GET /sentrix_status` | Latest height, sync state, active validator count, uptime seconds, build version. |
| `GET /sentrix_status_extended` | Status with extra runtime fields. |
| `GET /metrics` | Prometheus-format metrics for scraping. |

### Public

| Endpoint | What it returns |
| --- | --- |
| [`api.sentrixchain.com/sentrix_status`](https://api.sentrixchain.com/sentrix_status) | Mainnet status |
| [`testnet-api.sentrixchain.com/sentrix_status`](https://testnet-api.sentrixchain.com/sentrix_status) | Testnet status |
| [`api.sentrixchain.com/chain/info`](https://api.sentrixchain.com/chain/info) | Live circulating supply, max supply, active validators, mempool size, next block reward |
| [`api.sentrixchain.com/staking/validators`](https://api.sentrixchain.com/staking/validators) | Active validator set |
| [`api.sentrixchain.com/epoch/current`](https://api.sentrixchain.com/epoch/current) | Current epoch, validator set, rewards |
| [`bridge-api.sentrixchain.com/readiness`](https://bridge-api.sentrixchain.com/readiness) | Bridge production-readiness checklist |
| [`bridge-api.sentrixchain.com/unsafe-config`](https://bridge-api.sentrixchain.com/unsafe-config) | Routes still using NoopIsm or otherwise flagged unsafe |
| [`bridge-api.sentrixchain.com/routes`](https://bridge-api.sentrixchain.com/routes) | All bridge routes with origin/destination/ISM type |

### Reference docs

- [MONITORING.md](https://github.com/sentrix-labs/sentrix/blob/main/docs/operations/MONITORING.md) - What to watch: liveness, lag, mempool signals, threshold guidance.
- [OBSERVABILITY.md](https://github.com/sentrix-labs/sentrix/blob/main/docs/operations/OBSERVABILITY.md) - Prometheus scrape config, Grafana dashboard wiring.

## Governance

Sentrix Chain runs **permissioned-onboarding** today: the consensus is open and the binary is the same one anyone can build, but admission to the active validator set is co-signed by the chain admin. The plan is to migrate from a single-key authority to N-of-M as the validator base grows.

| Surface | Mechanism today | Target |
| --- | --- | --- |
| Validator set | Admin co-signs activation height for each onboarded validator | On-chain admission tied to self-stake + slashing |
| Canonical contract upgrades | Contracts are immutable; "deploy v2 + migrate" is the upgrade path | Same — immutability is deliberate |
| Safe-governed actions | `SentrixSafe` on both networks is currently 1-of-1 with a single authority signer | N-of-M as co-signers are recruited |
| Slashing / jailing | Liveness + double-sign evidence dispatched on-chain via `SubmitEvidence` and `JailEvidenceBundle` | Same |

Authority signer addresses, Safe migration history, and verification commands live in the canonical contracts repo at [`canonical-contracts/docs/ADDRESSES.md`](https://github.com/sentrix-labs/canonical-contracts/blob/main/docs/ADDRESSES.md). Multisig design and threat model: [`sentrix/docs/security/MULTISIG.md`](https://github.com/sentrix-labs/sentrix/blob/main/docs/security/MULTISIG.md).

---

## API Reference

The native node speaks four namespaces on a single port:

| Namespace | Examples |
| --- | --- |
| `eth_` | `eth_chainId`, `eth_blockNumber`, `eth_getBalance`, `eth_getCode`, `eth_sendRawTransaction`, `eth_call` — Ethereum-compatible (MetaMask, ethers.js, viem, web3.js, hardhat) |
| `net_` | Network info |
| `web3_` | Client version |
| `sentrix_` | Native operations — validators, BFT, staking, delegations, finality, jail evidence |

REST surface (60+ endpoints, full list at [`api.sentrixchain.com`](https://api.sentrixchain.com)):

- `/chain/info`, `/chain/blocks`, `/chain/blocks/{height}`
- `/transactions`, `/transactions/{txid}`, `/mempool`
- `/accounts/{address}`, `/accounts/{address}/balance`, `/accounts/{address}/code`, `/accounts/{address}/nonce`
- `/address/{address}`, `/address/{address}/history`
- `/staking/validators`, `/validators`, `/epoch/current`
- `/tokens`, `/tokens/{contract}`
- `/sentrix_status`, `/sentrix_status_extended`, `/health`, `/metrics`

Deep references in the core repo:

- [API_REFERENCE.md](https://github.com/sentrix-labs/sentrix/blob/main/docs/operations/API_REFERENCE.md) — full JSON-RPC + REST method coverage.
- [API_ENDPOINTS.md](https://github.com/sentrix-labs/sentrix/blob/main/docs/operations/API_ENDPOINTS.md) — endpoint catalog with examples.
- [GRPC.md](https://github.com/sentrix-labs/sentrix/blob/main/docs/operations/GRPC.md) — Tonic gRPC + gRPC-Web (`sentrix.v1.Sentrix`).
- [WEBSOCKET_SUBSCRIPTIONS.md](https://github.com/sentrix-labs/sentrix/blob/main/docs/operations/WEBSOCKET_SUBSCRIPTIONS.md) — `eth_subscribe` + `sentrix_subscribe` channels.
- [TRACE_RPC_SPEC.md](https://github.com/sentrix-labs/sentrix/blob/main/docs/operations/TRACE_RPC_SPEC.md) — debug/trace methods.
- [EIP1559_SPEC.md](https://github.com/sentrix-labs/sentrix/blob/main/docs/operations/EIP1559_SPEC.md) — fee market spec.

## Documentation

The core repo's `docs/` tree is organized by topic:

### Architecture

- [OVERVIEW.md](https://github.com/sentrix-labs/sentrix/blob/main/docs/architecture/OVERVIEW.md) - System-level architecture.
- [CONSENSUS.md](https://github.com/sentrix-labs/sentrix/blob/main/docs/architecture/CONSENSUS.md) - DPoS + BFT consensus design.
- [EVM.md](https://github.com/sentrix-labs/sentrix/blob/main/docs/architecture/EVM.md) - EVM adapter, revm internals.
- [NETWORKING.md](https://github.com/sentrix-labs/sentrix/blob/main/docs/architecture/NETWORKING.md) - libp2p, Noise XX, Kademlia, Gossipsub layers.
- [STATE.md](https://github.com/sentrix-labs/sentrix/blob/main/docs/architecture/STATE.md) - Binary sparse Merkle tree, MDBX storage.
- [TRANSACTIONS.md](https://github.com/sentrix-labs/sentrix/blob/main/docs/architecture/TRANSACTIONS.md) - Native and EVM transaction lifecycle.

### Operations

Full operations index: [`sentrix/docs/operations/`](https://github.com/sentrix-labs/sentrix/tree/main/docs/operations). Highlights:

- [DEVELOPER_QUICKSTART.md](https://github.com/sentrix-labs/sentrix/blob/main/docs/operations/DEVELOPER_QUICKSTART.md) - Build + run a node in five minutes.
- [MONITORING.md](https://github.com/sentrix-labs/sentrix/blob/main/docs/operations/MONITORING.md) - Liveness, lag, mempool signals.
- [OBSERVABILITY.md](https://github.com/sentrix-labs/sentrix/blob/main/docs/operations/OBSERVABILITY.md) - Prometheus metrics + dashboards.
- [CONTRACT_VERIFICATION.md](https://github.com/sentrix-labs/sentrix/blob/main/docs/operations/CONTRACT_VERIFICATION.md) - Sourcify-based contract verification flow.
- [SMART_CONTRACT_GUIDE.md](https://github.com/sentrix-labs/sentrix/blob/main/docs/operations/SMART_CONTRACT_GUIDE.md) - Deploy via Remix end-to-end.
- [EMERGENCY_ROLLBACK.md](https://github.com/sentrix-labs/sentrix/blob/main/docs/operations/EMERGENCY_ROLLBACK.md) - Incident response procedures.

### Security

- [MULTISIG.md](https://github.com/sentrix-labs/sentrix/blob/main/docs/security/MULTISIG.md) - SentrixSafe ownership and threshold design.
- [ATTACK_VECTORS.md](https://github.com/sentrix-labs/sentrix/blob/main/docs/security/ATTACK_VECTORS.md) - Threat model.
- [AUDIT_SUMMARY.md](https://github.com/sentrix-labs/sentrix/blob/main/docs/security/AUDIT_SUMMARY.md) - Audit history overview.
- [SECURITY_REPORT.md](https://github.com/sentrix-labs/sentrix/blob/main/docs/security/SECURITY_REPORT.md) - Detailed security report.

### Governance

- [GOVERNANCE.md](https://github.com/sentrix-labs/sentrix/blob/main/docs/GOVERNANCE.md) - Governance principles and decision-making model.

## Roadmap

Sentrix Chain's roadmap is tracked as four phase docs in the core repo. Each phase is independently scoped — the docs list completion criteria, not just intent.

- [Phase 1](https://github.com/sentrix-labs/sentrix/blob/main/docs/roadmap/PHASE1.md) - Mainnet readiness — consensus, EVM compatibility, validator set, base contracts.
- [Phase 2](https://github.com/sentrix-labs/sentrix/blob/main/docs/roadmap/PHASE2.md) - Ecosystem buildout — bridges, SDKs, DEX, indexer, explorer.
- [Phase 3](https://github.com/sentrix-labs/sentrix/blob/main/docs/roadmap/PHASE3.md) - Decentralization — multi-sig admin, broader validator onboarding, governance handoff.
- [CHANGELOG](https://github.com/sentrix-labs/sentrix/blob/main/docs/roadmap/CHANGELOG.md) - Release history with what shipped in each tag.

## Tutorials

### Add Sentrix to MetaMask

**Fastest path:** visit [chainlist.org/?search=sentrix](https://chainlist.org/?search=sentrix), connect MetaMask, click **Add to MetaMask** on the network you want. Sentrix is registered in [`ethereum-lists/chains`](https://github.com/ethereum-lists/chains) so the same one-click flow works in any wallet picker that consumes that registry.

**Manual fallback:** Sentrix Chain is EVM-compatible, so mainnet and testnet both add as custom networks in MetaMask. Open **Settings → Networks → Add a network → Add a network manually** and use the values below.

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

### Get testnet SRX from the faucet

1. Open the [Sentrix Faucet](https://faucet.sentrixchain.com).
2. Switch the network selector to **Sentrix Testnet**.
3. Paste your EVM-compatible wallet address (for example, from MetaMask).
4. Pass the Cloudflare Turnstile challenge.
5. Submit the request. The tx hash appears below the form — open it in [scan-testnet.sentrixchain.com](https://scan-testnet.sentrixchain.com) to confirm finalization.

The faucet drips a small amount per request and applies a per-address cooldown. Wait out the cooldown if you need more.

### Read Sentrix blocks with viem

Once [wevm/viem#4603](https://github.com/wevm/viem/pull/4603) merges, the chain config ships built-in:

```ts
import { createPublicClient, http } from 'viem'
import { sentrix } from 'viem/chains'  // also: sentrixTestnet

const client = createPublicClient({ chain: sentrix, transport: http() })

const block = await client.getBlock()
console.log(`block ${block.number} has ${block.transactions.length} txs`)
```

Until then, inline the chain config:

```ts
import { createPublicClient, http, defineChain } from 'viem'

export const sentrix = defineChain({
  id: 7119,
  name: 'Sentrix Chain',
  nativeCurrency: { name: 'Sentrix', symbol: 'SRX', decimals: 18 },
  rpcUrls: { default: { http: ['https://rpc.sentrixchain.com'] } },
  blockExplorers: { default: { name: 'SentrixScan', url: 'https://scan.sentrixchain.com' } },
})

const client = createPublicClient({ chain: sentrix, transport: http() })
const block = await client.getBlock()
const balance = await client.getBalance({ address: '0x0000000000000000000000000000000000000000' })
```

For testnet, use `id: 7120` and `https://testnet-rpc.sentrixchain.com`.

### Connect a wallet with wagmi

`wagmi` is the React hooks layer on top of viem. Configure once and every `useAccount` / `useReadContract` / `useWriteContract` hook in the app gets Sentrix automatically.

```ts
import { http, createConfig } from 'wagmi'
import { sentrix, sentrixTestnet } from 'viem/chains'  // post-merge of viem #4603
import { injected, walletConnect } from 'wagmi/connectors'

export const config = createConfig({
  chains: [sentrix, sentrixTestnet],
  connectors: [
    injected(),
    walletConnect({ projectId: process.env.NEXT_PUBLIC_WC_PROJECT_ID! }),
  ],
  transports: {
    [sentrix.id]: http(),
    [sentrixTestnet.id]: http(),
  },
})
```

For RainbowKit / ConnectKit / Reown AppKit (formerly Web3Modal) / RabbyKit, drop `sentrix` and `sentrixTestnet` into the same `chains` array — those pickers consume the viem chain registry directly.

### More tutorials

These are tracked as open issues — pull requests welcome:

- Deploy a Solidity contract on Sentrix (covered partially by [dApp Starter](https://github.com/SentrisCloud/dapp-starter))
- Send an SRX transaction with viem / ethers.js
- Run a Sentrix fullnode
- Run a Sentrix validator (see [Running a Node](#running-a-node) and [#16](https://github.com/sentrix-labs/awesome-sentrix/issues/16))
- Verify contracts with Sourcify (covered by [Foundry config](#foundry-config))

---

## Grants and Ecosystem

Sentrix Labs and SentrisCloud run separate contact lanes for each kind of partnership:

| Lane | Email | What it's for |
| --- | --- | --- |
| Grants | `grants@sentrixchain.com` | Ecosystem grant proposals, build-on-Sentrix funding |
| Builders | `builders@sentrixchain.com` | dApp inquiries, integration questions, technical onboarding |
| Validators | `validators@sentrixchain.com` | Validator activation, ops coordination, incident response |
| Partnerships | `partners@sentriscloud.com` | Exchange listings, infrastructure providers, business deals |
| Security | `security@sentrixchain.com` | Vulnerability disclosure (see [Security](#security)) |
| General support | `support@sentrixchain.com` | User-facing support |

For Founder / maintainer direct sponsorship, see the **Sponsor** link on the [Sentrix Labs profile](https://github.com/sentrix-labs).

## Security

Report vulnerabilities privately.

- Protocol issues (chain, contracts, bridge, SDKs): [security@sentrixchain.com](mailto:security@sentrixchain.com) or a [private GitHub Security Advisory](https://github.com/sentrix-labs/sentrix/security/advisories/new).
- Application issues (explorer, wallet, faucet, launchpad): [security@sentriscloud.com](mailto:security@sentriscloud.com).
- Network or validator abuse: [abuse@sentrixchain.com](mailto:abuse@sentrixchain.com).

Core repos ship a `SECURITY.md` with the disclosure timeline, severity tiers, scope, and safe-harbor terms. See [`sentrix-labs/sentrix/SECURITY.md`](https://github.com/sentrix-labs/sentrix/blob/main/SECURITY.md) for the canonical example.

## Audits

**External audit status:** no third-party audit firm has reviewed Sentrix Chain code yet. Treat the codebase accordingly when sizing exposure.

Internal review posture:

- Multiple rounds of internal code review (SECURITY_AUDIT_V11 is the most recent — 39 files, ~6,500 LoC).
- Topical audits on BFT consensus, EVM integration and gas accounting, dependency supply chain, CI/CD posture, validator infrastructure, and tokenomics correctness.
- `cargo audit` and `gitleaks` gate every PR.
- `slither` and `mythril` gate every Solidity PR.

Canonical hub (audit history, scope, methodology):

- [AUDIT_SUMMARY.md](https://github.com/sentrix-labs/sentrix/blob/main/docs/security/AUDIT_SUMMARY.md) - Navigation index for all security material.
- [SECURITY_AUDIT_V11.md](https://github.com/sentrix-labs/sentrix/blob/main/docs/security/SECURITY_AUDIT_V11.md) - Most recent code review.
- [SECURITY_REPORT.md](https://github.com/sentrix-labs/sentrix/blob/main/docs/security/SECURITY_REPORT.md) - Cumulative summary.
- [PENTEST_RESULTS.md](https://github.com/sentrix-labs/sentrix/blob/main/docs/security/PENTEST_RESULTS.md) - Penetration test methodology + raw results.
- [ATTACK_VECTORS.md](https://github.com/sentrix-labs/sentrix/blob/main/docs/security/ATTACK_VECTORS.md) - Threat model.

## Status Notes

- CoinBlast is currently marked as `Alpha`.
- Sentrix DEX is currently marked as `Early`.
- Solux Mobile is `In development`.
- The indexer is `Phase 1 / scaffold`.
- Some older app repositories under `sentrix-labs` are archived because they were consolidated into `SentrisCloud/frontend`.

## FAQ

### What is Sentrix Chain?

A Layer-1 Blockchain written in Rust with EVM compatibility. 1-second blocks, instant BFT finality, DPoS consensus, and a fixed 315M SRX supply on a 4-year halving curve. Solidity tools (Foundry, Hardhat, MetaMask, viem, ethers.js) connect natively via JSON-RPC.

### Why Rust if the chain is EVM-compatible?

The execution layer is EVM (via `revm`) so Solidity contracts run unmodified, but everything around it — consensus, storage, networking, RPC, gRPC — is Rust. The choice is about safety and performance of the surrounding system, not about asking developers to write Rust contracts.

### What is the difference between SRX and WSRX?

`SRX` is the native gas asset (no contract — it's the chain coin). `WSRX` is the canonical ERC-20 wrapper deployed at fixed addresses on both networks (see [Deployed canonical addresses](#deployed-canonical-addresses)). Wrap when an EVM-side flow needs an ERC-20 (DEX swaps, bridge collateral). Unwrap to get native SRX back.

### Is mainnet stable?

Mainnet is live and producing blocks (see [`/sentrix_status`](https://api.sentrixchain.com/sentrix_status) for current height + uptime). The codebase is under active development — internal review only, no third-party audit yet. Treat exposure accordingly.

### How do I get testnet SRX?

Open [`faucet.sentrixchain.com`](https://faucet.sentrixchain.com), switch to Sentrix Testnet, paste an EVM address, pass Turnstile, submit. Full walkthrough in [Tutorials → Get testnet SRX](#get-testnet-srx-from-the-faucet).

### Can I run my own validator?

Yes. The binary is open and the same one anyone can build. Joining the active set is co-signed by the chain admin today (see [Governance](#governance)). Hardware minimums, install one-liner, and onboarding flow are in [Running a Node](#running-a-node).

### What is BFT finality?

Once a block has at least 2/3 + 1 validator votes, it is finalized — no reorgs after that point. Different from Bitcoin / Ethereum probabilistic finality, where you wait for confirmations. Subscribe to `sentrix_finalized` over WSS to receive finalization events (see [WSS subscriptions](https://github.com/sentrix-labs/sentrix/blob/main/docs/operations/WEBSOCKET_SUBSCRIPTIONS.md)).

### What is "permissioned-onboarding"?

The validator set is open in code but admission is gated by an admin signature today. The plan is to migrate from a single-key authority to N-of-M as the validator base grows. See [Governance](#governance).

### How do I bridge to or from Sentrix?

A Hyperlane v3 bridge moves SRX between Sentrix Testnet and Sepolia via the WSRX wrap path. See [Bridges](#bridges) for the route table and status. Mainnet-out bridges are not deployed yet.

### Has the code been audited externally?

Not yet. Internal audits are documented under [Audits](#audits). External audit will be commissioned when budget and scope align — no committed timeline.

### How do I list a token on the canonical token list?

Open a PR to [`sentrix-labs/token-list`](https://github.com/sentrix-labs/token-list) with the token's contract address (deployed on mainnet `7119` or testnet `7120`), symbol, decimals, and logo URI. PRs that add tokens without a deployed contract are closed.

## Glossary

| Term | Meaning |
| --- | --- |
| `SRX` | Native gas asset of Sentrix Chain. |
| `WSRX` | Canonical ERC-20 wrapper of SRX, deployed at fixed addresses on mainnet and testnet. |
| `sentri` | Smallest unit: `1 SRX = 10^8 sentri`. All internal arithmetic is `u64` in `sentri`. |
| BFT | Byzantine Fault Tolerant. Consensus tolerates up to 1/3 dishonest validators while still finalizing blocks. |
| DPoS | Delegated Proof of Stake. Token holders delegate stake to validators who produce blocks. |
| Voyager | Codename for the current consensus engine (DPoS + BFT). Activated as the mainnet protocol mode. |
| Halving | Block-reward halving every 126M blocks (~4 years at 1-second blocks). BTC-parity schedule. |
| Premine | The 63M SRX (20% of cap) allocated at genesis to Founder, Ecosystem, Early Validator, and Reserve buckets. |
| Self-stake | A validator's own bonded SRX. Minimum 15,000 SRX to be considered for activation. |
| Jailing | A validator that misses liveness or double-signs is jailed (removed from the active set) via on-chain evidence dispatch. |
| Slashing | Stake confiscation that accompanies severe jail events (e.g. double-sign). |
| Authority signer | The current single-key admin EOA that co-signs validator activations and Safe-governed actions. |
| `SentrixSafe` | Canonical Safe contract on each network. Currently 1-of-1 with the authority signer; targets N-of-M. |
| MDBX | The memory-mapped key-value store backing `chain.db`. Used by Reth and Erigon for the same reason — high read throughput for the trie. |
| `revm` | The Rust EVM implementation used as Sentrix's execution adapter. |
| libp2p | The peer-to-peer networking stack. Noise XX for encryption, Kademlia for discovery, Gossipsub for messages. |
| Sourcify | The contract-verification standard Sentrix uses. Self-hosted at [`verify.sentrixchain.com`](https://verify.sentrixchain.com). |
| NoopIsm | A Hyperlane Interchain Security Module that accepts any message. Used in the testnet bridge today; production target is MultisigIsm. |
| MultisigIsm | The Hyperlane ISM that requires N-of-M validator signatures on bridge messages — production target. |

## Contributing

Contributions are welcome — from anyone building on, integrating with, or running infrastructure for Sentrix Chain.

**Building on Sentrix?** Submit your project via PR. The list groups projects by category (Applications, Wallets, Bridges, Developer Tools, Client Libraries, Templates, Indexers, Infrastructure) — open a PR adding your entry to the section that fits. Use the existing entries as a format reference.

Good contributions include:

- dApps, launchpads, DEXes, NFT platforms, and other applications running on Sentrix.
- Wallets, browser extensions, and signing tools that support Sentrix Chain.
- SDKs and client libraries in any language.
- Validator services, RPC providers, and infrastructure tooling.
- Bridges and cross-chain integrations.
- Indexers, explorers, and data services.
- Tutorials, RPC examples, SDK examples, validator guides.
- Corrections for outdated or broken links.

**Quality bar:** publicly accessible, directly related to Sentrix Chain, actively maintained, not misleading, not purely promotional. Pre-launch projects are fine if marked clearly (`Alpha`, `Early`, `In development`).

Read [CONTRIBUTING.md](CONTRIBUTING.md) for the full submission format and review process.

---

<p align="center">
  <sub>
    Built with care for the <a href="https://sentrixchain.com">Sentrix Chain</a> ecosystem.<br>
    Open under <a href="LICENSE">CC0-1.0</a> — copy, fork, remix freely.
  </sub>
</p>
