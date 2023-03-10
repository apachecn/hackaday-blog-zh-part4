# 在一对经典的游戏礼物中摸索

> 原文：<https://hackaday.com/2020/01/07/poking-around-inside-a-pair-of-classic-gaming-gifts/>

复古游戏现在很流行，可能像数百万其他人一样，[wrongbaud]发现自己在假期拥有了几个仿经典的游戏设备。但是*不同于*大多数人，他们现在使用这些设备来回放他们年轻时的游戏，[他决定试着玩他的新玩具，看看它们是如何工作的](https://wrongbaud.github.io/Holiday-Teardown/)。

第一个被拆开的是一款手持游戏《俄勒冈小径》( Oregon Trail )( T1 ),黑客读者可能会想起《T2 》( new York)第一次发布《T3》时的一次拆解。他的工作就在我们拆机的地方继续，把游戏的两个 EEPROM 芯片取出来，然后把里面的内容倒掉。正如所料，[wrongbaud]发现 I2C 连接的芯片包含游戏保存信息，SPI 闪存芯片存储实际的游戏文件。

[![](img/4a5c2d59ed9008fd1283a88b0152210f.png)](https://hackaday.com/wp-content/uploads/2020/01/retrogifts_detail.jpg) 接下来是 Bandai Namco 的 HDMI“棒”,允许用户玩一些 NES 游戏。这里[wrongbaud]再次解放了闪存芯片，并将其转储以供检查，这一次使用了他自己创建的 ESP32 工具。在固件映像中，他能够在`binwalk`的帮助下识别几个元素，比如闪屏图形和文本字符串。

但也许最有趣的是，他发现`binwalk`能够自动提取 NES 光盘本身。在用 NES 模拟器验证了它们是标准的 rom 之后，他推论说，如果有人愿意的话，用不同的 rom 重新打包固件应该是可能的。

这两个黑客都是很好的例子，说明如何用低成本的硬件、开源工具和足够的耐心对设备的固件进行逆向工程。即使你没有兴趣摆弄*俄勒冈小道*或者用 *Mappy* ROM 替换 *Contra* ，这篇文章对任何想自己做固件分析的人来说都是一个无价的资源。

这也不是[wrongbaud]第一次侵入这些非常流行的复古游戏。就在上个月，我们用重新发布的版本*狂暴*和*真人快打*报道了他以前的一些事迹。