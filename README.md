# Crypto-Crates
Crypto Crates is a Web3-native platform that enables users to create, publish, and track decentralized baskets of real-world stocks (ETF-like portfolios) across blockchain networks, with verifiable performance powered by zero-knowledge proofs on Mina Protocol.

Zero-Knowledge Web3 ETF Infrastructure on Mina Protocol
Crypto-Crates is a Web3-native platform that enables users to create, publish, and track decentralized baskets of real-world stocks (ETF-like portfolios) with verifiable performance using zero-knowledge proofs powered by Mina Protocol.
The project allows anyone to create custom stock baskets, publish them permissionlessly, and display cryptographically verified P&L and NAV calculations—without storing sensitive or heavy financial data on-chain.

✨ Key Features

📊 Custom Basket Creation
Create ETF-style portfolios composed of real-world stocks with user-defined weights.

🌐 Network-Agnostic Publishing
Users can select a blockchain network and publish baskets with minimal on-chain state.

🔍 Zero-Knowledge Verified Performance
P&L and NAV are computed off-chain and verified on-chain using Mina’s zk-SNARKs.

🔐 Minimal Trust & Scalable Design
No raw price feeds or historical data are stored on-chain.

🔁 Forkable & Social Portfolios
Public baskets can be forked, modified, and compared.

🧩 Composable Financial Primitive
Designed to be integrated into other DeFi, analytics, or portfolio tools.

🧠 Why Mina Protocol?

Mina Protocol enables succinct blockchain applications using zero-knowledge proofs. ZETF leverages Mina’s zkApps to:

Prove correctness of off-chain portfolio calculations
Maintain minimal on-chain state
Reduce trust in centralized price calculators
Enable verifiable financial transparency without data leakage
This makes Mina uniquely suited for real-world financial verification use cases.

🧩 Architecture Overview
User → Basket Builder UI
      → Off-chain Price Aggregator
      → Portfolio P&L Computation
      → zk-SNARK Proof Generation
      → Mina zkApp Verification
      → On-chain State Update

Components
Component	Description
Frontend	Basket creation UI & performance dashboard
Off-chain Engine	Price aggregation & P&L calculation
zk Prover	Generates proof of correct computation
Mina zkApp	Verifies proofs and updates state
Registry Contract	Stores basket metadata
🔍 Zero-Knowledge Flow

User creates or updates a basket

Off-chain service fetches stock prices via oracles

Portfolio NAV & P&L are computed

A zk-SNARK proves:

Correct prices were used

Weights were applied correctly

Final P&L is accurate

Proof is submitted to Mina zkApp

zkApp verifies proof and updates on-chain state

🛠 Tech Stack

Mina Protocol — zkApps & proof verification
TypeScript / Node.js — Off-chain computation & prover
SnarkyJS — Zero-knowledge circuit construction
Smart Contracts — Basket registry & metadata
Oracles — Real-world stock price feeds
React — Frontend UI

📦 Repository Structure
crypto_crates/
├── frontend/          # Basket builder & dashboard
├── zk-circuits/       # zk-SNARK circuits (SnarkyJS)
├── prover/             # Off-chain proof generation
├── contracts/          # Mina zkApps
├── oracle/             # Price aggregation layer
├── scripts/            # Deployment & utilities
└── README.md

🚧 Development Status

🚧 Active Development

Current focus:

MVP basket creation

zk proof generation for NAV & P&L

Mina testnet deployment

🗺 Roadmap

 Basket creation MVP
 Oracle integration
 zk proof generation (NAV & P&L)
 Mina zkApp verification
 Public basket registry
 Forking & social metrics
 Mainnet deployment

📊 Use Cases
Decentralized ETF creation
Transparent portfolio performance tracking
Strategy marketplaces
Social trading dashboards
Composable DeFi analytics

🤝 Contributing

Contributions are welcome!
Feel free to open issues or submit pull requests.

📜 Disclaimer

ZETF is a technical and experimental project.
It does not provide financial advice or investment products.

📄 License

MIT License
