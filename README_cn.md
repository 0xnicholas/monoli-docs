> 该文档索引包括Monoli主要研究项目和课题

## About Monoli
Monoli代表了[Lico labs]()研究的一个高性能区块链L1和其主要DeFi生态项目，目前处于产研深入探索阶段。Monoli旨在创建一个超高效区块链基础设施和结构化金融生态系统。它包括三个主要项目： [Monoli L1]()，[Monoli Perp DEX]()及[Monoli Vaults]()。

## Monoli L1
Monoli旨在通过全方面加强或重构区块链Layer 1的各个部分来提升区块链性能，目标为120,000TPS，为DeFi、高频交易和dApp提供web2级别的链上体验。
Monoli的主要是解耦并独立升级各L1组件（比如解耦共识和执行、执行和传播等），同时保持不同层的变速协同，这种架构能够适应区块链技术的长周期演进需求，同时在每个阶段都能进行最佳实践，在当下获得最优基础设施。

Monoli 在多个主要领域进行优化，从而实现了自身卓越的性能和全链执行的提升，并大大提高了去中心化/可扩展性的权衡。这些主要的改进领域如：

- **MonoBFT**，一种基于dag结构的高频最终性的BFT协议，旧版本为Hotstuff衍生。
- **TVA**， 交易顺序预先确定并可验证，同时异步执行。
- **ForceSync**，Monoli专有同步系统，用来确保所有节点一致。
- **Execution Framework**，一种VM无关（VM-Agnostic）的执行框架。
- **Loom**，一种VMs混合执行网络，主要包括LoomVM，一个由RISC-V编译支持的安全且确定的字节码虚拟机（旧版为rWASM VM）。和VMs等效执行环境。
- **MonoDB**，由RocksDB改进而来的分层存储数据库。
- **TurboCast**，可靠的高效网络传播机制，采用了动态广播树。
- **LiquiBoost**，Monoli原生合约，用于节点激励和开发者激励。

以及 [Gazer]( https://github.com/0xnicholas/gazer) (Monoli L1 Framework & SDK)


## Monoli DEX
Monoli DEX是Monoli L1网络的原生Perp DEX，基于订单薄，交易处理速度快。旨在实现高频交易与中心化交易所几乎相同的用户体验，并支持超过100多种不同代币对的杠杆交易环境。
Monoli DEX 提供了一个强大的交易平台，适合高频交易者、专业交易员以及那些希望利用杠杆和永续合约进行市场投机的用户。通过其创新的技术架构和机制，使得加密衍生品交易更加高效、安全和公平。
DEX的技术基础皆得益于Monoli L1的高效特性，大幅提升了交易效率，能够使得交易者进行自动化策略和高频交易。

Monoli DEX提供以下四种交易方式：
1. **Market Order**：以当前市场价格立即执行交易。
2. **Limit Order**：以指定的期望价格执行交易。
3. **Scale Order**：在设定的价格范围内建立并执行多个限价订单。
4. **TWAP**：在固定的时间间隔内将一个订单分成多个订单执行交易。

除了特定代币的永续合约，Monoli DEX 还提供以下类型的交易工具：
- **指数永续合约**：提供各种区块链生态系统指数的永续期货交易，例如追踪特定蓝筹 NFT 集合平均底价的指数 (NFTI-USD)。
- **Vaults**：包括做市策略Vault（用户自定义做市和平台做市 MLP, Monoli Liquidity Provider）；结构化Vault（MTP, Monoli Tranche Perp Vault），以及信用违约风险衍生品库（MCD, Monoli Credit Default Vault）。


## Resources

Website: https://monoli.xyz/

### L1
- [Monoli L1 [draft v0.8.3]](https://nicholas.feishu.cn/wiki/A301w7iE5ikIgikRasScq9OxnYg) (main doc)
- [Monoli L1 [draft v0.7.2]](https://nicholas.feishu.cn/wiki/RMAlwhsbZi1lYTkGheNcip7gnnc?from=from_copylink)
- [Monoli L1 Tech Book](https://nicholas.feishu.cn/wiki/OPJuwcVayi27k5klYeYcR2ixnSb)
- [Monoli Developer Docs](https://nicholas.feishu.cn/wiki/JpM6waMvIijcohkSuUncbVHNnUe)


### DEX
- [Monoli Perp DEX [v1.2]](https://nicholas.feishu.cn/wiki/Ecy3wEeKyi09TXkbupncOVosn0d) (main doc)
- [DEX Product Prototype](https://nicholas.feishu.cn/wiki/Rqknwd9yHiMa8ykWIkOcoHGGned)
- [DEX Risk Management and Cases](https://nicholas.feishu.cn/wiki/Z4WawXpb5iqz7QkCazrcWFqxnXe)
- [Monoli DEX Tech Docs](https://nicholas.feishu.cn/wiki/CvqYwM7eliHImLkSGmPcSPByn6d)

### Ecosystem
* [**Monogram**](https://nicholas.feishu.cn/wiki/IQlGwoq4QiyGGFk5Y0rcU51Ingg): Monoli上的一个合成美元协议，提供了一个由delta中性策略支持的加密原生稳定币。$M结合了挂钩稳定性和内在收益率，使其成为链上金融应用的坚实基础。

* [**Plaid**](https://nicholas.feishu.cn/wiki/IrgFwa9ijikrI7k1sx3c1yjsnxa?from=from_copylink): Plaid是Monoli的原生链上CLOB协议，为DeFi应用程序提供统一、高效的流动性，提供精确交易，并为Monoli的链上金融生态系统形成一个共享流动性层。

* [**Sunwell**](https://nicholas.feishu.cn/wiki/UOA6w3orwihjEIkHU6scxfWTnUe?from=from_copylink): Sunwell协议是将结构性金融商品变为链上金融原语的关键一步，旨在建立一套支持资产代币化、原生收益产生与结构化包装的链上协议，面向高效链上融资、风险定价与收益工程的 DeFi 应用。

* **Dakai**: 以意图为中心的协议，引入了一个声明式交易模型，将执行的复杂性从用户转移到求解器网络。

* Monoli **Bridge**: Monoli Bridge是一个原生的跨链网关，它支持在Monoli和以太坊（以及更多）之间快速、低成本和安全的资产转移，通过去中心化的架构支持无缝互操作。

* **Octa**: 一个去中心化的MPC签名者网络，旨在通过零信任密码学模型和高性能的去中心化架构解决区块链互操作性挑战。

* **Bagel Wallet**: 一个支持意图的可编程钱包，它允许用户表达所需的结果，同时抽象出交易的复杂性。

### Papers

#### *Consensus*

* [[Issue] Rethinking Consensus for Ordering-First Blockchains: Commit-Only Snapshots from Deterministic DAG ](https://nicholas.feishu.cn/wiki/UIEAwFWRhi7mXFkUxjbcTgIAndh?from=from_copylink): ”Ordering-First“, 弱共识理念提出，其中基于dag的确定性执行（TVA）定义了交易顺序，而共识层只提交快照哈希，从而将排序与共识解耦。

* [[Issue] Consensus-less Transaction Confirmation: Optimizing Low-Latency, High-Throughput Blockchain Systems with BFT Broadcast and Explicit Dependency Models](https://nicholas.feishu.cn/wiki/Ss1NwgVQTiaX92kEsrwcpwtXnrb?from=from_copylink): 探索了如何通过BFT广播和显式依赖模型来实现无共识的交易确认，以大幅优化延迟和吞吐量。

* [\[Issue\] A DAG-Structured BFT Protocol for High-Frequency Finality](https://nicholas.feishu.cn/wiki/Bpc0wOMBEiZhkpko1gucyHlsnCc): 采用DAG结构改进共识机制，并对比Hotstuff方案。

* [\[Issue\] High Performance, Fast Finality, Fork-Resistant BFT](https://nicholas.feishu.cn/wiki/QHzww7kL4iTMwxkiqNLcadAQnLf): 较早版本对MonoBFT的研究，基于HotStuff系列。

* [\[Issue\] 1 Slot, 1s Finality](https://nicholas.feishu.cn/wiki/UbVpw5ccLilDt0k2g4xcFR2LnPh): 1slot/1s实现最终性的方案

#### *Execution*
* [[Issue] DAG-Based Transaction Ordering Without Consensus: Designing a Verifiable Sequencer via TVA](https://nicholas.feishu.cn/wiki/AXvWw3pnBix6bIkUUCOc1rQpnnc?from=from_copylink): 探索将TVA集成到基于dag的区块链中，在不依赖共识层排序的情况下实现确定性、可验证的交易排序，实现高通量的并行执行。

* [[Paper] LoomVM: A Secure and Deterministic Bytecode Virtual Machine Powered by RISC-V Frontend Compilation](https://nicholas.feishu.cn/wiki/KFw9wBl7ViOaTdke0YTcEqPtnsh?from=from_copylink): 提出一种面向链上执行的安全确定性字节码虚拟机LoomVM，将RISC-V二进制文件转换为可验证、gas感知的字节码，以实现在Monoli区块链中高效、可分析、zk友好的智能合约执行。

* [[Issue] Abstract Execution in Blockchain: A Study on VM-Agnostic Architecture Design](https://nicholas.feishu.cn/wiki/O3ebwHIPJiH5DykdHSsccL6xn6d?from=from_copylink): 研究抽象执行体系结构，通过与虚拟机无关的、模块化的、开放的、可组合的、跨不同区块链系统的执行来隐藏区块链复杂性。

* [[Issue] Shared Execution as a Public Good:  Scalable, Permissionless, and Shared Execution for Multi-VM Systems](https://nicholas.feishu.cn/wiki/HaBCwYiiGiodqrk0bWCcEENWn1g?from=from_copylink): 探索了Loom如何作为公共产品实现共享执行——支持在开放执行网络中跨异构虚拟机的可扩展、免许可执行。

* [[Issue] Multi-VM Equivalent Execution Methods and an Intermediate Representation in a Unified Execution Environment](https://nicholas.feishu.cn/wiki/DUmIw1IQuitqE1ki5A2cj3XLnqf): 全面概述了Loom， Monoli的统一执行环境，多虚拟机等效执行和中间表示在实现跨虚拟机兼容性方面的作用。

* [[Agenda] Planning the Monoli Blockchain Smart Contract Language](https://nicholas.feishu.cn/wiki/AcMuwXbfZiBHaqkbox0comGnnZc?from=from_copylink): 定义Monoli基于Rust的智能合约语言的需求、架构和路线图，以及支持Rust和Solidity智能合约的虚拟机。

* [\[Issue\] Parallelism Meets Finality: A Hybrid DAG-Blockchain Execution Model](https://nicholas.feishu.cn/wiki/IJVnwmHITiEgrvkREvFcHBs4n9e): DAG + 区块链混合结构的执行模型。

* [\[Issue\] Intra-chain Parallelism](https://nicholas.feishu.cn/wiki/QfuqwL318ipbyYkKmArc67Btn1g): 并行执行扩容专题分析

#### *DB, DA*
* [[Issue] Designing a DAG-Compatible, Multi-VM Scalable Storage Layer for Monoli](https://nicholas.feishu.cn/wiki/AjMAwGpTaim0NjkHbTJctRcznmk?from=from_copylink): Monoli可扩展的、兼容dag的存储层的设计探索，以支持多虚拟机执行。

#### *Architecture*
- [Gazer: Monoli L1 Framework & SDK](https://nicholas.feishu.cn/wiki/PN5iw3MN7iLKWVkeLpmclVaUn9g?from=from_copylink) Gazer是一个Rust框架，用于以模块化和可扩展的方式构建区块链。它是一组用于构建Monoli链的库和原语

- [[Issue] Rebuilding vs Refining: Architectural Paradigms for High-Performance Blockchains]() 下一代区块链架构探索，工程优化型和革新型架构对比

- [[Issue] What's the ideal block size](https://nicholas.feishu.cn/wiki/FEnIwzQyviOls1k8pngc5W2EnAU?from=from_copylink) 寻找高性能链中最佳区块大小与可扩展性

- [[Issue] Native Accounts for On-chain Finance](https://nicholas.feishu.cn/wiki/Mlj6wfTEviPKcckdktVcP62cnhT?from=from_copylink) 讨论不同代表性区块链的账户模型设计，Monoli Accounts设计探索

#### *DEX, DeFi*
- [[Issue] DPS Benchmarking Methods](https://nicholas.feishu.cn/wiki/YRKUwMpigi2LYvkeV3xcv27Xnyd?from=from_copylink) 以吞吐量和延迟为性能考量，并以AMM为操作基准进行系统测试分析
- [[Issue] Controls over perpetual contract trading](https://nicholas.feishu.cn/wiki/C4GOwP5aEiX6BskixNHcx1sMn2b?from=from_copylink) index price, mark price, funding rate 永续合约交易主要控制变量的不同设计
- [[Issue] Why fully transparent trading markets are beneficial](https://nicholas.feishu.cn/wiki/MS7aw1pHxiGbH4kcuLPcsvzenxg?from=from_copylink) 对透明交易市场的正面分析
- [[Issue]Feasibility of On-chain Dark Pools](https://nicholas.feishu.cn/wiki/AqZpw7tPNiS8Ofk1zincP4oZnEd?from=from_copylink)  链上暗池讨论
- [[Paper] Structured Finance of TradFi Inspires DeFi Protocol (Monoli Structured Derivatives Protocol)](https://nicholas.feishu.cn/wiki/DDwywlelQiqRfXko4F8cniY6nr9)  从TradFi中借鉴结构化金融产品用于DeFi，以及Monoli结构化Vaults MTP和MCD的设计


* [[Issue] Asset Tokenization Meets DeFi: Enabling On-Chain Structured Products with Native Yield Logic](https://nicholas.feishu.cn/wiki/UOA6w3orwihjEIkHU6scxfWTnUe?from=from_copylink): 资产代币化和原生收益率逻辑如何影响链上结构性产品，将DeFi创新与传统金融工程结合起来的研究。

* [[Issue] Structured Finance of TradFi Inspires DeFi Protocol (Monoli Structured Derivatives Protocol)](https://nicholas.feishu.cn/wiki/DDwywlelQiqRfXko4F8cniY6nr9?from=from_copylink): 探索来自TradFi的结构化金融原语如何启发DeFi中的多层衍生协议，使Monoli上的更复杂、可组合的金融产品成为可能。

* [[Paper] Plaid: Optimizing Decentralized Central Limit Orderbooks: Incentive Mechanisms and Matching Engine Efficiency](https://nicholas.feishu.cn/wiki/IrgFwa9ijikrI7k1sx3c1yjsnxa?from=from_copylink): Plaid提供了一个高性能，低延迟的链上CLOB协议，由Monoli提供支持，作为一个低成本的公共产品，以增强生态系统的流动性和DeFi用户体验。

#### *OTHER*
- [Financial Statement for Monoli](https://nicholas.feishu.cn/wiki/GtTGwvHO0ii0zYkdpWqcsO5dn3h)  Monoli项目财务预测
- [Monoli Litepaper](https://nicholas.feishu.cn/wiki/In06wTQ4zi7zM1kQTFcc8cklnVb?from=from_copylink)  Monoli简要概述
- [MEPs](https://nicholas.feishu.cn/wiki/V87Zwm8EWiWPSXkA7lHcaOQengf?from=from_copylink) Monoli改进提案记录
- [[Paper] From Multi-chain Integration to Unified Operations: The Omnichain Operationally Harmonized Infrastructure [draft]](https://nicholas.feishu.cn/wiki/ZWr0wJwxuib9r6kXGjEcDZTuncc?from=from_copylink) 链抽象和全链互操作性的早期思考
- [[Paper] The MA End Game - Massive Adoption Capability Solutions](https://nicholas.feishu.cn/wiki/M9Cuw8PWVin7lhkx2MZcLkk4nAg?from=from_copylink) 实现web3大规模采用需要解决的问题，早期指引了Monoli的愿景