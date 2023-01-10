# 使用 FPGAs 加速 IOTA 工作验证

> 原文：<https://hackaday.com/2019/11/16/speeding-up-iota-proof-of-work-using-fpgas/>

区块链自 20 世纪 90 年代初就作为一个概念存在，但在 IOTA 开发 Tangle 之前，为物联网交易保留分布式账本并没有得到广泛实施。这家区块链公司最初是作为一家硬件初创公司成立的，后来转向了物联网的交易结算。Tangle，他们基于有向无环图(DAG)的分布式分类帐架构，就像一个“没有块和链的区块链”。

顾名思义，Tangle 是一个事务网，它引用了过去的两个事务和其他事务的一个子部分。所有积极的参与者都参与交易的审批，而不是由矿商和股东负责达成整体共识。交易过程要求客户用他们的私钥签名，选择两个随机的未确认交易作为参考，并执行工作证明。

正如您所料，工作证明的难度非常高。该过程类似于在比特币挖掘中寻找随机数，尽管由于交易在低功率节点上运行，难度被设置为较低的阈值。尽管如此，由于 IOTA 事务通常发生在小型嵌入式平台上，这可能需要几分钟来完成，考虑到这些仅仅是事务，这是相对较长的时间。

因为 Curl-P81 散列应该并行计算，所以它们不能在通用 CPU 上有效计算。IOTA 参考实现(IRI) [PearlDiver](https://github.com/iotaledger/PearlDiver) 的 [PiDiver 1.3](https://gitlab.com/microengineer18/pidiver1.3) 、【Thomas Pototschnig】的[端口](https://gitlab.com/microengineer18/pidiver1.3/wikis/home)，执行随机数搜索。因为它运行在 FPGAs 上，所以与 Raspberry Pi 相比，它能够将工作验证的速度提高 140 倍以上。 [FPGA](https://gitlab.com/microengineer18/pidiver1.3/wikis/hardware) 能够在单个时钟周期内计算一轮哈希，在 85 个周期内计算一次完整的哈希(以及测试有效随机数)。一次可以计算七个并行哈希，在 188MHz 的频率下给出 15.8 兆哈希/秒。与 Raspberry Pi 上的 90 毫秒相比，FPGA 上的工作验证需要大约 300 毫秒，因此这是速度上的显著提高。

因为这个项目是开源的，所以 IRI 可以使用这个核心来创建他们 PearlDiver 的修改版本。该板可以用作 Raspberry Pi 帽子，尽管它也可以通过 USB 连接，在没有 Pi 的情况下工作。

虽然这并没有解决在个人物联网设备上使用 IOTA 的安全问题，但这无疑是对他们工作证明过程速度的一个重大改进，而且软件加速令人难以置信地满意。

 [https://www.youtube.com/embed/kAGCbu1CgoM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/kAGCbu1CgoM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

