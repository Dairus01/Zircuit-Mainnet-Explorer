# Zircuit Mainnet Explorer

A live **Blockscout-powered blockchain explorer** for the **Zircuit Mainnet**, providing real-time visibility into blocks, transactions, token transfers, account balances, and on-chain analytics.

🔗 **Live Demo:** [https://zircuit.cloud.blockscout.com/](https://zircuit.cloud.blockscout.com/)

---

## Overview

The **Zircuit Mainnet Explorer** is a custom Blockscout instance deployed using **Blockscout Autoscout Cloud**.  
It indexes Zircuit’s EVM-compatible network and exposes a full-featured explorer UI and developer APIs for transactions, tokens, contracts, and analytics.

The explorer is designed to make Zircuit transparent, auditable, and developer-friendly by giving anyone direct insight into on-chain data.

---

## Key Features

- **Real-time data indexing** for blocks, transactions, and logs  
- **Full block explorer UI** with block, transaction, and token pages  
- **Account and holder analytics** with top balances and token distributions  
- **Token registry** for ERC-20 and ERC-721 assets on Zircuit  
- **Contract verification support** for developers and auditors  
- **Charts and stats** showing network utilization, fees, and growth trends  
- **API Documentation** including REST, RPC, and GraphQL endpoints  
- **WalletConnect integration** for MetaMask and compatible wallets  
- **Custom branding and theming** for a Zircuit-native explorer feel  

---

## Architecture

This project is powered by **Blockscout Autoscout**, a managed deployment layer that automates explorer hosting and indexing.
With Blockscout you can index your blockchain in minutes.

**Core components:**

| Layer | Technology | Role |
|-------|-------------|------|
| **Autoscout Cloud** | Blockscout Cloud | Manages instance deployment and scaling |
| **Backend** | Elixir (Phoenix Framework) | Handles data ingestion and API endpoints |
| **Database** | PostgreSQL | Stores indexed blocks, txs, tokens, and contracts |
| **Frontend** | React + TypeScript | Renders the explorer UI and analytics |
| **Blockchain Data Source** | Zircuit RPC | Provides live blockchain data |
| **Plugins** | Charts & Stats | Adds visualization for metrics and network activity |

---

## How It Works

1. **Deployment**:  
   Using [Autoscout](https://docs.blockscout.com/using-blockscout/autoscout), we created a new instance and filled in:
   - Chain Name: `Zircuit Mainnet`  
   - Chain ID: `48900`  
   - RPC URL: `https://mainnet.zircuit.com/`  
   - WS URL: `wss://mainnet.zircuit.com/`  
   - Node Type: `Geth`  
   - Gas Token Symbol: `ETH`

2. **Indexing**:  
   The Blockscout indexer connects to the Zircuit RPC node and continuously fetches new blocks and transactions. Data is parsed and stored in PostgreSQL.

3. **API Layer**:  
   Once indexed, data becomes accessible through:
   - `/api` → REST endpoints  
   - `/graphiql` → GraphQL playground  
   - `/eth-rpc` → Native RPC interface

4. **Frontend UI**:  
   The web UI dynamically updates as the indexer processes new blocks, showing live transaction feeds, token transfers, and stats.

5. **Monitoring**:  
   The Autoscout dashboard provides access to real-time logs, indexer performance, and resource metrics.

---

## Technologies Used

- **Blockscout Autoscout Cloud**
- **Elixir + Phoenix Framework**
- **PostgreSQL**
- **React + TypeScript**
- **Zircuit RPC Node**
- **Charts & Stats Plugin**
- **WalletConnect Integration**

---

## Partner Technology Benefits

**Blockscout Autoscout** removed the complexity of manual deployment.  
Instead of running multiple Docker containers and syncing a database manually, Autoscout handled:

- Instance provisioning  
- Data indexing setup  
- Cloud hosting and SSL configuration  
- Real-time monitoring and scaling  

This allowed us to focus on customization, branding, and analytics rather than infrastructure.

---

## What Makes It Unique

- First public **Zircuit Mainnet Explorer** deployed on **Blockscout Cloud**  
- Fully functional **real-time indexer** connected to a live Layer 2  
- **Developer-ready APIs** for anyone to integrate analytics or dashboards  
- **Custom branding** reflecting Zircuit’s identity  
- **Optimized stability** with batch and retry logic tuning  

---

## 🗺️ Future Plans

- Enable **contract verification** workflow for developers  
- Integrate **token risk analytics** and whale tracking  
- Add **security and anomaly detection** dashboards  
- Build a **Zircuit API SDK** for developers  
- Extend multi-chain explorer support for Zircuit Testnet  

---

## 🧑‍💻 Team & Credits

**Built by:** Dairus ([@okohdairus](mailto:okohdairus@gmail.com))  
**Deployed via:** [Blockscout Autoscout Cloud](https://docs.blockscout.com/using-blockscout/autoscout)  
**Blockchain:** [Zircuit Mainnet](https://www.zircuit.com)

---

## 🧱 Repository Structure (if applicable)

