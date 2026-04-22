# EtherEver (ETE)

> *"이더리움의 역사 위에 교육의 가치를 더하다"*  
> *"Adding educational value on top of Ethereum's history."*

EtherEver (ETE) is an Ethereum hard fork designed for **smart contract education and hands-on learning**.  
The chain preserves the full Ethereum block history from genesis to block **#1,919,999** — the same fork point as Ethereum Classic — and runs independently from block **#1,920,000** onwards.

[![Discord](https://img.shields.io/badge/Discord-Join-5865F2?logo=discord)](https://discord.com/invite/dfSF58pzZB)
[![Block Explorer](https://img.shields.io/badge/Explorer-etherever.ever--chain.xyz-blue)](https://etherever.ever-chain.xyz)
[![YouTube](https://img.shields.io/badge/YouTube-@지만쫌-red?logo=youtube)](http://www.youtube.com/@지만쫌)

---

## What is EtherEver?

EtherEver is a live Ethereum-equivalent PoW chain built as a fully accessible environment for learning smart contract deployment, DApp development, and blockchain fundamentals — using real mainnet-equivalent tooling.

| Property | Value |
|---|---|
| Ticker | **ETE** |
| Chain ID | **58051** (`0xe2c3`) |
| Fork Source | Core-Geth (go-ethereum variant) |
| Fork Block | #1,919,999 (same as Ethereum Classic) |
| Independent Chain Start | #1,920,000 |
| Consensus | **PoW** (Proof of Work, ~13s block time) |
| Active Hardforks | Homestead → London (Shanghai and Cancun excluded) |
| EVM Compatibility | Full — compatible with Hardhat, Foundry, Remix, MetaMask |

> Blocks #0 through #1,919,999 share identical block hashes with Ethereum mainnet.  
> EtherEver preserves the early Ethereum history as part of its chain.

---

## Features

### Block Explorer
- **EtherEver Explorer** — [etherever.ever-chain.xyz](https://etherever.ever-chain.xyz)  
  BlockScout-based. Displays per-block mining rewards for all historical blocks.  
  *(Core-Geth modified with Nethermind-compatible mode to enable transparent reward data.)*

### Mobile Wallet
- Custom **EtherEver MetaMask** app — Android APK available  
- EtherEver network pre-configured — no manual RPC setup required  
- Full GUI wallet management without command-line

### Developer Environment
- 100% compatible with standard Ethereum dev tools: **Hardhat**, **Foundry**, **Remix IDE**
- Add EtherEver to MetaMask manually using Chain ID `58051` and RPC `https://ever-chain.xyz`

### Community
- Discord: [discord.com/invite/dfSF58pzZB](https://discord.com/invite/dfSF58pzZB)
- YouTube: [@지만쫌](http://www.youtube.com/@지만쫌)

---

## Running a Node

### 1. Install Go 1.21

```bash
wget https://dl.google.com/go/go1.21.0.linux-amd64.tar.gz
sudo rm -rf /usr/local/go
sudo tar -C /usr/local -xzf go1.21.0.linux-amd64.tar.gz
echo 'export PATH=$PATH:/usr/local/go/bin' >> ~/.bashrc
source ~/.bashrc
go version
```

### 2. Build

```bash
make geth
```

### 3. Run

```bash
# Start node with interactive console
./build/bin/geth console
```

Default data directory: `~/.ethereum`

### 4. Useful console commands

```javascript
admin.nodeInfo.enode   // show this node's enode URL
net.peerCount          // number of connected peers
admin.peers            // list connected peers
miner.start()          // start mining
eth.blockNumber        // current block height
```

---

## Adding EtherEver to MetaMask

| Field | Value |
|---|---|
| Network Name | EtherEver |
| RPC URL | `https://ever-chain.xyz` |
| Chain ID | `58051` |
| Currency Symbol | `ETE` |
| Block Explorer | `https://etherever.ever-chain.xyz` |

---

## Vision

- **Education-first**: Deploy real smart contracts on a live PoW chain without mainnet risk
- **Historical continuity**: Ethereum's early history (#0–#1,919,999) preserved in the chain
- **Accessible**: Pre-configured MetaMask app removes setup friction for new users
- **Long-term**: Community-driven growth with a planned automated exchange program

---

## Links

| Resource | URL |
|---|---|
| Block Explorer | https://etherever.ever-chain.xyz |
| Discord | https://discord.com/invite/dfSF58pzZB |
| YouTube | http://www.youtube.com/@지만쫌 |
| GitHub | https://github.com/makewalletfirst |

---

## License

LGPL-3.0 / GPL-3.0 — See [COPYING](./COPYING) and [COPYING.LESSER](./COPYING.LESSER) for details.  
Based on [Core-Geth](https://github.com/etclabscore/core-geth) / [go-ethereum](https://github.com/ethereum/go-ethereum).
