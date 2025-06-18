# About Monoli
[Monoli]() 是一个高性能区块链 L1，旨在创建一个链上流动性平台和结构化金融生态系统。它包括三个主要项目： [Monoli L1]()，[Monoli Perp DEX]()和[Monoli Vaults]()。

## Monoli L1
Monoli L1旨在通过分别加强共识和执行层来优化区块链性能，为DeFi、高频交易和dApp提供web2级别的链上体验。其核心洞察在于，现有区块链在高交易吞吐量、低延迟和跨链互操作性方面存在瓶颈，难以竞争CEXs的实时性能和流动性需求。
Monoli 的思路是通过共识和执行独立进行，优化共识机制，采用确定性的交易排序和异步执行，来快速完成共识。而在执行层，通过设计一个与VM无关的执行框架，增强了可扩展性、交易效率和跨链互操作性。同时在执行环境中，通过Loom整合了多VM，使开发者能在任意VM上进行build，使得在不同链上运行的智能合约在执行逻辑、状态管理等方面表现一致，实现了不需要更改代码的应用迁移和开发。

Monoli 在多个主要领域进行优化，从而实现了自身卓越的性能和全链执行的提升，并大大提高了去中心化/可扩展性的权衡。这些主要的改进领域如：

- [MonoBFT]()
- [TVA]()
- [Execution Framework]()
- [Loom]()
- [MonoDB]()
- [TurboCast]()
- [LiquiBoost]()

以及 [Gazer]( https://github.com/0xnicholas/gazer) (Monoli L1 Framework & SDK)


## Monoli DEX
Monoli DEX是Monoli L1网络的原生Perp DEX，基于订单薄，交易处理速度快。旨在实现高频交易与中心化交易所几乎相同的用户体验，并支持超过100多种不同代币对的杠杆交易环境。
Monoli DEX 提供了一个强大的工具箱，适合高频交易者、专业交易员以及那些希望利用杠杆和永续合约进行市场投机的用户。通过其创新的技术架构和机制，使得加密衍生品交易更加高效、安全和公平。
DEX的技术基础皆得益于Monoli L1的高效特性，MonoBFT优化共识针对端到端延迟做了结构性优化；订单簿利用链下匹配和Fast Block，大幅优化了交易效率；Loom系统提供了统一的执行环境和高效互操作，更进一步降低了交易延迟。这种性能能够使得交易者进行自动化策略和高频交易。

Monoli DEX提供以下四种交易方式：
1. Market order：以当前市场价格立即执行交易。
2. Limit order：以指定的期望价格执行交易。
3. Scale order：在设定的价格范围内建立并执行多个限价订单。
4. TWAP：在固定的时间间隔内将一个订单分成多个订单执行交易。

除了特定代币的永续合约，Monoli DEX 还提供以下类型的交易工具：
- 指数永续合约：提供各种区块链生态系统指数的永续期货交易，例如追踪特定蓝筹 NFT 集合平均底价的指数 (NFTI-USD)。
- [Vaults]()：包括做市策略Vault（用户自定义做市和平台做市 MLP, Monoli Liquidity Provider）；结构化Vault（MTP, Monoli Tranche Perp Vault），以及信用违约风险衍生品库（MCD, Monoli Credit Default Vault）。

大多数以 Orderbook 为基础的DEX 不是缺乏自己的网络，就是其架构也只专注于交易功能，因此无法形成从属的生态系统，与 DEX 产生协同效应。相比之下，Monoli 作为 Layer 1网络，并不仅限于DEX，而是愿景建立一个庞大的生态系统，结合链上用户与DEX用户，通过生态内各dApp、利用MEP 发行的原生代币、以及Monoli多VM混合执行的引进，创造出单一DEX无法达到的流行性网络效应。

## Resources

Website: https://monoli.xyz/

_L1_
- [Monoli L1 [draft v0.7.1]](https://nicholas.feishu.cn/wiki/A301w7iE5ikIgikRasScq9OxnYg) (main doc)
- [Monoli L1 Tech Book](https://nicholas.feishu.cn/wiki/OPJuwcVayi27k5klYeYcR2ixnSb)
- [Monoli Developer Docs](https://nicholas.feishu.cn/wiki/JpM6waMvIijcohkSuUncbVHNnUe)


_DEX_
- [Monoli Perp DEX [v1.2]](https://nicholas.feishu.cn/wiki/Ecy3wEeKyi09TXkbupncOVosn0d) (main doc)
- [DEX Product Prototype](https://nicholas.feishu.cn/wiki/Rqknwd9yHiMa8ykWIkOcoHGGned)
- [DEX Risk Management and Cases](https://nicholas.feishu.cn/wiki/Z4WawXpb5iqz7QkCazrcWFqxnXe)
- [Monoli DEX Tech Docs](https://nicholas.feishu.cn/wiki/CvqYwM7eliHImLkSGmPcSPByn6d)

_Ecosystem Protocols_
- [Monogram](https://nicholas.feishu.cn/wiki/UOA6w3orwihjEIkHU6scxfWTnUe) (Asset tokenization and yield protocols)

_相关文档_
- [Financial Statement for Monoli](https://nicholas.feishu.cn/wiki/GtTGwvHO0ii0zYkdpWqcsO5dn3h)  Monoli项目财务预测
- [Gazer: Monoli L1 Framework & SDK]( https://github.com/0xnicholas/gazer) Gazer, Monoli L1的核心开发框架
- [[Issue] Intra-chain parallelism, primary solution for native scaling](https://nicholas.feishu.cn/wiki/QfuqwL318ipbyYkKmArc67Btn1g)  并行执行扩容专题
- [[Issue] 1 slot, 1s finality](https://nicholas.feishu.cn/wiki/UbVpw5ccLilDt0k2g4xcFR2LnPh) 1slot/1s实现最终性的方案
- [[Issue] Why fully transparent trading markets are beneficial](https://nicholas.feishu.cn/wiki/MS7aw1pHxiGbH4kcuLPcsvzenxg?from=from_copylink)  对透明交易市场的正面分析
- [[Issue]Feasibility of On-chain Dark Pools](https://nicholas.feishu.cn/wiki/AqZpw7tPNiS8Ofk1zincP4oZnEd?from=from_copylink)  链上暗池讨论
- [[Issue] Fundamental enhancement of the Monoli execution architecture, replacing the rWASM Runtime with the RISC-V Runtime](https://nicholas.feishu.cn/wiki/KFw9wBl7ViOaTdke0YTcEqPtnsh?from=from_copylink) 执行层RISC-V Runtime建设，替代原rWASM Runtime
- [[Paper] Structured Finance of TradFi Inspires DeFi Protocol (Monoli Structured Derivatives Protocol)](https://nicholas.feishu.cn/wiki/DDwywlelQiqRfXko4F8cniY6nr9  从TradFi中借鉴结构化金融产品用于DeFi，以及Monoli结构化Vaults MTP和MCD的设计
- [[Paper] From Multi-chain Integration to Unified Operations: The Omnichain Operationally Harmonized Infrastructure [draft]](https://nicholas.feishu.cn/wiki/ZWr0wJwxuib9r6kXGjEcDZTuncc?from=from_copylink) 链抽象和全链互操作性的早期思考
- [[Paper] The MA End Game - Massive Adoption Capability Solutions](https://nicholas.feishu.cn/wiki/M9Cuw8PWVin7lhkx2MZcLkk4nAg?from=from_copylink)  实现web3大规模采用需要解决的问题，指引Monoli的愿景
- [Monoli Litepaper](https://nicholas.feishu.cn/wiki/In06wTQ4zi7zM1kQTFcc8cklnVb?from=from_copylink)  Monoli简要概述
- [MEPs](https://nicholas.feishu.cn/wiki/V87Zwm8EWiWPSXkA7lHcaOQengf?from=from_copylink) Monoli改进提案记录
