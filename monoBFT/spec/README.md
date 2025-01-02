# MonoBFT Spec

MonoBFT provides Byzantine Fault Tolerant State Machine Replication using hash-linked batches of transactions(blocks).

每个区块都有唯一索引(height)，height在blockchain中是monotonic的，每个区块都有一组已知的加权validators进行验证。validator集合会改变，
只要集合总权重少于1/3 malicious or faulty，BFT就能保证区块链的安全性和有效性。

commit: 指来自当前validator集合总权重的2/3以上的signed messages，validators轮流提出区块并投票，一旦收到足够的votes，区块即被视为committed.
这些votes将被包含下一个区块中，作为前一个区块已被提交的证明(这些votes不能被包含在当前区块中，因为该区块已被创建)。

应用会返回块中每个交易的结果，还可以返回对验证集所作的更新，以及其最新状态的加密摘要(Merkle roots).

MonoBFT旨在实现对区块链最新状态的高效verification and authentication. 为此它在区块头中嵌入了相关信息，包括区块的内容，提交区块的验证集以及
应用返回结果。 只有在提交区块后才会执行区块。因此，应用结果只能包含在下一个程序块中。

交易结果和验证器集等信息永远不会直接包含在区块中，只有它们的Merkle roots才会包含在区块中。
因此，区块验证需要一个单独的数据结构来存储这些信息。我们称之为State。区块验证还需要访问前一个区块。

Data Structures
- Encoding and Digests
- Blockchain
- State

Consensus Protocol
- Consensus Algorithm
- Creating a proposal
- Time
- Light-Client

P2P and Network
- P2P Layer
- Peer Ex
- Block Sync
- Consensus
- Mempool
- Evidence

RPC
- RPC Spec

Utils
- API
- Log(write-ahead)

## Data Structures

### Blockchain


### Encoding
MonoBFT uses Proto3, for all data structures.


