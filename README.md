# Crypto Crates
## Zero-Knowledge Web3 ETF Infrastructure on Mina Protocol

Crypto Crates is a Web3-native platform that enables users to create, publish, and track decentralized baskets of real-world stocks (ETF-like portfolios) with **verifiable performance using zero-knowledge proofs powered by Mina Protocol**.

The project allows anyone to build custom stock baskets, publish them permissionlessly, and display cryptographically verified P&L and NAV calculations—without storing sensitive or heavy financial data on-chain.

---

## ✨ Features

- 📊 **Custom Basket Creation**  
  Create ETF-style portfolios composed of real-world stocks with user-defined weights.

- 🌐 **Network-Agnostic Publishing**  
  Users can select a blockchain network and publish baskets with minimal on-chain state.

- 🔍 **Zero-Knowledge Verified Performance**  
  Portfolio NAV and P&L are computed off-chain and verified on-chain using Mina zk-SNARKs.

- 🔐 **Scalable & Trust-Minimized**  
  No raw price feeds or historical data are stored on-chain.

- 🔁 **Forkable & Social Portfolios**  
  Public baskets can be forked, modified, and compared.

- 🧩 **Composable Financial Primitive**  
  Designed to integrate with DeFi, analytics, and portfolio tools.

---

## 🧠 Why Mina Protocol?

Mina Protocol enables succinct blockchain applications through zero-knowledge proofs.  
Crypto Crates leverages Mina’s zkApps to:

- Prove correctness of off-chain portfolio calculations
- Maintain minimal on-chain state
- Reduce trust in centralized price calculators
- Enable verifiable financial transparency without data leakage

This makes Mina uniquely suited for real-world financial verification use cases.



---

## 🧩 Architecture Overview

User
└─▶ Basket Builder UI
└─▶ Off-chain Price Aggregator
└─▶ Portfolio P&L Computation
└─▶ zk-SNARK Proof Generation
└─▶ Mina zkApp Verification
└─▶ On-chain State Update

---

## 🧱 Core Components

| Component | Description |
|--------|------------|
| Frontend | Basket creation UI & analytics dashboard |
| Oracle Layer | Aggregates real-world stock prices |
| Off-chain Engine | Computes NAV & P&L |
| zk Prover | Generates proofs of correct computation |
| Mina zkApp | Verifies proofs and updates state |
| Registry Contract | Stores basket metadata |

---

## 🔍 Zero-Knowledge Verification Flow

1. User creates or updates a basket
2. Off-chain service fetches stock prices via oracles
3. Portfolio NAV & P&L are calculated
4. zk-SNARK proves:
   - Correct prices were used
   - Basket weights were applied correctly
   - Final P&L is accurate
5. Proof is submitted to a Mina zkApp
6. zkApp verifies the proof and updates minimal on-chain state

---

## 🛠 Tech Stack

- **Mina Protocol** — zkApps & proof verification
- **SnarkyJS** — Zero-knowledge circuit construction
- **Node.js / TypeScript** — Off-chain computation & prover
- **Smart Contracts** — Basket registry & metadata
- **Oracle Feeds** — Real-world stock price aggregation
- **React** — Frontend UI

---

## 📁 Repository Structure
crypto_crates/
├── frontend/ # Basket builder & dashboard
├── zk-circuits/ # zk-SNARK circuits (SnarkyJS)
├── prover/ # Off-chain proof generation
├── contracts/ # Mina zkApps
├── oracle/ # Price aggregation layer
├── scripts/ # Deployment & utilities
└── README.md

---

## 🚧 Development Status

**Status:** Active development

Current focus:
- MVP basket creation
- Oracle integration
- zk proof generation for NAV & P&L
- Mina testnet deployment

---

## 🗺 Roadmap

- [ ] Basket creation MVP
- [ ] Oracle integration
- [ ] zk proof generation (NAV & P&L)
- [ ] Mina zkApp verification
- [ ] Public basket registry
- [ ] Forking & social metrics
- [ ] Mainnet deployment

---

## 📊 Use Cases

- Decentralized ETF creation
- Transparent portfolio performance tracking
- Strategy marketplaces
- Social trading dashboards
- Composable DeFi analytics

---

## 🤝 Contributing

Contributions are welcome!

- Open an issue for bugs or feature requests
- Submit a pull request for improvements

---

## ⚠️ Disclaimer

Crypto crates is an experimental software project.  
It does **not** provide financial advice or investment products.

---

## 📜 License

MIT License
