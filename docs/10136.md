# Pi Pico 项目完美播放 Pong

> 原文：<https://hackaday.com/2021/05/13/pi-pico-project-plays-pong-perfectly/>

即使技术不断进步，我们发现自己一次又一次地回归经典。Pong 很可能是经典游戏，而 Raspberry Pi Pico 是最新的微控制器之一。所以[Nick Bild]在他的 [Pico Pong 项目中熟练地将它们结合起来，该项目包括手势控制和自定义 VGA 输出](https://github.com/nickbild/pico_pong)。

滚动自己的 VGA 信号不是一件简单的事，这个项目充分利用了 Pico 的特性来完成它。显示数据缓存在内存中，而[可编程 I/O (PIO)](https://hackaday.com/2021/01/29/a-look-at-the-interesting-rp2040-peripheral-those-pios/) 程序通过直接内存访问(DMA)直接从缓存中读取，并直接写入显示器。这允许纳秒精度，同时让 CPU 自由处理输入和运行游戏。即使卸载了显示工作，ARM 处理器也必须以 258 MHz 的频率大规模超频，远远超过其[的 133 MHz 规格](https://datasheets.raspberrypi.org/pico/pico-product-brief.pdf)，才能让事情顺利运行。[Nick]仍然发现自己受限于 640×350 的分辨率和偶然发现的复古精确的单色配色方案。

手势控制来自一对连接到 GPIO 的红外光束。红外发光二极管向上照射到反射器上，光线向下反射到探测器上。阻挡其中一个光束会导致你的桨上下移动，这在视频中看起来很有反应(嵌入在下面)。

我们以前见过[尼克]玩 Pong，尽管那时候它是基于古老的 6502 的手持游戏。就在最近，我们写了关于[树莓派 Pico 驱动另一款经典游戏:贪吃蛇](https://hackaday.com/2021/05/11/play-your-favorite-nokia-game-on-the-raspberry-pi-pico/)。

 [https://www.youtube.com/embed/2wJyQ80iF74?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/2wJyQ80iF74?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

