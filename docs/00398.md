# 倒带实况广播

> 原文：<https://hackaday.com/2018/08/20/rewinding-live-radio/>

尽管在广播技术的历史上，它现在是一个被遗忘的事后想法，但我们经常忘记 TiVo 有多么创新。这个机顶盒所做的只是将一个硬盘连接到一个有线电视盒，但它的功能令人难以置信:你可以暂停直播电视。你可以录制节目。你可以倒回电视。这是一种不可思议的能力，以前没有人见过。当然，在亚马逊、网飞和 YouTube 之间，没有人再看电视了，所有这些平台都有暂停按钮，但是 TiVO 棒极了。

还有一点广播仍然存在。收音机。对于他的 Hackaday 奖参赛作品，[MagicWolfi]正在[将机顶盒带到电台](https://hackaday.io/project/112183-rrb-the-radio-rewind-button)。他发明了收音机倒带按钮，它的功能和你想象的一模一样:可以把直播的收音机倒带几分钟。

要在电视或收音机上设置暂停或倒带按钮，唯一真正需要的是一堆内存。TiVO 是用硬盘做的，而[MagicWolfi]是用 256 MB 的 SDRAM 做的。这意味着他需要访问大量 RAM，为此他转向 Digilent ARTY S7 板。是的，这是一个 FPGA，但实际上是一个相当简单的问题解决方案。

电路的其余部分是一个 FM 接收器芯片和一个 Arduino 形子板上的 I2S 音频编解码器。这个项目的主控制器是一个红色的大按钮，可以简单地将音频流倒回几分钟。很难说[MagicWolfi]能倒带音频流多长时间，但 256 MB 在音频世界里是一吨。

The [HackadayPrize2018](https://hackaday.io/prize) is Sponsored by: [![Microchip](img/20eb9d92b47da4c15177567c02a65727.png)](https://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey)  [![Supplyframe](img/2d012d9fc9c7873688699aeadb4742d2.png)](https://supplyframe.com/)