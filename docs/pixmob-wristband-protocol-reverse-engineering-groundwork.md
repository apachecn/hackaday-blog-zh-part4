# PixMob 腕带协议逆向工程基础

> 原文：<https://hackaday.com/2022/08/06/pixmob-wristband-protocol-reverse-engineering-groundwork/>

PixMob 腕带背后的想法很简单——在音乐会上，组织者将这些分发给音乐会观众，在演出期间，红外投影仪用于传输命令，因此它们都同步点亮。有时，参加者会被允许在活动结束后把这些手镯带回家，一些黑客已经尝试重新使用它们。

然而，该协议是专有的，我们还没有看到任何人在不拆开它们或重新刷新微控制器的情况下重复使用这些腕带。[Dani Weidman]告诉我们，他们如何与[Zach Resmer]一起为这些腕带的[逆向工程协议奠定了基础。](https://github.com/danielweidman/pixmob-ir-reverse-engineering)

我们的两个黑客从网上一个乐于助人的陌生人那里获得了一些记录，然后在他们的腕带上重放这些红外记录。其中大多数没有引起任何反应——据推测是配置包，但其中三个导致腕带以不同的颜色闪烁。他们将这些录音翻译成二进制数据包，Dani 经历了不同的可能组合，在这里和那里调整位，传输数据包，并查看哪些被接受为有效。最后，他们得到了大约 100 个有效的数据包，甚至弄清楚了一些协议特性，如彩色动画字节和运动灵敏度模式使能数据包。

GitHub 库提供了一些不错的文档，甚至还有一个视频，你可以在一个带红外发射器的 Arduino 上运行的示例代码，甚至还有一些你可以用 [Flipper Zero](https://hackaday.com/2021/07/24/how-the-flipper-zero-hacker-multitool-gets-made-and-tested/) 发送出去的数据包。如果你有兴趣了解更多关于这款设备的内部信息，[请查看我们在 2019 年推出的拆卸功能](https://hackaday.com/2019/11/26/pixmob-led-wristband-teardown-plus-ir-emitters-and-how-to-spot-them/)。