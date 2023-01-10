# MIDI 控制的霓虹灯

> 原文：<https://hackaday.com/2018/10/11/midi-controlled-neon/>

制作霓虹灯标志的人是一个充满活力的社区，有玻璃弯曲和高压电子设备。然而，有必要对这些霓虹灯进行排序，而 MIDI 似乎是实现这一点的方法。这就是[david]为了进入 Hackaday 奖正在做的事情，结果看起来已经很不错了。

这个项目的想法是将 MIDI 数据传输到控制器，控制器相应地激活氖管。至于为什么[david]选择 MIDI 而不是 DMX512 或其他协议，这里的目的是为了与*音乐*同步，如果你已经有一台发送 MIDI 的鼓机，你还不如直接接入它。

该建筑使用 Arduino Leonardo 和 Olimex 生产的 MIDI 盾。这个防护罩连接到[一个霓虹灯电源](http://www.t2-neonpower.com/PRODUCTS/NEON_SUPPLIES/5k30_120V_files/5k30_120V.html)上，它有控制电路，可以快速方便地打开和关闭霓虹灯。最终结果是一台笔记本电脑(带有 DJ 软件的其余部分)向 Akai 鼓机发送 MIDI 时钟信号。这台鼓机输出 MIDI 音符到盾牌，目前设置为控制三个霓虹灯变压器。

结果看起来很棒，闪烁的头骨与哔哔声和滴答声同步。当然，这可以扩展到更多的 MIDI 同步霓虹灯。休息之后，您可以查看几个构建视频。

 [https://www.youtube.com/embed/OF9CwCswp7Y?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/OF9CwCswp7Y?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/DhQSyJzafW4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/DhQSyJzafW4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



The [HackadayPrize2018](https://hackaday.io/prize) is Sponsored by: [![Microchip](img/20eb9d92b47da4c15177567c02a65727.png)](https://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey)  [![Supplyframe](img/2d012d9fc9c7873688699aeadb4742d2.png)](https://supplyframe.com/)