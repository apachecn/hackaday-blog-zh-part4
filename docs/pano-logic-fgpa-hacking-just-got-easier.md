# 帕诺逻辑 FGPA 黑客变得更加容易

> 原文：<https://hackaday.com/2019/04/19/pano-logic-fgpa-hacking-just-got-easier/>

当 Pano Logic 在 2012 年倒闭时，他们独特的基于 FPGA 的瘦客户端突然成为 IT 部门不想与之有任何关系的负担。新的和旧的设备充斥着二手市场，有一段时间你可以买到这些有趣的小玩意，价格不会比运费高多少。由于黑客社区的巨大兴趣，这些盒子的价格在易贝有所攀升，但它们仍然是让你接触 FPGA 黑客的一个很好的方式。

尤其是现在，Pano Logic 的狂热爱好者[【Skip Hansen】已经想出了如何在他们身上刷新新固件，而不必打开机箱](https://github.com/skiphansen/pano_progfpga)并打开 JTAG 或 SPI 编程器。对于经验丰富的硬件黑客来说，这似乎没什么大不了的，但是如果你是游戏新手，或者只是对软件方面更感兴趣，这个技巧会让事情变得容易得多。如果事情变糟，聘请外部程序员仍然是一个好主意，但如果你只是想展示一些演示，看看硬件能做什么，这将极大地提高生活质量。

[![](img/58028ca1017d6a290266ce10d2214b3c.png)](https://hackaday.com/wp-content/uploads/2019/04/panoupdate_detail.png) 即使你对摆弄一家已倒闭的湾区初创公司的孤立产品不感兴趣，这篇文章也是对实用软件逆向工程的一次迷人审视。事实证明，[Skip]并没有从头开始创建这个新的固件更新工具。他实际上从 Ghidra 的 Pano Logic 中打开了官方的 Linux 更新实用程序，并且能够计算出固件映像实际上在程序中的位置。然后，他用 C 语言编写了自己的工具，用用户提供的固件映像修补更新工具。

修补后，你需要做的就是遵循官方更新程序，Pano Logic 在休息后的 YouTube 视频中记录了这一过程。[Skip]提到他在摆弄的官方软件中没有找到任何明确的许可证信息，当然，随着公司的倒闭，无论如何也不太可能有人会来敲他的门。尽管如此，他说，Pano Logic updater 的下载仍然在那里的管道上浮动，供您查找，所以他没有分发任何人的代码，但他自己在这个项目中。

有许多黑客正在努力将 Pano Logic 瘦客户端转变为有用的通用 FPGA 平台，[例如[Tom Verbeure]，他令人难以置信的图形演示激发了[Skip]的灵感](https://hackaday.com/2018/12/07/racing-the-beam-on-a-thin-client-in-fpgas/)，让他在易贝开发了自己的设备。随着对 USB 和 SDRAM 的支持由[【张文婷】添加，同时让他的 FPGA GBA 仿真器在硬件上运行](https://hackaday.com/2019/03/23/game-boy-recreated-in-verilog/)，似乎从来没有一个更好的时间来乘坐 Pano Logic 列车。

 [https://www.youtube.com/embed/DPkF5EisGDQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/DPkF5EisGDQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

