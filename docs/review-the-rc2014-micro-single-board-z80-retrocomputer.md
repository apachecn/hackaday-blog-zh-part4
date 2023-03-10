# 回顾:RC2014 微型单板 Z80 逆向计算机

> 原文：<https://hackaday.com/2019/10/02/review-the-rc2014-micro-single-board-z80-retrocomputer/>

8 月底，我去了 Hebden Bridge，在 2019 年的 Osh camp 上做了一次演讲，这是一个在约克郡山谷度过的有趣的周末。这次活动给每位参加者一个由赞助商提供的电子工具包，而不是徽章，今年的这个特别有趣。 [RC2014 Micro](https://rc2014.co.uk/modules/rc2014-micro/) 是基于 RC2014 Z80 的 retrocomputer 的最新迭代，它是一台单板计算机，将 RC2014 精简到最低限度。花一个晚上的时间在黑客空间组装它，看看吧！

## 这是一个 SBC，但不是你所知道的！

[![The kit contents](img/7eeedfc6fb890bed3c1b92fb2e7004b1.png)](https://hackaday.com/wp-content/uploads/2019/09/rc2-014-micro-kit-contents.jpg)

The kit contents

该套件采用非常紧凑的热封防静电包装，打开后发现其中包含 PCB、一块载有集成电路的泡沫、几个无源器件以及非常简单的入门和组装指南。从芯片数量来看，设计的简单性显而易见，有 Z80 本身、6850 UART、27C512 ROM、62256 RAM、用于时钟产生的 74HCT04 和用于地址解码的 74HCT32。快速入门已经足够了，但是还有一组更全面的在线说明 (PDF)。

[![I added chip sockets and jumpers to my kit.](img/472f12a98d8d114773e4ad0b9efa2a3e.png)](https://hackaday.com/wp-content/uploads/2019/09/rc2-014-micro-kit-less-chips.jpg)

I added chip sockets and jumpers to my kit.

组装通孔套件几乎没有挑战性，尽管这是 DIP 集成电路通孔套件的最大可能密度。与大多数通孔项目一样，你选择的顺序是一切:首先是电阻，然后是电容，复位按钮和晶体，然后是集成电路。

我总是有点羞于将 IC 直接焊接到电路板上，所以我用插座和跳线补充了我的工具包。跳线用于为 Grant Searle 的 [ROM 基本分布](http://searle.hostei.com/grant/z80/SimpleZ80.html#RomBasic)或 Steve Cousins 的 [SCM 1.0](https://smallcomputercentral.wordpress.com/small-computer-monitor/small-computer-monitor-v1-0/) 机器码监视器选择 FTDI 电源和 ROM 地址，套件说明建议用截止电阻线硬接线。扩展总线没有一排引脚，因为该套件没有背板，背板是较大的 RC2014 套件的一个功能，但它有一组用于 FTDI 串行电缆的直角引脚。

## 你的 Arduino 上没有开发环境！

![](img/18d6c697acc6aa2d522841409a95ffa7.png)

组装完我的 RC2014 Mini 并对它进行了目视检查后，是时候给它通电，看看它是否工作了。安装 FTDI 电源的跳线时，我连接了串行电缆，并将其插入 USB 端口。

一个非常棒的地方是，Micro 在 PCB 的背面有串行电缆线的颜色，这样就不用担心弄反了。从 bash 提示符快速得到一个串行终端，点击 reset 按钮，我得到了一个基本的解释器。我的 RC2014 Micro 第一次工作，我可以直接给它发出基本命令，如`PRINT "Hello World!"`，并获得预期的输出。

[![The SCM ROM monitor.](img/92992cd9bbf5dbc224d901b999098274.png)](https://hackaday.com/wp-content/uploads/2019/09/rc2-014-micro-scm.jpg)

The SCM ROM monitor.

因此，我建造了一台小型 Z80 单板计算机，与完全模块化版本的 RC2014 相比，工作量要少得多。它的创造者斯潘塞告诉我，Micro 最初被设计为廉价的 RC2014，作为研讨会和类似活动的多种选择，与他的 RC2014 迷你板非常相似，但没有提供 Pi 零点端子和其他一些组件。它缺乏更全面的操作系统(如 CP/M)所需的额外硬件，所以我只能使用 2019 年可用的部件来构建尽可能最小的 8 位计算机。我的问题是:我能用它做什么？

## 所以。8 位单板机能做什么？

我的第一台电脑是 Sinclair ZX81，它怎么可能比得上这个在会议上免费赠送的小套件呢？尽管 Sinclair 包括黑白电视显示接口、磁带备份接口和键盘，但核心计算能力在能力上与这款 RC2014 Micro 没有太大区别——毕竟，它是相同的处理器芯片。正是这个平台让年轻得多的我接触到了计算，我立刻如饥似渴地阅读了 Sinclair BASIC，然后继续在上面编写机器代码。由于简单的基本编程，它成为了一个通用的计算和计算便签簿，用于重复的家庭作业，并且通过我的 [Maplin 8255 I/O 端口卡](https://hackaday.com/2016/11/21/sinclair-io-board-completed-over-30-years-later/)，我能够以现代技术意识的孩子可能使用 Arduino 的方式使用它。

RC2014 Micro 作为一个基本的机器代码学习平台，可以很好地满足所有这些功能，在这个平台上，您可以以大多数现代计算机上无法实现的方式接触到硬件，尽管 Arduino 代表了硬件接口的一个更明智的选择，但如果您希望尝试，也可以为 Micro 的扩展总线提供 RC2014 背板和 I/O 板。我会用它来做这些事情吗？它肯定比它的全尺寸兄弟要方便得多，所以我很可能会用一点 Z80 代码来弄脏我的手。35 年里你能忘记的事情多得令人震惊！

RC2014 Micro [可以从斯潘塞的 Tindie 商店](https://www.tindie.com/products/semachthemonkey/rc2014-micro-single-board-z80-computer-kit/)购买，对于那些车间客户来说有很大的批量折扣。如果您想要完整的 retrocomputer 体验，这是一个很好的选择，因为它提供了尽可能简单的 Z80 硬件和软件方式。简单性的代价是没有非易失性存储和缺乏运行 CP/M 的硬件，但必须记住，它是 RC2014 系列的底部。为了比较，你可以阅读[我们对最初 RC2014](https://hackaday.com/2016/09/08/review-the-rc2014-z80-computer/) 的评论，我们会说微型的主要优势是它相对容易建造。