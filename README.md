[[中文]](README_cn.md)

# About Monoli
[Monoli]() is a high-performance blockchain L1 designed to create an on-chain liquidity platform and structured finance ecosystem. It includes three major projects: [Monoli L1](), [Monoli Perp DEX]() and [Monoli Vaults]().

## Monoli L1
Monoli L1 optimizes blockchain performance by enhancing the consensus and execution layers respectively, providing a web2 level on-chain experience for Defi, high-frequency trading and dapps. The core insight is that existing blockchains have bottlenecks in high transaction throughput, low latency, and cross-chain interoperability to compete for the real-time performance and liquidity needs of CEXs.

The idea of L1 is to optimize the consensus mechanism by performing consensus and execution independently, using deterministic transaction ordering and asynchronous execution to complete consensus quickly. At the execution layer, scalability, transaction efficiency and cross-chain interoperability are enhanced by designing a VM-agnostic execution framework. Meanwhile, in the execution environment, multiple VMs are integrated through Loom, enabling developers to build on any VM, so that smart contracts running on different chains perform consistently in terms of execution logic, state management, and so on, realizing application migration and development without the need to change code.

L1 is optimized in several key areas to achieve its own superior performance and omni-chain execution enhancements, and to greatly improve the decentralization/scalability trade-off. These major areas of improvement are as follows:

- [MonoBFT]()
- [TVA]()
- [Execution Framework]()
- [Loom]()
- [MonoDB]()
- [TurboCast]()
- [LiquiBoost]()

and [Gazer]( https://github.com/0xnicholas/gazer) (Monoli L1 Framework & SDK)


## Monoli DEX
Monoli DEX is the native Perp DEX for the Monoli L1 network, based on order thinning and fast transaction processing. Designed to enable high-frequency trading with virtually the same user experience as centralized exchanges, and supports a leveraged trading environment of over 100 different token pairs.

Monoli DEX offers a powerful toolbox for high-frequency traders, professional traders and those looking to speculate on the markets using leverage and perpetual contracts. Through its innovative technical architecture and mechanisms, it makes crypto derivatives trading more efficient, secure and fair.

DEX's technological foundation is made possible by the efficient features of Monoli L1, MonoBFT Optimized Consensus, which is structurally optimized for end-to-end latency; the Order Book, which leverages off-chain matching and Fast Block to dramatically optimize trading efficiency; and the Loom system, which provides a unified execution environment and efficient interoperability to further reduce trading latency. This performance enables traders to engage in automated strategies and high-frequency trading.

Monoli DEX offers the following four trading methods:
1. Market order: Immediate execution of a trade at the current market price.
2. Limit order: Execute a trade at a specified desired price.
3. Scale order: in the set price range to establish and execute multiple limit orders.
4. TWAP: A single order is divided into multiple orders to execute transactions within a fixed time interval.

In addition to token-specific perpetual contracts, Monoli DEX offers the following types of trading instruments:
- Index Perpetual Contracts: Offers perpetual futures trading on various blockchain ecosystem indices, such as an index tracking the average floor price of a specific blue chip NFT pool (NFTI-USD).
- [Vaults](): Includes Market Making Strategy Vaults (user-defined market making and platform market making MLP, Monoli Liquidity Provider); Structured Vaults (MTP, Monoli Tranche Perp Vault), and Credit Default Risk Derivatives Vaults (MCD, Monoli Credit Default Vault).

Most Orderbook-based DEXs either lack their own networks or have architectures that focus only on trading functionality, thus failing to form a subordinate ecosystem to synergize with DEXs. In contrast, Monoli, as a Layer 1 network, is not limited to DEX, but envisions a large ecosystem that combines on-chain and DEX users, creating a popular network effect that cannot be achieved by a single DEX through the dApps in the ecosystem, the native tokens issued by MEPs, and the introduction of Monoli's multi-VM hybrid execution.

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

_Related Papers_
- [Financial Statement for Monoli](https://nicholas.feishu.cn/wiki/GtTGwvHO0ii0zYkdpWqcsO5dn3h)
- [Gazer: Monoli L1 Framework & SDK]( https://github.com/0xnicholas/gazer)
- [[Issue] DPS Benchmarking Methods](https://nicholas.feishu.cn/wiki/YRKUwMpigi2LYvkeV3xcv27Xnyd?from=from_copylink)
- [[Issue] Controls over perpetual contract trading](https://nicholas.feishu.cn/wiki/C4GOwP5aEiX6BskixNHcx1sMn2b?from=from_copylink)
- [[Issue] Intra-chain parallelism, primary solution for native scaling](https://nicholas.feishu.cn/wiki/QfuqwL318ipbyYkKmArc67Btn1g)
- [[Issue] 1 slot, 1s finality](https://nicholas.feishu.cn/wiki/UbVpw5ccLilDt0k2g4xcFR2LnPh)
- [[Issue] Why fully transparent trading markets are beneficial](https://nicholas.feishu.cn/wiki/MS7aw1pHxiGbH4kcuLPcsvzenxg?from=from_copylink)
- [[Issue]Feasibility of On-chain Dark Pools](https://nicholas.feishu.cn/wiki/AqZpw7tPNiS8Ofk1zincP4oZnEd?from=from_copylink)
- [[Issue] Fundamental enhancement of the Monoli execution architecture, replacing the rWASM Runtime with the RISC-V Runtime](https://nicholas.feishu.cn/wiki/KFw9wBl7ViOaTdke0YTcEqPtnsh?from=from_copylink)
- [[Paper] Structured Finance of TradFi Inspires DeFi Protocol (Monoli Structured Derivatives Protocol)](https://nicholas.feishu.cn/wiki/DDwywlelQiqRfXko4F8cniY6nr9)
- [[Paper] From Multi-chain Integration to Unified Operations: The Omnichain Operationally Harmonized Infrastructure [draft]](https://nicholas.feishu.cn/wiki/ZWr0wJwxuib9r6kXGjEcDZTuncc?from=from_copylink)
- [[Paper] The MA End Game - Massive Adoption Capability Solutions](https://nicholas.feishu.cn/wiki/M9Cuw8PWVin7lhkx2MZcLkk4nAg?from=from_copylink)
- [Monoli Litepaper](https://nicholas.feishu.cn/wiki/In06wTQ4zi7zM1kQTFcc8cklnVb?from=from_copylink)
- [MEPs](https://nicholas.feishu.cn/wiki/V87Zwm8EWiWPSXkA7lHcaOQengf?from=from_copylink)
