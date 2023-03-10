# 在 Cortex M0+上 DIY 40FPS 16bpp 平台

> 原文：<https://hackaday.com/2019/09/02/diy-40fps-16bpp-platformer-on-a-cortex-m0/>

当然，你可以在树莓派上玩一堆复古游戏，但如果你真的是铁杆玩家，你可以建立自己的复古主机，并为它编写自己的游戏。[Nicola Wrachien]进入今年 Hackaday 奖的是他的 DIY Cortex M0+游戏机和他编写的测试硬件的平台游戏。

[Nicola]正在使用的电路板是 uChip，一种基于 ATSAMD21(运行 Arduino Zero 的同一芯片)的小型 DIP 电路板。再加上 160×128 的 TFT LCD 屏幕，构成了硬件的主体。一个载板包含这两个器件以及几个按钮和一个运算放大器。

ATSAMD21 芯片有不错的硬件 DMA，[Nicola]用它来获得所需的帧速率。由于 DMA 硬件和 CPU 可以同时工作，当 DMA 处理一个图形块时，CPU 处理下一个块。使用这个系统，[Nicola]能够获得比最初设计更好的帧速率。请看一下[Nicola]的网页，了解关于所用算法的更多细节。

为了在[Nicola]用来展示控制台的平台上创建一个关卡，[Nicola]用 Java 创建了一个成熟的关卡编辑器。使用编辑器，您可以放置图块和精灵并设置它们的行为。然后，地图可以以优化的格式导出，以便加载到硬件和游戏中。

休息之后是一段展示比赛的视频。网站上不缺少很棒的 DIY 游戏机——看看这个令人印象深刻的[矢量游戏机](https://hackaday.com/2018/12/26/delicious-vector-game-console-runs-pac-man-tetris-mario-and-then-some/)，或者如果 RetroPie 更适合你，看看这个 [DIY 塞尔达播放设备](https://hackaday.com/2017/10/20/diy-nintendo-switch-may-be-better-than-real-thing/)。

 [https://www.youtube.com/embed/-dM5cK1SgUk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/-dM5cK1SgUk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



The [HackadayPrize2019](https://prize.supplyframe.com) is Sponsored by: [![Supplyframe](img/79a7db035b8a2b6c2b7b0895c45b7de8.png)](https://supplyframe.com/)  [![Digi-Key](img/ba094a14c430ab81591a2abdc54a5363.png)](https://hackaday.io/digikey)  [![Microchip](img/5023ef0b7ff1aee311cba9b54a3ac9fe.png)](https://hackaday.io/microchip)