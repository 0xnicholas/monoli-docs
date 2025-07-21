[[中文]](/README_cn.md)

> This index outlines the major research tracks and initiatives under the Monoli project.

## About Monoli

**Monoli** is a high-performance Layer 1 blockchain and its associated native DeFi ecosystem, developed under [Lico labs](). Currently in an intensive R\&D phase, Monoli aims to create an ultra-efficient blockchain infrastructure and a structured financial ecosystem. The Monoli ecosystem consists of three core pillars: [Monoli L1](), [Monoli Perp DEX](), and [Monoli Vaults]().

## Monoli L1

Monoli is designed to push the performance limits of Layer 1 blockchains by decoupling and independently optimizing core components—such as consensus, execution, and networking—while maintaining *variable-speed coordination* between layers. This architectural approach enables Monoli to align with the long-term evolutionary trajectory of blockchain technology while achieving best-in-class infrastructure in every stage.

With a target throughput of **120,000 TPS**, Monoli aims to deliver a Web2-grade user experience for DeFi, high-frequency trading (HFT), and on-chain applications. Key innovations and enhancements include:

* **[MonoBFT]()**, A high-frequency finality BFT protocol built on DAG structures (earlier based on a HotStuff derivative).
* **[TVA]()**, A time-verifiable asynchronous execution model that deterministically pre-orders transactions while enabling asynchronous execution.
* **[ForceSync]()**, Monoli’s proprietary state and block synchronization system that ensures robust node consistency.
* **[Execution Framework]()**, A VM-agnostic execution environment supporting diverse smart contract runtimes.
* **[Loom]()**, A hybrid VM execution network, centered around **LoomVM**, a secure and deterministic bytecode virtual machine compiled from RISC-V (replacing rWASM). It supports multi-VM equivalent execution environments.
* **[MonoDB]()**, A multi-tiered database built on top of RocksDB, optimized for performance and scalability.
* **[TurboCast]()**, A high-efficiency networking layer using adaptive broadcast trees for rapid message propagation.
* **[LiquiBoost]()**, A native on-chain incentive protocol designed to reward both validators and developers.

In addition, Monoli provides a modular Rust SDK and framework named **[Gazer](https://github.com/0xnicholas/gazer)** for building custom blockchain systems.

## Monoli DEX

**Monoli DEX** is the native perpetual futures exchange on the Monoli L1 network. Built on a high-speed orderbook matching engine, it aims to deliver near-centralized exchange performance for high-frequency and professional traders. It supports leveraged trading for over 100 token pairs.

Designed for power users—quantitative traders, professionals, and leverage speculators—Monoli DEX maximizes efficiency, fairness, and execution speed by leveraging the full performance capabilities of Monoli L1.

The exchange supports four primary order types:

1. **Market Orders** – Execute immediately at the best available price.
2. **Limit Orders** – Execute at a user-specified price.
3. **Scale Orders** – Place multiple limit orders across a price range.
4. **TWAP** – Time-weighted average price execution over intervals.

Beyond standard perps, Monoli DEX also offers structured perpetual products:

* **Index Perps** – Trade ecosystem indices like NFT floor price composites (e.g., *NFTI-USD*).
* **[Vaults]()**:

  * Market-making vaults (user-customized and platform-driven via **MLP**, Monoli Liquidity Provider).
  * Structured derivative vaults (**MTP**, Monoli Tranche Perp Vault).
  * Credit risk protection vaults (**MCD**, Monoli Credit Default Vault).

## Resources

**Website**: [https://monoli.xyz](https://monoli.xyz)

### *L1*

* [Monoli L1 \[draft v0.8\]](https://nicholas.feishu.cn/wiki/A301w7iE5ikIgikRasScq9OxnYg) (main doc)
* [Monoli L1 \[draft v0.7.2\]](https://nicholas.feishu.cn/wiki/RMAlwhsbZi1lYTkGheNcip7gnnc)
* [Monoli L1 Tech Book](https://nicholas.feishu.cn/wiki/OPJuwcVayi27k5klYeYcR2ixnSb)
* [Developer Docs](https://nicholas.feishu.cn/wiki/JpM6waMvIijcohkSuUncbVHNnUe)

### *DEX*

* [Monoli Perp DEX \[v1.2\]](https://nicholas.feishu.cn/wiki/Ecy3wEeKyi09TXkbupncOVosn0d) (main doc)
* [DEX Product Prototype](https://nicholas.feishu.cn/wiki/Rqknwd9yHiMa8ykWIkOcoHGGned)
* [DEX Risk Management and Case Studies](https://nicholas.feishu.cn/wiki/Z4WawXpb5iqz7QkCazrcWFqxnXe)
* [DEX Technical Documentation](https://nicholas.feishu.cn/wiki/CvqYwM7eliHImLkSGmPcSPByn6d)

### *Ecosystem Protocols*

* [Monogram](https://nicholas.feishu.cn/wiki/IQlGwoq4QiyGGFk5Y0rcU51Ingg): L1 native synthetic dollar protocol.($M stablecoin)

### Research Topics

#### *Consensus*

* [\[Issue\] A DAG-Structured BFT Protocol for High-Frequency Finality](https://nicholas.feishu.cn/wiki/Bpc0wOMBEiZhkpko1gucyHlsnCc): Adopts DAG-based consensus for high-frequency environments; comparison with HotStuff.
* [\[Issue\] High Performance, Fast Finality, Fork-Resistant BFT](https://nicholas.feishu.cn/wiki/QHzww7kL4iTMwxkiqNLcadAQnLf): Early research on MonoBFT based on HotStuff series.
* [\[Issue\] 1 Slot, 1s Finality](https://nicholas.feishu.cn/wiki/UbVpw5ccLilDt0k2g4xcFR2LnPh): Achieving 1-slot, 1-second finality.

#### *Execution*

* [\[Issue\] Parallelism Meets Finality: A Hybrid DAG-Blockchain Execution Model](https://nicholas.feishu.cn/wiki/IJVnwmHITiEgrvkREvFcHBs4n9e): Merging DAG concurrency with blockchain finality guarantees.
* [\[Paper\] LoomVM: A Secure and Deterministic Bytecode Virtual Machine Powered by RISC-V](https://nicholas.feishu.cn/wiki/KFw9wBl7ViOaTdke0YTcEqPtnsh)
* [\[Issue\] From RISC-V ELF to LBC](https://nicholas.feishu.cn/wiki/Bgr8wq3XdioEJwkLYgjcLDWNnVb): Building a compiler and VM runtime from RISC-V ELF to Loom Bytecode (LBC).
* [\[Issue\] Loom Runtime Architecture](https://nicholas.feishu.cn/wiki/LdzZwdOGXiYWM3k1ZsMcTVJ4nAc): VM interpreter, memory model, and hostcall system.
* [\[Issue\] Intra-chain Parallelism](https://nicholas.feishu.cn/wiki/QfuqwL318ipbyYkKmArc67Btn1g): Native scaling through intra-chain parallelism.
* [\[Issue\] Multi-VM Equivalence and Intermediate Representation](https://nicholas.feishu.cn/wiki/DUmIw1IQuitqE1ki5A2cj3XLnqf): Unified intermediate representation for equivalent multi-VM execution (e.g., rWASM).

#### *Architecture*

* [Gazer](https://nicholas.feishu.cn/wiki/PN5iw3MN7iLKWVkeLpmclVaUn9g): Modular Rust SDK for building Monoli chains.
* [\[Issue\] Rebuilding vs Refining](#): Comparing engineering-optimized vs innovation-driven architecture paths.
* [\[Issue\] What's the Ideal Block Size](https://nicholas.feishu.cn/wiki/FEnIwzQyviOls1k8pngc5W2EnAU) Finding the Optimal Block Size and Scalability Trade-offs in High-Performance Blockchains.
* [\[Issue\] Native Accounts for On-Chain Finance](https://nicholas.feishu.cn/wiki/Mlj6wfTEviPKcckdktVcP62cnhT) Account Model Designs in Representative Blockchains and Monoli's Design Exploration.

#### *DEX*

* [\[Issue\] DPS Benchmarking Methods](https://nicholas.feishu.cn/wiki/YRKUwMpigi2LYvkeV3xcv27Xnyd): Measuring throughput and latency using AMM-style benchmarks.
* [\[Issue\] Controls Over Perpetual Contract Trading](https://nicholas.feishu.cn/wiki/C4GOwP5aEiX6BskixNHcx1sMn2b): Design of index price, mark price, and funding rate mechanisms.
* [\[Issue\] Why Fully Transparent Trading Markets Are Beneficial](https://nicholas.feishu.cn/wiki/MS7aw1pHxiGbH4kcuLPcsvzenxg) Benefits and Merits of Transparent Trading Markets.
* [\[Issue\] Feasibility of On-Chain Dark Pools](https://nicholas.feishu.cn/wiki/AqZpw7tPNiS8Ofk1zincP4oZnEd) Design and Implications of On-Chain Dark Pool Mechanisms.
* [\[Paper\] Structured Finance of TradFi Inspires DeFi (Monoli Structured Derivatives Protocol)](https://nicholas.feishu.cn/wiki/DDwywlelQiqRfXko4F8cniY6nr9): Applying structured finance instruments (MTP & MCD) in DeFi.

#### *OTHER*

* [Monoli Financial Forecast](https://nicholas.feishu.cn/wiki/GtTGwvHO0ii0zYkdpWqcsO5dn3h) Financial Projections for Monoli's Business Operations.
* [Monoli Litepaper](https://nicholas.feishu.cn/wiki/In06wTQ4zi7zM1kQTFcc8cklnVb)
* [Monoli Enhancement Proposals (MEPs)](https://nicholas.feishu.cn/wiki/V87Zwm8EWiWPSXkA7lHcaOQengf)
* [\[Paper\] From Multi-chain Integration to Unified Operations](https://nicholas.feishu.cn/wiki/ZWr0wJwxuib9r6kXGjEcDZTuncc): Early explorations of omnichain infrastructure.
* [\[Paper\] The MA End Game – Massive Adoption Capability](https://nicholas.feishu.cn/wiki/M9Cuw8PWVin7lhkx2MZcLkk4nAg): Vision for enabling mass adoption in Web3, a guiding principle for Monoli.