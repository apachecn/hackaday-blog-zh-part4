# Pi Pico 为超频献出生命

> 原文：<https://hackaday.com/2022/08/25/pi-pico-gives-its-life-for-overclocking/>

一辆树莓派 Pico 能开多快？嗯，[显然答案是 1 GHz](https://www.raspberrypi.com/news/dont-try-this-at-home-overclocking-rp2040-to-1ghz/) 如果你冻结它，并给它两倍于正常情况下的电压。哦，有一点。几分钟后，芯片会自己炸。

这是[大卫]报告的结果，他用了一个珀耳帖冷却器和一个相当严重的过电压。dhrystone 的分数从大约 200 到超过 1100。当然，还有令人讨厌的早逝要担心，所以你可能不想在家尝试这个。

甚至在芯片被淘汰之前，还有其他问题需要解决。例如，一旦你的频率远远超过 250 MHz，Pico 的 SPI 闪存就跟不上了，所以你想运行的所有[软件都必须先放在 RAM 中](https://github.com/davidb990/rp2040_xoc)。您可能还想研究一下系统时钟参数。

老实说，我们喜欢超频电脑或其他任何东西。好消息是，如果你油炸一个匹克，它不会对你的钱包造成相当大的影响。这也是一种有趣的方式来学习更多关于处理器内部的知识。根据[David]的说法，冷却器将零件冷却到零下 40 摄氏度。我们想知道在液氮浴中会怎么样？

当然，你也可以[推一个普通的 Pi](https://hackaday.com/2020/11/11/adventures-in-overclocking-which-raspberry-pi-4-flavor-is-fastest/) 。如果你真的需要一个 1 GHz 超频的微控制器，也许[可以试试 Teensy](https://hackaday.com/2022/01/02/teensy-4-pushed-to-the-limit-with-1-ghz-overclock/) 。