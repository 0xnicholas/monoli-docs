[[中文]](/README_cn.md)

> This index outlines the major research tracks and initiatives under the Monoli project.

## About Monoli

**Monoli** is a high-performance Layer 1 blockchain and its associated native DeFi ecosystem, developed under [Lico labs](). Currently in an intensive R\&D phase, Monoli aims to create an ultra-efficient blockchain infrastructure and a structured financial ecosystem. The Monoli ecosystem consists of three core pillars: [Monoli L1](), [Monoli Perp DEX](), and [Monoli Vaults]().

## Monoli L1

Monoli is designed to push the performance limits of Layer 1 blockchains by decoupling and independently optimizing core components—such as consensus, execution, and networking—while maintaining *variable-speed coordination* between layers. This architectural approach enables Monoli to align with the long-term evolutionary trajectory of blockchain technology while achieving best-in-class infrastructure in every stage.

With a target throughput of **120,000 TPS**, Monoli aims to deliver a Web2-grade user experience for DeFi, high-frequency trading (HFT), and on-chain applications. Key innovations and enhancements include:

* **MonoBFT**, A high-frequency finality BFT protocol built on DAG structures (earlier based on a HotStuff derivative).
* **TVA**, A time-verifiable asynchronous execution model that deterministically pre-orders transactions while enabling asynchronous execution.
* **ForceSync**, Monoli’s proprietary state and block synchronization system that ensures robust node consistency.
* **Execution Framework**, A VM-agnostic execution environment supporting diverse smart contract runtimes.
* **Loom**, A hybrid VM execution network, centered around **LoomVM**, a secure and deterministic bytecode virtual machine compiled from RISC-V (replacing rWASM). It supports multi-VM equivalent execution environments.
* **MonoDB**, A multi-tiered database built on top of RocksDB, optimized for performance and scalability.
* **TurboCast**, A high-efficiency networking layer using adaptive broadcast trees for rapid message propagation.
* **LiquiBoost**, A native on-chain incentive protocol designed to reward both validators and developers.

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

## Resources

**Website**: [https://monoli.xyz](https://monoli.xyz)

### L1

* [Monoli L1 \[draft v0.8.3\]](https://nicholas.feishu.cn/wiki/A301w7iE5ikIgikRasScq9OxnYg) (main doc)
* [Monoli L1 \[draft v0.7.2\]](https://nicholas.feishu.cn/wiki/RMAlwhsbZi1lYTkGheNcip7gnnc)
* [Monoli L1 Tech Book](https://nicholas.feishu.cn/wiki/OPJuwcVayi27k5klYeYcR2ixnSb)
* [Developer Docs](https://nicholas.feishu.cn/wiki/JpM6waMvIijcohkSuUncbVHNnUe)

### DEX

* [Monoli Perp DEX \[v1.2\]](https://nicholas.feishu.cn/wiki/Ecy3wEeKyi09TXkbupncOVosn0d) (main doc)
* [DEX Product Prototype](https://nicholas.feishu.cn/wiki/Rqknwd9yHiMa8ykWIkOcoHGGned)
* [DEX Risk Management and Case Studies](https://nicholas.feishu.cn/wiki/Z4WawXpb5iqz7QkCazrcWFqxnXe)
* [DEX Technical Documentation](https://nicholas.feishu.cn/wiki/CvqYwM7eliHImLkSGmPcSPByn6d)

### Ecosystem
* [**Monogram**](https://nicholas.feishu.cn/wiki/IQlGwoq4QiyGGFk5Y0rcU51Ingg): A synthetic dollar protocol on Monoli, providing a crypto-native stablecoin backed by delta-neutral derivative strategies. $M combines peg stability with intrinsic yield, making it a robust foundation for on-chain financial applications.

* [**Plaid**](https://nicholas.feishu.cn/wiki/IrgFwa9ijikrI7k1sx3c1yjsnxa?from=from_copylink): Plaid is Monoli’s native on-chain CLOB protocol that powers unified, high-efficiency liquidity for DeFi applications, offering precision trading and forming a share liquidity layer for Monoli’s on-chain financial ecosystem.

* [**Sunwell**](https://nicholas.feishu.cn/wiki/UOA6w3orwihjEIkHU6scxfWTnUe?from=from_copylink): Sunwell represents a critical step in transforming structured financial products into on-chain financial primitives, enabling asset tokenization, native yield generation, and structured wrapping for advanced DeFi applications in capital formation, risk pricing, and yield engineering.

* **Dakai**: The intent-centric protocols, introducing a declarative transaction model that shifts execution complexity away from users to solver networks.

* Monoli **Bridge**: Monoli Bridge is a native cross-chain gateway that enables fast, low-cost, and secure asset transfers between Monoli and Ethereum(and more), supporting seamless interoperability through a decentralized architecture.

* **Octa**: A decentralized MPC signer network designed to solve blockchain interoperability challenges through a Zero Trust cryptographic model and a high-performance, decentralized architecture.

* **Bagel Wallet**: An intent-enabled programmable wallet that allows users to express desired outcomes while abstracting away transaction complexity.

### Papers

#### *Consensus*
* [[Issue] Rethinking Consensus for Ordering-First Blockchains: Commit-Only Snapshots from Deterministic DAG ](https://nicholas.feishu.cn/wiki/UIEAwFWRhi7mXFkUxjbcTgIAndh?from=from_copylink): ”Ordering-First“, A novel consensus paradigm where deterministic DAG-based execution defines transaction order, and the consensus layer commits only to snapshot hashes, decoupling ordering from agreement.

* [[Issue] Consensus-less Transaction Confirmation: Optimizing Low-Latency, High-Throughput Blockchain Systems with BFT Broadcast and Explicit Dependency Models](https://nicholas.feishu.cn/wiki/Ss1NwgVQTiaX92kEsrwcpwtXnrb?from=from_copylink): An exploration of how consensus-free transaction confirmation, enabled by BFT broadcast and explicit dependency models, optimizes latency and throughput.

* [\[Issue\] A DAG-Structured BFT Protocol for High-Frequency Finality](https://nicholas.feishu.cn/wiki/Bpc0wOMBEiZhkpko1gucyHlsnCc): Adopts DAG-based consensus for high-frequency environments; comparison with HotStuff.

* [\[Issue\] High Performance, Fast Finality, Fork-Resistant BFT](https://nicholas.feishu.cn/wiki/QHzww7kL4iTMwxkiqNLcadAQnLf): Early research on MonoBFT based on HotStuff series.

* [\[Issue\] 1 Slot, 1s Finality](https://nicholas.feishu.cn/wiki/UbVpw5ccLilDt0k2g4xcFR2LnPh): Achieving 1-slot, 1-second finality.

#### *Execution*
* [[Issue] DAG-Based Transaction Ordering Without Consensus: Designing a Verifiable Sequencer via TVA](https://nicholas.feishu.cn/wiki/AXvWw3pnBix6bIkUUCOc1rQpnnc?from=from_copylink): This issue explores integrating TVA into DAG-based blockchains to achieve deterministic, verifiable transaction ordering without relying on consensus-layer sequencing, enabling auditable, fair, and high-throughput parallel execution.

* [\[Issue\] Parallelism Meets Finality: A Hybrid DAG-Blockchain Execution Model](https://nicholas.feishu.cn/wiki/IJVnwmHITiEgrvkREvFcHBs4n9e): Merging DAG concurrency with blockchain finality guarantees.

* [[Paper] LoomVM: A Secure and Deterministic Bytecode Virtual Machine Powered by RISC-V Frontend Compilation](https://nicholas.feishu.cn/wiki/KFw9wBl7ViOaTdke0YTcEqPtnsh?from=from_copylink): This paper presents LoomVM, a secure and deterministic bytecode virtual machine designed for on-chain execution, translating RISC-V binaries into verifiable, gas-aware bytecode to enable high-performance, analyzable, and zk-friendly smart contract execution in the Monoli blockchain.

* [[Agenda] Planning the Monoli Blockchain Smart Contract Language](https://nicholas.feishu.cn/wiki/AcMuwXbfZiBHaqkbox0comGnnZc?from=from_copylink): Define the requirements, architecture, and roadmap for Monoli’s Rust-based smart contract language and a VM supporting both Rust and Solidity smart contracts.

* [[Issue] Abstract Execution in Blockchain: A Study on VM-Agnostic Architecture Design](https://nicholas.feishu.cn/wiki/O3ebwHIPJiH5DykdHSsccL6xn6d?from=from_copylink): A study on abstract execution architecture that hides blockchain complexity through a VM-agnostic, modular execution layer—enabling open, composable execution across diverse blockchain systems.

* [[Issue] Shared Execution as a Public Good:  Scalable, Permissionless, and Shared Execution for Multi-VM Systems](https://nicholas.feishu.cn/wiki/HaBCwYiiGiodqrk0bWCcEENWn1g?from=from_copylink): An exploration of how Loom enables shared execution as a public good—supporting scalable, permissionless execution across heterogeneous VMs in an open execution network.

* [\[Issue\] Multi-VM Equivalence and Intermediate Representation](https://nicholas.feishu.cn/wiki/DUmIw1IQuitqE1ki5A2cj3XLnqf): A comprehensive overview of Loom, Monoli’s unified execution environment, focusing on multi-VM equivalent execution and the role of an intermediate representation in enabling cross-VM compatibility.

* [\[Issue\] Intra-chain Parallelism](https://nicholas.feishu.cn/wiki/QfuqwL318ipbyYkKmArc67Btn1g): Native scaling through intra-chain parallelism.

#### *DB, DA*
* [[Issue] Designing a DAG-Compatible, Multi-VM Scalable Storage Layer for Monoli](): A design exploration of Monoli’s scalable, DAG-compatible storage layer to support multi-VM execution.

#### *Architecture*
* [Gizmo](https://nicholas.feishu.cn/wiki/PN5iw3MN7iLKWVkeLpmclVaUn9g): Modular Rust SDK for building Monoli chains.

* [\[Issue\] Rebuilding vs Refining](#): Comparing engineering-optimized vs innovation-driven architecture paths.

* [\[Issue\] What's the Ideal Block Size](https://nicholas.feishu.cn/wiki/FEnIwzQyviOls1k8pngc5W2EnAU) Finding the Optimal Block Size and Scalability Trade-offs in High-Performance Blockchains.

* [\[Issue\] Native Accounts for On-Chain Finance](https://nicholas.feishu.cn/wiki/Mlj6wfTEviPKcckdktVcP62cnhT) Account Model Designs in Representative Blockchains and Monoli's Design Exploration.

#### *DEX, DeFi*

* [\[Issue\] DPS Benchmarking Methods](https://nicholas.feishu.cn/wiki/YRKUwMpigi2LYvkeV3xcv27Xnyd): Measuring throughput and latency using AMM-style benchmarks.
* [\[Issue\] Controls Over Perpetual Contract Trading](https://nicholas.feishu.cn/wiki/C4GOwP5aEiX6BskixNHcx1sMn2b): Design of index price, mark price, and funding rate mechanisms.
* [\[Issue\] Why Fully Transparent Trading Markets Are Beneficial](https://nicholas.feishu.cn/wiki/MS7aw1pHxiGbH4kcuLPcsvzenxg) Benefits and Merits of Transparent Trading Markets.
* [\[Issue\] Feasibility of On-Chain Dark Pools](https://nicholas.feishu.cn/wiki/AqZpw7tPNiS8Ofk1zincP4oZnEd) Design and Implications of On-Chain Dark Pool Mechanisms.
* [\[Paper\] Structured Finance of TradFi Inspires DeFi (Monoli Structured Derivatives Protocol)](https://nicholas.feishu.cn/wiki/DDwywlelQiqRfXko4F8cniY6nr9): Applying structured finance instruments (MTP & MCD) in DeFi.

* [[Issue] Asset Tokenization Meets DeFi: Enabling On-Chain Structured Products with Native Yield Logic](https://nicholas.feishu.cn/wiki/UOA6w3orwihjEIkHU6scxfWTnUe?from=from_copylink): A study of how asset tokenization and native yield logic power on-chain structured products, bridging DeFi innovation with traditional financial engineering.

* [[Issue] Structured Finance of TradFi Inspires DeFi Protocol (Monoli Structured Derivatives Protocol)](https://nicholas.feishu.cn/wiki/DDwywlelQiqRfXko4F8cniY6nr9?from=from_copylink): Exploring how structured finance principles from TradFi can inspire multi-layered derivative protocols in DeFi, enabling more sophisticated, composable financial products on Monoli.

* [[Paper] Plaid: Optimizing Decentralized Central Limit Orderbooks: Incentive Mechanisms and Matching Engine Efficiency](https://nicholas.feishu.cn/wiki/IrgFwa9ijikrI7k1sx3c1yjsnxa?from=from_copylink): Plaid provides a performant, low-latency on-chain CLOB protocol powered by Monoli's smart accounts and parallel execution, serving as a low-cost public good to enhance ecosystem liquidity and DeFi user experience.

#### *OTHER*

* [Monoli Financial Forecast](https://nicholas.feishu.cn/wiki/GtTGwvHO0ii0zYkdpWqcsO5dn3h) Financial Projections for Monoli's Business Operations.
* [Monoli Litepaper](https://nicholas.feishu.cn/wiki/In06wTQ4zi7zM1kQTFcc8cklnVb)
* [Monoli Enhancement Proposals (MEPs)](https://nicholas.feishu.cn/wiki/V87Zwm8EWiWPSXkA7lHcaOQengf)
* [\[Paper\] From Multi-chain Integration to Unified Operations](https://nicholas.feishu.cn/wiki/ZWr0wJwxuib9r6kXGjEcDZTuncc): Early explorations of omnichain infrastructure.
* [\[Paper\] The MA End Game – Massive Adoption Capability](https://nicholas.feishu.cn/wiki/M9Cuw8PWVin7lhkx2MZcLkk4nAg): Vision for enabling mass adoption in Web3, a guiding principle for Monoli.