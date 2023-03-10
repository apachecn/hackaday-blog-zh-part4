# 实际操作:BornHack 2020 徽章有 9×32 个由 CircuitPython 提供的闪烁

> 原文：<https://hackaday.com/2020/08/27/hands-on-bornhack-2020-badge-has-9x32-of-bling-fed-by-circuitpython/>

尽管疫情大范围取消，今年博恩哈克仍然发生了，他们甚至再次设法给所有与会者带来了电子徽章。如果你错过了，我已经发布了[关于黑客阵营本身的概述](https://hackaday.com/2020/08/24/running-a-successful-hacker-camp-in-a-pandemic-bornhack-2020/)。今天让我们一起来挖掘一下[2020 博恩哈克徽章](https://github.com/bornhack/badge2020)！

由 Thomas Flummer 设计并在丹麦制造，它采用 PCB 的形式，形状为大约 60 度的圆弧，其顶部的大部分被 9×32 的 SMD LEDs 阵列占据。在正面的其余部分有常见的 4 路按钮阵列和用于 SAO 连接器的空间，而在背面有一组 GPIO 垫和一对 AA 电池座用于电源。连接是通过 USB-C 和红外线，而且有用地还有一个电源开/关开关。

其硬件的核心是一个 [SAMD21G18A](https://www.microchip.com/wwwproducts/en/ATsamd21g18) ARM Cortex M0+微控制器，这可能不是最令人兴奋的芯片，但随着 LED 驱动器的出现，硬件变得更加有趣。一对 [IS31FL3731](http://www.issi.com/WW/pdf/31FL3731.pdf) 芯片(你可能从 Brian Benchoff 的机器人先生徽章上认出来)各自驱动一半的 Charliplexed LED 阵列。这些多功能芯片通过 I2C 接口提供自己的内部帧寄存器，免去了微控制器扫描 LED 矩阵的麻烦。这一选择既充分利用了该应用中相对较少的微控制器，又为软件选择开辟了道路。该徽章运行 Adafruit 的 CircuitPython，因此可以通过 USB 连接进行编程，就像任何其他 CircuitPython 板一样。为了测试这一点，我把我的 GNU/Linux 笔记本电脑放在一边，拿起一个不太通用的东西来测试它的易用性:Chromebook。

```

# configure I2C
i2c = busio.I2C(board.SCL, board.SDA)

# turn on LED drivers
sdb = DigitalInOut(board.SDB)
sdb.direction = Direction.OUTPUT
sdb.value = True

# set up the two LED drivers
display = adafruit_is31fl3731.Matrix(i2c, address=0x74)
display2 = adafruit_is31fl3731.Matrix(i2c, address=0x77)

text_to_show = "BornHack 2020 - make clean"

```

CircuitPython 设备作为磁盘驱动器安装，其中可以找到一个 Python 文件，可以用您选择的代码进行编辑。BornHack 徽章[附带显示 BornHack 横幅文本](https://github.com/bornhack/badge2020/blob/hardware/examples/startHere/code.py)的代码，该文本用作对其显示功能的快速介绍。很明显，文本滚动性能还有待提高，但这种微控制器并不是 CircuitPython 平台所支持的最强大的微控制器之一。Chromebook 很高兴能够编辑代码，尽管查看 Python 串行控制台需要潜入其 Linux 虚拟机。

BornHack badge 是一个极具吸引力的设计，通过使用流行的 CircuitPython 平台，并通过其适当大小的 LED 矩阵和可用的 GPIOs，实现了能够轻松编程的目标，并有机会在营地外用作通用显示/实验平台。它可能不是最强大的徽章，但它的工作做得很好。特别是，它实现了许多其他人错过的壮举，到达营地时已完全组装好，硬件和软件都正常工作。你可以在我们放在休息时间下方的营地的[托马斯徽章展示中看到更多信息。](https://www.youtube.com/watch?v=1t1gyQ_yyU8&t=328)

我们期待看到它对其他类似徽章的影响。与此同时，如果你有兴趣，你可以将其与我们去年审查的 2019 年博恩哈克徽章进行比较。

 [https://www.youtube.com/embed/1t1gyQ_yyU8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=328&wmode=transparent](https://www.youtube.com/embed/1t1gyQ_yyU8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=328&wmode=transparent)

