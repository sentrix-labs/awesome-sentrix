# Awesome Sentrix [![Awesome](https://awesome.re/badge-flat.svg)](https://awesome.re) [![Last commit](https://img.shields.io/github/last-commit/sentrix-labs/awesome-sentrix?label=updated)](https://github.com/sentrix-labs/awesome-sentrix/commits/main) [![Secret scan](https://img.shields.io/github/actions/workflow/status/sentrix-labs/awesome-sentrix/gitleaks.yml?branch=main&label=secret-scan)](https://github.com/sentrix-labs/awesome-sentrix/actions/workflows/gitleaks.yml)

> A curated list of official resources, developer tools, infrastructure, applications, and guides for **Sentrix Chain**.

<p align="center">
  <a href="https://sentrixchain.com">Website</a> ·
  <a href="https://scan.sentrixchain.com">Explorer</a> ·
  <a href="https://faucet.sentrixchain.com">Faucet</a> ·
  <a href="https://github.com/sentrix-labs/whitepaper">Whitepaper</a> ·
  <a href="https://t.me/SentrixChain">Telegram</a> ·
  <a href="https://x.com/sentrixchain">X</a>
</p>

**Sentrix Chain** is a Rust-based, EVM-compatible Layer-1 Blockchain focused on protocol engineering, validator infrastructure, RPC compatibility, staking, and developer tooling. _Read this in [Bahasa Indonesia](README.id.md)._

> This list focuses on official and actively maintained Sentrix resources. Alpha or in-development projects are marked clearly.

## Who is this for

| You are… | Start at |
| --- | --- |
| **A Solidity developer** building dApps on Sentrix | [Developer Tools](#developer-tools) → [Tutorials](#tutorials) → [dApp Starter](https://github.com/SentrisCloud/dapp-starter) |
| **A Rust developer** integrating with Sentrix nodes | [Rust SDK](https://github.com/SentrisCloud/sdk-rs) → [gRPC endpoints](#networks) |
| **A node operator** running a validator or fullnode | [Running a Node](#running-a-node) |
| **A user** trying out the chain | [Add Sentrix to MetaMask](#add-sentrix-to-metamask) → [Faucet](https://faucet.sentrixchain.com) → [Solux wallet](https://solux.sentriscloud.com) |
| **A security researcher** looking for in-scope targets | [Security](#security) |

## Contents

- [Who is this for](#who-is-this-for)
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

## Core Protocol

- [Sentrix Core Node](https://github.com/sentrix-labs/sentrix) - Core Rust implementation of the Sentrix Layer-1 Blockchain.
- [Whitepaper](https://github.com/sentrix-labs/whitepaper) - Sentrix Chain whitepaper and protocol narrative.
- [Canonical Contracts](https://github.com/sentrix-labs/canonical-contracts) - Official EVM contracts including WSRX, Multicall3, SentrixSafe, and TokenFactory.
- [Sentrix DEX Contracts](https://github.com/sentrix-labs/sentrix-dex) - Native AMM / DEX contracts for the Sentrix ecosystem.
- [Brand Kit](https://github.com/sentrix-labs/brand-kit) - Official logos, icons, banners, and brand assets.

## Developer Tools

- [dApp Starter](https://github.com/SentrisCloud/dapp-starter) - End-to-end starter for deploying and interacting with contracts on Sentrix.
- [TypeScript SDK](https://github.com/SentrisCloud/sdk-ts) - SDK for interacting with Sentrix EVM, native APIs, and BFT channels.
- [Rust SDK](https://github.com/SentrisCloud/sdk-rs) - Typed Rust clients for native REST, EVM (alloy), gRPC (tonic), and secp256k1 wallet/signing. `Early`
- [Sentrix gRPC-Web Client](https://github.com/SentrisCloud/sentrix-grpc-wasm) - Rust + WebAssembly gRPC-Web client packaged via wasm-pack, for browser dApps. `Early`
- [Token List](https://github.com/sentrix-labs/token-list) - Canonical Uniswap-token-list-v1 registry for Sentrix mainnet (7119) and testnet (7120).
- [Indexer](https://github.com/SentrisCloud/indexer) - Postgres-backed REST indexer for blocks, transactions, logs, tokens, and native chain data. `Phase 1 / scaffold`

## Smart Contracts

- [Canonical Contracts](https://github.com/sentrix-labs/canonical-contracts) - WSRX, Multicall3, SentrixSafe, and TokenFactory.
- [Sentrix DEX](https://github.com/sentrix-labs/sentrix-dex) - AMM and liquidity infrastructure for SRX ecosystem markets.
- [Token List](https://github.com/sentrix-labs/token-list) - Uniswap-token-list-v1 registry of recognized tokens on Sentrix Chain.
- [dApp Starter Contracts](https://github.com/SentrisCloud/dapp-starter/tree/main/contracts) - Example Solidity contracts for deployment on Sentrix.

### Deployed canonical addresses

Verified live (`eth_getCode` non-empty on the listed chain). Full source-of-truth at [`canonical-contracts/docs/ADDRESSES.md`](https://github.com/sentrix-labs/canonical-contracts/blob/main/docs/ADDRESSES.md).

| Contract | Mainnet (`7119`) | Testnet (`7120`) |
| --- | --- | --- |
| WSRX | `0x4693b113e523A196d9579333c4ab8358e2656553` | `0x85d5E7694AF31C2Edd0a7e66b7c6c92C59fF949A` |
| Multicall3 | `0xFd4b34b5763f54a580a0d9f7997A2A993ef9ceE9` | `0x7900826De548425c6BE56caEbD4760AB0155Cd54` |
| TokenFactory | `0xc753199b723649ab92c6db8A45F158921CFDEe49` | `0x7A2992af0d4979aDD076347666023d66d29276Fc` |
| SentrixSafe | `0x6272dC0C842F05542f9fF7B5443E93C0642a3b26` | `0xc9D7a61D7C2F428F6A055916488041fD00532110` |

## Infrastructure

- [SentrixScan](https://scan.sentrixchain.com) - Sentrix block explorer.
- [Obsidian Engine (Explorer V2)](https://github.com/SentrisCloud/sentrix-explorer-v2) - Rust + WebAssembly block explorer. Coexists with SentrixScan on a separate domain. `Early`
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

### Get testnet SRX from the faucet

1. Open the [Sentrix Faucet](https://faucet.sentrixchain.com).
2. Switch the network selector to **Sentrix Testnet**.
3. Paste your EVM-compatible wallet address (for example, from MetaMask).
4. Pass the Cloudflare Turnstile challenge.
5. Submit the request. The tx hash appears below the form — open it in [scan-testnet.sentrixchain.com](https://scan-testnet.sentrixchain.com) to confirm finalization.

The faucet drips a small amount per request and applies a per-address cooldown. Wait out the cooldown if you need more.

### Read Sentrix blocks with viem

```ts
import { createPublicClient, http } from 'viem';

const sentrix = {
  id: 7119,
  name: 'Sentrix Chain',
  network: 'sentrix',
  nativeCurrency: { name: 'Sentrix', symbol: 'SRX', decimals: 18 },
  rpcUrls: { default: { http: ['https://rpc.sentrixchain.com'] } },
} as const;

const client = createPublicClient({ chain: sentrix, transport: http() });

const block = await client.getBlock();
console.log(`block ${block.number} has ${block.transactions.length} txs`);

const balance = await client.getBalance({
  address: '0x0000000000000000000000000000000000000000',
});
console.log(`balance: ${balance} wei`);
```

For testnet, swap `id` to `7120` and the RPC URL to `https://testnet-rpc.sentrixchain.com`.

### More tutorials

These are tracked as open issues — pull requests welcome:

- Deploy a Solidity contract on Sentrix (covered partially by [dApp Starter](https://github.com/SentrisCloud/dapp-starter))
- Send an SRX transaction with viem / ethers.js
- Run a Sentrix fullnode
- Run a Sentrix validator (see [Running a Node](#running-a-node) and [#16](https://github.com/sentrix-labs/awesome-sentrix/issues/16))
- Verify contracts with Sourcify (covered by [Foundry config](#foundry-config))

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
