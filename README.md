# Monoli-L1
> disappointing to see how far behind defi was compared to its centralized counterparts. @nicholaslico

Monoli Layer1(以下简称L1) 的主要目的是为高性能衍生品交易所而构建的，它受到[perps](https://github.com/0xnicholas/perps) DEX(orderbook model)的需求推动，这使得Monoli有别于通用L1设计，为DEX做了关键优化。

## Motivation
> [设计文档](./docs/design/README.md)

**成为价格发现的来源**

> Orderbooks is too useful.

|||
|---|---|
|AMM| front-running and MEV attacks|
|RFQ|RFQ solution it is too opaque, and the asymmetry between makers and takers leads to centralization|
|Orderbooks|Order books are the only tested and sustainable solution at scale, as they let liquidity providers precisely control their risk, leading to capital efficiency and tighter spreads, and it can be decentralized.|

**高性能专用L1**

链下订单薄的validators(如dydx)实际上可能会拥有过多的集中权力，不可行；需要能够完全支持链上订单薄的区块链，但没有一条能满足性能目标的最低延迟和TPS要求。

L1需要适当的去中心化，通过CometBFT共识实现，保证所有验证者交易顺序一致，状态包括所有交易状态，不依赖链下订单薄。L1的状态转化逻辑借鉴了高性能NFT系统中使用的模式和抽象。L1专注于运行高性能EX，不支持通用智能合约。

(PoS)L1 由PoS机制保护，L1 的staking和slashing机制与其他 Cosmos 链的工作方式类似。

(Fees)L1的费用将比通用L1每笔操作的gas值低几个数量级，这是因为L1仅运行优化的`exchange state machine`而不是通用的智能合约。而交易费则接近于0。

(Latency)共识使用尽可能减少端到端延迟的CometBFT调整版本，该延迟以发送请求到接收其提交的响应之间的持续时间来衡量。此性能允许用户以最小的更改从中心化加密货币场所移植交易策略，并通过用户界面为散户用户提供即时反馈。

(Throughput)L1计划支持每秒20,000次操作，包括orders/cancels和liquidations.

## Overveiw
### Monoli EVM
> 基于[reth](https://reth.rs/)改写


### MonoBFT
> 由[CometBFT](https://github.com/cometbft/cometbft) Go改编为Rust版本，同时参考了[tendermint-rs](https://github.com/informalsystems/tendermint-rs)


### Orderbook
L1 state包含每个asset的orderbook


### Oracle

### Bridge
> run with an EVM bridge


## _Reference
- [Reth](https://github.com/paradigmxyz/reth)
- [CometBFT](https://github.com/cometbft/cometbft)