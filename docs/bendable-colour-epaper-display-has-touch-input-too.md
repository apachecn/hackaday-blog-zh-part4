# 可弯曲的彩色电子纸显示屏也有触摸输入

> 原文：<https://hackaday.com/2021/10/12/bendable-colour-epaper-display-has-touch-input-too/>

德累斯顿技术大学的互动媒体实验室一直忙于研究可穿戴电子设备的用户界面，并提出了一个很好的项目，我们任何人都可以复制，以创建自己的可穿戴彩色电子纸显示设备。他们甚至还想出了一个添加触摸输入的简洁方法。通过将三个[线性电阻触摸条](https://www.spectrasymbol.com/product/thinpot/)(实际上是触摸电位计)粘贴到背板上，并将后者直接放置在塑料逻辑 Legio 2.1”柔性[电泳显示器(EPD)](https://en.wikipedia.org/wiki/Electronic_paper) 的后面，创建了一个基本的触摸界面。它看起来确实需要施加相当大的力才能在触摸条上被检测到，但它应该能够承受。

硬件的其余部分是标准 fayre，使用现成的板来驱动 EPD，并使用 Adafruit Feather nRF52840 检测板来实现应用和蓝牙功能。外壳是 3D 打印的(自然),一切都可以用我们身边的物品来建造。下面的视频展示了一些可能的应用，包括有趣地将显示屏用作另一种可穿戴设备的表带的一部分。这也是一份关于在智能手表中增加互动显示屏的报告。毕竟，[你不能有太多的显示器](https://www.reddit.com/r/pcmasterrace/comments/mimr89/can_you_ever_have_too_many_monitors/)。

在民政总署的档案中可以找到许多可穿戴项目，包括这个[可疑的可穿戴范围](https://hackaday.com/2021/09/03/wearable-scope-lets-your-fingers-do-the-probing/)，一种将有机发光二极管纤维编织成服装的[方法](https://hackaday.com/2018/01/21/weaving-with-light-an-oled-fibre-fabric-display/)。最后，对于可穿戴 DIY 技术的一个很好的介绍，你可以做得比 Sophy Wong 的这个[超级演讲更糟。](https://hackaday.com/2019/11/27/supercon-talk-sophy-wong-is-designing-the-future-of-wearable-technology/)

 [https://www.youtube.com/embed/Pmrj-5yKTBg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Pmrj-5yKTBg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

