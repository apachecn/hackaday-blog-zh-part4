# 在任天堂游戏机上挖掘比特币

> 原文：<https://hackaday.com/2021/04/01/mining-bitcoin-on-the-nintendo-game-boy/>

开采加密货币是一项电力密集型业务，大型企业囤积 ASIC 设备和高端 GPU，以无休止地寻求主宰世界的金钱。[【stacksmashing】的比特币挖矿游戏男孩就是其中之一。](https://www.youtube.com/watch?v=4ckjr9x214c)(视频，下面嵌入。)

黑客攻击相对简单。Game Boy 通过 Raspberry Pi Pico 和电平转换器连接到 PC，以处理不同的电压电平。Game Boy 在 flash cart 上运行定制软件，该软件对来自 PC 的输入数据运行 SHA 哈希算法，并将结果报告给与比特币网络通信的 PC。

[stacksmashing]很好地解释了这个项目，涵盖了从游戏男孩的链接端口协议到比特币算法的细节。对于有技术经验的人来说，你需要知道的重建项目的一切都在那里。虽然 Game Boy 每秒只能处理 0.8 个哈希，比尖端硬件慢了数万亿倍，但该项目仍然很有趣，也很有教育意义，所以在下面的评论中引发热议之前，请考虑这一点。如果你真的对底层数学感兴趣，[你可以试着用纸和笔来计算比特币的哈希值](https://hackaday.com/2014/09/29/mining-bitcoins-with-pencil-and-paper/)。

 [https://www.youtube.com/embed/4ckjr9x214c?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/4ckjr9x214c?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



【感谢 Stephan 的提示！]