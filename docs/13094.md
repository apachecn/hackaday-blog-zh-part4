# 黑客向 MemoryStick 挑战并获胜

> 原文：<https://hackaday.com/2022/03/20/hacker-challenges-memorystick-to-a-fight-and-wins/>

当一个熟练的黑客对一个专有格式进行逆向工程，并与每个人分享其本质时，这是非常令人惊讶的。今天，我们得到了这样一篇关于记忆棒的报道。这是那些专有格式之一，索尼设备的主要产品，这些类似 SD 卡的存储设备显然是为了帮助充实索尼的口袋，我们可以从严格的锁定和虚高的价格中看出这一点。因此，这种格式对于黑客来说一直是难以接近的。没有更多的-【德米特里·格林伯格】在这里与[详细分析了记忆棒协议和内部结构。](https://dmitry.gr/?r=05.Projects&proj=31.%20Memory%20Stick)

如果你曾经想阅读一个设计不太合理的协议，从物理层的怪癖到 MemoryStick 和 MemoryStick Pro 之间令人费解的巨大差异，这将是所有黑客的娱乐读物。Dmitry 不仅描述了设计的糟糕部分，然而，尽管这种咆哮读起来很有趣，但页面的大部分内容都是寄存器摘要、结构描述和见解，以及我们从未得到的关于 MemoryStick 的内容。

有一句话被用来链接到[Dmitry]的一个相关项目，这是一个独立的 rabbithole 他为 PalmOS 提供了[二进制补丁 MemoryStick 驱动程序，为一些索尼 Clie 手持设备添加了 MemoryStick Pro 支持。鉴于上述非专业和专业标准之间的差异，这是一个比该网站的一些读者更老的设备的不朽事业，我们不禁留下深刻印象。](https://old.reddit.com/r/Palm/comments/ta27ev/announce_powermspro_add_memory_stick_pro_support/)

作为结束语，[Dmitry]与我们分享了 STM32 的一些内存棒位碰撞示例。任何曾经想接近 MemoryStick 的人，无论是为了制造转换器适配器以恢复旧技术，数据恢复或保存目的，还是仅仅出于黑客的好奇心，现在都可以在他们的努力中感到不那么孤独了。

我们很高兴在记忆棒方面看到如此伟大的黑客行为——这是非常需要的，以至于我们唯一提到记忆棒的文章是关于完全避免使用记忆棒插槽的。[Dmitry]正是这种逆向工程工作的合适人选，我们一直在跟踪的[丰富的逆向工程历史——他最近对](https://hackaday.com/blog/?s=Dmitry+Grinberg)[廉价 E-Ink 设备中一个不知名的微控制器](https://hackaday.com/2021/05/15/reverse-engineering-an-unknown-microcontroller-in-e-ink-displays/)的逆向工程之旅值得一看。