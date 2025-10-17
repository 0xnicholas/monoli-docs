[[中文]](/README_cn.md)

> This index outlines the major research tracks and initiatives under the Monoli project.

## About Monoli

**Monoli** is a high-performance Layer 1 blockchain and its associated native DeFi ecosystem, developed under [Lico labs](). Currently in an intensive R\&D phase, Monoli aims to create an ultra-efficient blockchain infrastructure and a structured financial ecosystem. The Monoli ecosystem consists of three core pillars: [Monoli L1](https://nicholas.feishu.cn/wiki/A301w7iE5ikIgikRasScq9OxnYg?from=from_copylink), [Monoli Perp DEX](https://nicholas.feishu.cn/wiki/Ecy3wEeKyi09TXkbupncOVosn0d?from=from_copylink), and [Monoli Platform](https://nicholas.feishu.cn/wiki/IjZ6wPIAUiAuNGkXneicQKMfn2K?from=from_copylink).

## Monoli L1

Monoli is designed to push the performance limits of Layer 1 blockchains by decoupling and independently optimizing core components—such as consensus, execution, and networking—while maintaining *variable-speed coordination* between layers. This architectural approach enables Monoli to align with the long-term evolutionary trajectory of blockchain technology while achieving best-in-class infrastructure in every stage.

With a target throughput of **240,000 TPS**, Monoli aims to deliver a Web2-grade user experience for DeFi, high-frequency trading (HFT), and on-chain applications. Key innovations and enhancements include:

* **MonoBFT**, A high-frequency finality BFT protocol built on DAG structures (earlier based on a HotStuff derivative).
* **ForceSync**, Monoli’s proprietary state and block synchronization system that ensures robust node consistency.
* **Execution Framework**, A VM-agnostic execution environment supporting diverse smart contract runtimes.
* **Loom**, A hybrid VM execution network, centered around **LoomVM**, a secure and deterministic bytecode virtual machine compiled from RISC-V (replacing rWASM). It supports multi-VM equivalent execution environments.
* **MonoEVM**,
* **MonoDB**, A multi-tiered database built on top of RocksDB, optimized for performance and scalability.
* **TurboCast**, A high-efficiency networking layer using adaptive broadcast trees for rapid message propagation.
* **LiquiBoost**, A native on-chain incentive protocol designed to reward both validators and developers.
* **Realm Chain**, Monoli Realm Chain is a modular L1 blockchain architecture designed to support the rapid construction and optimization of Domain-Specific Chains. By reusing core modules and tools from Monoli L1, Realm Chain provides a high-performance, scalable, and compliance-friendly infrastructure for specific use cases.

In addition, Monoli provides a modular Rust SDK and framework named **Gizmo** for building custom blockchain systems.

## Monoli DEX

**Monoli DEX** is the native perpetual futures exchange on the Monoli L1 network. Built on a high-speed orderbook matching engine, it aims to deliver near-centralized exchange performance for high-frequency and professional traders. It supports leveraged trading for over 100 token pairs.

Designed for power users—quantitative traders, professionals, and leverage speculators—Monoli DEX maximizes efficiency, fairness, and execution speed by leveraging the full performance capabilities of Monoli L1.

The exchange supports four primary order types:

1. **Market Order** – Execute immediately at the best available price.
2. **Limit Order** – Execute at a user-specified price.
3. **Scale Order** – Place multiple limit orders across a price range.
4. **TWAP** – Time-weighted average price execution over intervals.

Beyond standard perps, Monoli DEX also offers structured perpetual products:

* **Index Perps** – Trade ecosystem indices like NFT floor price composites (e.g., *NFTI-USD*).
- **FundingRate Future**：FF enables traders to express their view on funding rates. Those bullish on funding rates can open a long position whereas bears can open a short position. FF also enables those with a floating funding rate exposure to hedge their funding rates payment / receivables.
* **Vaults**:

  * Market-making vaults (user-customized and platform-driven via **MLP**, Monoli Liquidity Provider).
  * FF Vaults (Funding Future Vault).
  * Structured derivative vaults (**MTP**, Monoli Tranche Perp Vault).
  * Credit risk protection vaults (**MCD**, Monoli Credit Default Vault).

## Monoli Platform
Monoli Platform is the ecosystem development platform for the Monoli public chain. Independently, it also serves as an open integration platform spanning the web systems and stands as the crypto world's first iPaaS product, enabling developers to efficiently build Web3 applications and related cross-system products.

First and foremost, this platform provides reliable infrastructure for developers to construct Web3 applications. It offers comprehensive general-purpose and domain-specific API services, abstracting away blockchain complexity so developers can efficiently build Web3-related applications using an API-led approach.

Simultaneously, it functions as an enterprise-grade hybrid integration platform. Through its API integration capabilities and blockchain engine, businesses can leverage a unified API gateway to connect with traditional information management systems (SaaS/ERP/Fintech...) while seamlessly integrating with Monoli's blockchain network. This achieves cross-system, cross-chain, low-latency integration of data and business flows.

## Resources

**Website**: [https://monoli.xyz](https://monoli.xyz)

### L1

* [Monoli L1 (v0.8.4)](https://nicholas.feishu.cn/wiki/A301w7iE5ikIgikRasScq9OxnYg) (main doc)
* [Monoli L1 (v0.7.2)](https://nicholas.feishu.cn/wiki/RMAlwhsbZi1lYTkGheNcip7gnnc?from=from_copylink)
* [Monoli L1 (early version)]()
* [Monoli L1 Tech Book](https://nicholas.feishu.cn/wiki/OPJuwcVayi27k5klYeYcR2ixnSb)
* [Monoli Wiki](https://nicholas.feishu.cn/wiki/JpM6waMvIijcohkSuUncbVHNnUe?from=from_copylink)

### DEX

* [Monoli Perp DEX \[v1.2.2\]](https://nicholas.feishu.cn/wiki/Ecy3wEeKyi09TXkbupncOVosn0d) (main doc)
* [DEX Product Prototype](https://nicholas.feishu.cn/wiki/Rqknwd9yHiMa8ykWIkOcoHGGned)
* [Perpetual DEX Tech Book (prime edition)](https://nicholas.feishu.cn/wiki/CvqYwM7eliHImLkSGmPcSPByn6d): Monoli DEX prime edition technical docs. this edition is mainly used to test,review architectual and technical options.
* [DEX Risk Management and Case Studies](https://nicholas.feishu.cn/wiki/Z4WawXpb5iqz7QkCazrcWFqxnXe)

### Platform

* [Monoli Platform](https://nicholas.feishu.cn/wiki/IjZ6wPIAUiAuNGkXneicQKMfn2K?from=from_copylink) (main doc)

### Ecosystem
* [**Monogram**](https://nicholas.feishu.cn/wiki/IQlGwoq4QiyGGFk5Y0rcU51Ingg): A synthetic dollar protocol on Monoli, providing a crypto-native stablecoin backed by delta-neutral derivative strategies. $M combines peg stability with intrinsic yield, making it a robust foundation for on-chain financial applications.

* [**Plaid**](https://nicholas.feishu.cn/wiki/IrgFwa9ijikrI7k1sx3c1yjsnxa?from=from_copylink): Plaid is Monoli’s native on-chain CLOB protocol that powers unified, high-efficiency liquidity for DeFi applications, offering precision trading and forming a share liquidity layer for Monoli’s on-chain financial ecosystem.

* [**Sunwell**](https://nicholas.feishu.cn/wiki/UOA6w3orwihjEIkHU6scxfWTnUe?from=from_copylink): Sunwell represents a critical step in transforming structured financial products into on-chain financial primitives, enabling asset tokenization, native yield generation, and structured wrapping for advanced DeFi applications in capital formation, risk pricing, and yield engineering.

* **Dakai**: The intent-centric protocols, introducing a declarative transaction model that shifts execution complexity away from users to solver networks.

* [Monoli **Bridge**](https://nicholas.feishu.cn/wiki/EqCcw81P1ix9qikLC1QcU6A4nhe?from=from_copylink): Monoli Bridge is a native cross-chain gateway that enables fast, low-cost, and secure asset transfers between Monoli and Ethereum(and more), supporting seamless interoperability through a decentralized architecture.

* **Octa**: A decentralized MPC signer network designed to solve blockchain interoperability challenges through a Zero Trust cryptographic model and a high-performance, decentralized architecture.

* **Bagel Wallet**: An intent-enabled programmable wallet that allows users to express desired outcomes while abstracting away transaction complexity.

### Papers

#### *Consensus*
* [[Issue] Uncertified DAGs for Scalable BFT Consensus: Optimizing Latency and Throughput in Next-Generation Blockchain Architectures](https://nicholas.feishu.cn/wiki/Xx7gwdJ7SiH03XktyJucrkmrnyS?from=from_copylink) MonoBFT V0.9, Certificateless design

* [[Issue] Scalable Mempool Design for DAG-Based Blockchain Consensus: Optimizing Transaction Propagation and Storage for Low-Latency and High-Throughput](https://nicholas.feishu.cn/wiki/UIEAwFWRhi7mXFkUxjbcTgIAndh?from=from_copylink): (MonoGraph) A better Mempool, that reliably distributes transactions, is the key enabler of a high-performance ledger. It should be separated from the consensus protocol altogether, leaving consensus only the job of ordering small fixed-size references. This leads to an overall system throughput being largely unaffected by consensus throughput.

* [[Issue] Consensus-less Transaction Confirmation: Optimizing Low-Latency, High-Throughput Blockchain Systems with BFT Broadcast and Explicit Dependency Models](https://nicholas.feishu.cn/wiki/Ss1NwgVQTiaX92kEsrwcpwtXnrb?from=from_copylink): An exploration of how consensus-less transaction confirmation, enabled by reliable broadcast(TurboCast) and explicit dependency models, optimizes latency and throughput.

* [\[Issue\] A DAG-Structured BFT Protocol for High-Frequency Finality](https://nicholas.feishu.cn/wiki/Bpc0wOMBEiZhkpko1gucyHlsnCc): Adopts DAG-based consensus for high-frequency environments; comparison with HotStuff.

* [[Issue] DAG-Based Transaction Ordering Without Consensus: Designing a Verifiable Sequencer via TVA](https://nicholas.feishu.cn/wiki/AXvWw3pnBix6bIkUUCOc1rQpnnc?from=from_copylink): This issue explores integrating TVA into DAG-based blockchains to achieve deterministic, verifiable transaction ordering without relying on consensus-layer sequencing, enabling auditable, fair, and high-throughput parallel execution.

* [\[Issue\] High Performance, Fast Finality, Fork-Resistant BFT](https://nicholas.feishu.cn/wiki/QHzww7kL4iTMwxkiqNLcadAQnLf): Early research on MonoBFT(v0.7) based on HotStuff series.

* [[Issue] n slot, ms finality, or near-instant finality](https://nicholas.feishu.cn/wiki/UbVpw5ccLilDt0k2g4xcFR2LnPh):

#### *Execution*

* [[Paper] LoomVM: A Secure and Deterministic Bytecode Virtual Machine Powered by RISC-V Frontend Compilation](https://nicholas.feishu.cn/wiki/KFw9wBl7ViOaTdke0YTcEqPtnsh?from=from_copylink): This paper presents LoomVM, a secure and deterministic bytecode virtual machine designed for on-chain execution, translating RISC-V binaries into verifiable, gas-aware bytecode to enable high-performance, analyzable, and zk-friendly smart contract execution in the Monoli blockchain.

* [[Paper] MonoEVM+ : Optimizing the EVM through Consensus and Client Innovation (reth)](https://nicholas.feishu.cn/wiki/UZkmwTCQEiraRkkzHmjcarpdnwf?from=from_copylink): Monoli L1 supports EVM, and MonoEVM uses reth/revm as the execution engine base.

* [[Agenda] Planning the Monoli Blockchain Smart Contract Language](https://nicholas.feishu.cn/wiki/AcMuwXbfZiBHaqkbox0comGnnZc?from=from_copylink): Define the requirements, architecture, and roadmap for Monoli’s Rust-based smart contract language and a VM supporting both Rust and Solidity smart contracts.

* [[Issue] Abstract Execution in Blockchain: A Study on VM-Agnostic Architecture Design](https://nicholas.feishu.cn/wiki/O3ebwHIPJiH5DykdHSsccL6xn6d?from=from_copylink): A study on abstract execution architecture that hides blockchain complexity through a VM-agnostic, modular execution layer—enabling open, composable execution across diverse blockchain systems.

* [[Issue] Shared Execution as a Public Good:  Scalable, Permissionless, and Shared Execution for Multi-VM Systems](https://nicholas.feishu.cn/wiki/HaBCwYiiGiodqrk0bWCcEENWn1g?from=from_copylink): An exploration of how Loom enables shared execution as a public good—supporting scalable, permissionless execution across heterogeneous VMs in an open execution network.

* [\[Issue\] Multi-VM Equivalence and Intermediate Representation](https://nicholas.feishu.cn/wiki/DUmIw1IQuitqE1ki5A2cj3XLnqf): A comprehensive overview of Loom, Monoli’s unified execution environment, focusing on multi-VM equivalent execution and the role of an intermediate representation in enabling cross-VM compatibility.

* [\[Issue\] Parallelism Meets Finality: A Hybrid DAG-Blockchain Execution Model](https://nicholas.feishu.cn/wiki/IJVnwmHITiEgrvkREvFcHBs4n9e): Merging DAG concurrency with blockchain finality guarantees.

* [\[Issue\] Intra-chain Parallelism](https://nicholas.feishu.cn/wiki/QfuqwL318ipbyYkKmArc67Btn1g): Native scaling through intra-chain parallelism.

#### *DB, DA*
* [[Issue] Designing a DAG-Compatible, Multi-VM Scalable Storage Layer for Monoli](): A design exploration of Monoli’s scalable, DAG-compatible storage layer to support multi-VM execution.

#### *Architecture*
* [Gizmo](https://nicholas.feishu.cn/wiki/PN5iw3MN7iLKWVkeLpmclVaUn9g): Gizmo is a Rust framework for building blockchains in a modular and scalable way. It is a set of libraries and primitives for building Monoli chains.

* [[Issue] Rebuilding vs Refining: Architectural Paradigms for High-Performance Blockchains]() Exploration of the next generation blockchain architecture, comparison of engineering optimization and innovation architectures.

* [[Issue] Shared Security Models for Realm Chains in the Monoli Ecosystem](https://nicholas.feishu.cn/wiki/PIAEwG3ZYiQoPPkaGhKcB8lKn4g?from=from_copylink):

* [[Paper] Realm Chain: Modular L1 Architecture for Domain-Specific Blockchain](https://nicholas.feishu.cn/wiki/JgXCwVHenimPwdkJlPbcjhuSnHd?from=from_copylink): Monoli Realm Chain is a modular L1 blockchain architecture designed to support the rapid construction and optimization of Domain-Specific Chains. By reusing core modules and tools from Monoli L1, Realm Chain provides a high-performance, scalable, and compliance-friendly infrastructure for specific use cases(eg. stablecoin payments).

* [[Issue] Monoli Native Bridge: Seamless Interoperability for Realm Chains and Ethereum](https://nicholas.feishu.cn/wiki/EqCcw81P1ix9qikLC1QcU6A4nhe?from=from_copylink): Monoli native bridging solution, which enables users to securely and efficiently transfer messages and assets between Monoli realm chain and other major public chains.

* [\[Issue\] What's the Ideal Block Size](https://nicholas.feishu.cn/wiki/FEnIwzQyviOls1k8pngc5W2EnAU) Finding the Optimal Block Size and Scalability Trade-offs in High-Performance Blockchains.

* [\[Issue\] Native Accounts for On-Chain Finance](https://nicholas.feishu.cn/wiki/Mlj6wfTEviPKcckdktVcP62cnhT) Account Model Designs in Representative Blockchains and Monoli's Design Exploration.

#### *DEX, DeFi*

* [\[Issue\] DPS Benchmarking Methods](https://nicholas.feishu.cn/wiki/YRKUwMpigi2LYvkeV3xcv27Xnyd): Measuring throughput and latency using AMM-style benchmarks.
* [\[Issue\] Controls Over Perpetual Contract Trading](https://nicholas.feishu.cn/wiki/C4GOwP5aEiX6BskixNHcx1sMn2b): Design of index price, mark price, and funding rate mechanisms.
* [\[Issue\] Why Fully Transparent Trading Markets Are Beneficial](https://nicholas.feishu.cn/wiki/MS7aw1pHxiGbH4kcuLPcsvzenxg) Benefits and Merits of Transparent Trading Markets.
* [\[Issue\] Feasibility of On-Chain Dark Pools](https://nicholas.feishu.cn/wiki/AqZpw7tPNiS8Ofk1zincP4oZnEd) Design and Implications of On-Chain Dark Pool Mechanisms.
* [\[Paper\] Structured Finance of TradFi Inspires DeFi (Monoli Structured Derivatives Protocol)](https://nicholas.feishu.cn/wiki/DDwywlelQiqRfXko4F8cniY6nr9): Applying structured finance instruments (MTP & MCD) in DeFi.

* [[Paper] $M Stablecoin, a synthetic dollar based crypto-native solution for money](https://nicholas.feishu.cn/wiki/IQlGwoq4QiyGGFk5Y0rcU51Ingg?from=from_copylink)

* [[Issue] Asset Tokenization Meets DeFi: Enabling On-Chain Structured Products with Native Yield Logic](https://nicholas.feishu.cn/wiki/UOA6w3orwihjEIkHU6scxfWTnUe?from=from_copylink): A study of how asset tokenization and native yield logic power on-chain structured products, bridging DeFi innovation with traditional financial engineering.

* [[Issue] Structured Finance of TradFi Inspires DeFi Protocol (Monoli Structured Derivatives Protocol)](https://nicholas.feishu.cn/wiki/DDwywlelQiqRfXko4F8cniY6nr9?from=from_copylink): Exploring how structured finance principles from TradFi can inspire multi-layered derivative protocols in DeFi, enabling more sophisticated, composable financial products on Monoli.

* [[Issue] Advancing Global Payments: Designing a Stablecoin-Optimized Layer 1 Blockchain for Seamless TradFi-DeFi Integration](https://nicholas.feishu.cn/wiki/GAw6wbgCSi4sElkdETMcZDrdnjc?from=from_copylink): Exploring a “high-performance, payment-focused blockchain” that utilizes the Monoli Realm Chain architecture. Positioned as a high-performance, stablecoin-payment-oriented L1 public chain. Capable of bridging the TradFi and crypto worlds, emphasizing privacy and compliance. The economic model avoids traditional token economics, with fees paid in stablecoins.

* [[Paper] Plaid: Optimizing Decentralized Central Limit Orderbooks: Incentive Mechanisms and Matching Engine Efficiency](https://nicholas.feishu.cn/wiki/IrgFwa9ijikrI7k1sx3c1yjsnxa?from=from_copylink): Plaid provides a performant, low-latency on-chain CLOB protocol powered by Monoli's smart accounts and parallel execution, serving as a low-cost public good to enhance ecosystem liquidity and DeFi user experience.

#### *OTHER*

* [Monoli Financial Forecast](https://nicholas.feishu.cn/wiki/GtTGwvHO0ii0zYkdpWqcsO5dn3h) Financial Projections for Monoli's Business Operations.
* [Monoli Litepaper](https://nicholas.feishu.cn/wiki/In06wTQ4zi7zM1kQTFcc8cklnVb)
* [Monoli Enhancement Proposals (MEPs)](https://nicholas.feishu.cn/wiki/V87Zwm8EWiWPSXkA7lHcaOQengf)
* [\[Paper\] From Multi-chain Integration to Unified Operations](https://nicholas.feishu.cn/wiki/ZWr0wJwxuib9r6kXGjEcDZTuncc): Early explorations of omnichain infrastructure.
* [\[Paper\] The MA End Game – Massive Adoption Capability](https://nicholas.feishu.cn/wiki/M9Cuw8PWVin7lhkx2MZcLkk4nAg): Vision for enabling mass adoption in Web3, a guiding principle for Monoli.