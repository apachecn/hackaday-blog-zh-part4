# 另一个 PC 电源项目

> 原文：<https://hackaday.com/2020/03/24/another-pc-power-supply-project/>

规模经济是一件美妙的事情，以开关电源为例。在个人电脑出现之前，一个像样的多电压、大电流电源会相当昂贵。但是个人电脑意味着廉价的供应，有时甚至是免费的，就像你在垃圾箱里找到的旧个人电脑一样。[OneMarcFifty]决定为 PC 供应商制作一个漂亮的设置，包括一个非常漂亮的彩色显示屏，上面有条形图和其他精美的东西。你可以在下面的视频中看到电源的运行。

显示屏是由 Arduino Nano 驱动的漂亮的 TFT。该项目使用 ACS712 电流传感器模块，这是一种很好的霍尔效应器件，可产生线性电流输出，电压隔离超过 2 KV。

有三个电流传感器，每个输出一个。与许多类似的项目相比，真正令人印象深刻的是非常好的图形输出。GitHub 拥有所有的软件和 PCB 布局。当然，您必须使外壳适应您的特定电源，但安排外壳应该很容易。

只有几个按钮，用户界面有点笨拙，但不比许多其他项目更笨拙。实际上，您只需使用按钮来更改条形图的速度、比例和分辨率。输出电压是固定的，没有电流限制。

另一个答案是找到一个更高电压的电源，并将其与一个便宜的电源模块匹配。我们还看到[非 PC 电源放在 PC 机箱里](https://hackaday.com/2017/10/14/not-your-typical-atx-bench-psu/)。

 [https://www.youtube.com/embed/1I17_Nu-uhY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/1I17_Nu-uhY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

