# 将数千名《我的世界》玩家放在同一个服务器上

> 原文：<https://hackaday.com/2021/09/10/putting-thousands-of-minecraft-players-on-the-same-server/>

多年来，多线程一直是从机器中获取更多性能的常用技术。如今，一切都是关于水平扩展或向工作人员池中添加更多虚拟机。《我的世界》服务器在某些方面仍然停留在过去，因为它既不支持多线程，也不支持水平伸缩。[Jackson Roberts]决定改变这一切，通过黑掉《我的世界》来支持成千上万的玩家，而不是几十个。

因为服务器是单线程的，在一个服务器上有超过 100 个玩家会使它变慢。一些 mod 试图优化和加速现有的服务器，但[杰克逊]想要更多。早期的概念验证是将世界分割成独立的服务器，每个服务器拥有 64×64 个区块(区块是《我的世界》定义的 16×256×16 的世界体积)。当穿越边界时，玩家和僵尸等实体从一个服务器转移到另一个服务器。虽然可行，但演示还是有一些问题，比如如果一台服务器宕机，世界的部分地区将无法访问。边界也很不协调，因为你必须重新连接，而且看不到服务器外的玩家。

[杰克逊]没有分裂世界，而是采取了分裂玩家的方法，并为坚持和传播变化提供了一些支持。一个代理位于几个《我的世界》服务器的前面，每个服务器都连接到一个 WorldQL 服务器(一个基于 Postgres 的空间数据库)。每个服务器都向 WorldQL 服务器报告玩家的位置，并接收他们加载位置的更新。当服务器联机时，它会跟上存储在 WorldQL 中的更改并开始同步，从而允许服务器自动伸缩。仍然有一些核心游戏机制还没有为黄金时间做好准备，例如 NPC 和 Redstone，但迄今为止的进展是显著的。

《我的世界》插件的[代码已经在 GitHub](https://github.com/WorldQL/mammoth) 上发布，但更多代码将在未来发布。所以，如果你对更香草的东西感兴趣，为什么不惊叹于香草《我的世界》里面的[完全可玩的口袋妖怪红呢？](https://hackaday.com/2018/04/30/game-ception-pokemon-red-playable-inside-minecraft/)