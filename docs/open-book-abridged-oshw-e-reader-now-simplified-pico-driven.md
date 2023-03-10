# 开卷节略:OSHW 电子阅读器现在简化，微微驱动

> 原文：<https://hackaday.com/2022/09/29/open-book-abridged-oshw-e-reader-now-simplified-pico-driven/>

如果你曾经寻找过开源电子阅读器，你肯定见过[乔伊·卡斯蒂略]的开卷阅读器，但你可能还没见过他围绕着树莓皮做的删节版。

[开放图书项目](https://hackaday.com/2019/10/31/building-an-open-hardware-ebook-reader/)将一个 4.2 英寸的 E-Ink 屏幕与我们都知道和喜爱的微处理器配对，建立了一个黑客友好的电子阅读器平台。两年前，这个项目[在我们的 Adafruit Feather 竞赛中获得了第一名](https://hackaday.com/2020/01/22/winners-of-the-take-flight-with-feather-contest/)——Feather footprint 使 Open Book 兼容多种 MCU，让黑客可以选择他们可破解的电子阅读器将在哪个 CPU 上运行。现在，是时候进行基于 RP2040 的重启了。

[![three PCBs being shown - one soldered-together version with a Pico on it, and two upopulated PCBs, showing front and back, on the populated PCB, you can see the Raspberry Pi Pico and other components soldered on. On the unpopulated PCBs, you can see there's a lot of text helping you understand and assemble this e-reader.](img/c93466afed5d72c63dd9c460d7b70b71.png)](https://hackaday.com/wp-content/uploads/2022/09/hadimg_openbook_pico_pic2.jpeg) 该项目旨在让您在采购零件和 PCB 后自行组装。为了在这个过程中帮助你，PCB 本身就像一本书的一页——在丝网印刷上，有对每个组件用途的解释，以及对你进行黑客攻击有用的信息，向即将手持烙铁投入组装的黑客传达硬件背景故事。这个硬件还配有简单但功能强大的软件——而且，作为完全开源的设备，任何缺失的功能都可以添加进来。

Joey 为我们录制了一个 30 分钟的 Pi Pico 版本的视频，组装和测试新订购的主板，然后展示软件成功启动和运行。基于 Pi Pico 的版本已经大大简化，与以前的版本相比，许多自组装方面都有所改进——整个过程真的不到半小时，而且他还用一个非常基本的烙铁就完成了！

如果随着开发的进行，你在寻找这个版本的更新，[在 Twitter](https://twitter.com/josecastillo/) 上关注【Joey】是你最好的选择。他让我们周围的设备变得更加自由，然后与我们所有人分享秘方，对此他并不陌生！在 2021 年的 Remoticon 期间，他展示了卡西欧 F-91W 手表的嵌入式替代主板，并告诉我们[所有关于逆向工程其无控制器部分液晶显示器](https://hackaday.com/2022/02/24/remoticon-2021-joey-castillo-teaches-old-lcds-new-tricks/)——值得任何想让这些液晶显示器屈从于他们意愿的黑客一听。

> 更新:这再好不过了。仅用 30 分钟就完成了组装和全部功能，包括第一次启动时语言芯片的自动闪烁(总共用了 60 秒)。链接全视频！[https://t.co/J9vXF2HYwA](https://t.co/J9vXF2HYwA)pic.twitter.com/z9TsVPcBixT2
> 
> —@ joeycastillo @ mastodon . social(@ Jose Castillo)[2022 年 9 月 18 日](https://twitter.com/josecastillo/status/1571350075208790019?ref_src=twsrc%5Etfw)