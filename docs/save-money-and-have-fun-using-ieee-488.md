# 使用 IEEE-488 省钱又开心

> 原文：<https://hackaday.com/2022/01/31/save-money-and-have-fun-using-ieee-488/>

几个月前，我和一个同事在讨论 GPIB 设备的控制。仅仅基于我的直觉和最简短的研究，我告诉他昂贵和专有的 GPIB 控制器解决方案很容易被开源工具和 Linux 所取代。在接下来的几周里，由于沮丧，我几次几乎放弃了我的立场。凭借一些毅力，把问题分成小块，并在网上大量搜索以学习他人的经验，我的计划最终成功了。我没有完全放弃我最初的立场，我后退了几步，增加了一些限定条件。

## 什么是 GPIB？

[![](img/d944136f775666d88f66e81b78877caa.png)](https://hackaday.com/wp-content/uploads/2022/01/hpib-early-example-diagram.png)

Example of HP-IB block diagram from the 1970s, from hp9845.net

回到 20 世纪 60 年代，如果测试设备是互连的，也没有任何公认的方法。到了 60 年代后期，这种情况因卡笼控制器系统而有所改善。它们有许多接口卡，每个仪器一个，在底板上提供一个公共接口。虽然这种方法是可行的，但惠普工程师意识到，他们可以显著改进这一概念，在仪器中包括这些“桥接电路板”，并用无源电缆取代卡盒背板。由此开始了后来成为惠普接口总线(HP-IB)的发展。惠普杂志【1972 年 10 月刊[以两篇主要文章介绍了 HP-IB:一篇*电子仪器实用接口系统*和*可编程仪器的通用数字接口:系统的演变*。](https://www.hpl.hp.com/hpjournal/pdfs/IssuePDFs/1972-10.pdf)

> 为了克服在互连仪器和数字设备中遇到的许多问题，已经定义了一种新的接口系统。该系统为系统互连提供了新的便利和灵活性。从经济角度来看，实验室和大型系统中使用的互连仪器现在变得可行。

惠普随后向 IEC 提交了 HP-IB，并成为国际标准。几年后，它成为我们今天所知的 [GPIB(通用接口总线)或 IEEE-488](https://en.wikipedia.org/wiki/IEEE-488) ，于 1975 年首次正式化。

## 手头的任务

为什么我需要使用 50 年前的通信接口？由于 GPIB 是这么多年来事实上的接口，许多二手测试设备可以在二手市场上以非常合理的价格找到，比现代的同类设备便宜得多。此外，越多的测试设备被放在实验室的工作台上，就意味着越少的测试设备被放入回收系统或垃圾填埋场。但我不需要这些辩解——这种旧装备的享受和怀旧感对我来说已经是足够的理由了。

[![](img/d1889aaaaec1959d06a1e83305535976.png)](https://hackaday.com/wp-content/uploads/2022/01/gpib-digipot-diagram-yellow.jpg)

Diagram of a typical digipot, the TPL0501 (from Digikey Article Library)

但是，为什么首先要通过计算机接口与测试设备对话呢？在我的项目中，我需要校准 digipot 在每个可编程游标位置的电阻。这样我就可以根据测量数据创建一个校准算法，您可以输入所需的欧姆值并获得相应的游标寄存器值。当然，我可以手动进行这些测量，但对于 256 个游标位置，这将变得非常繁琐。如果您想了解有关数字电位计的更多信息，请查看 Digikey 库中的这篇[文章，了解数字电位计的基础知识以及如何使用它们。](https://www.digikey.com/en/articles/the-fundamentals-of-digital-potentiometers)

[![](img/4f1823bb9203afbe0163fccc7100c42c.png)](https://hackaday.com/wp-content/uploads/2022/01/gpib-keithley-195a.jpg)

Used Keithley 195A Bench DMM from c.1982

我评分一个二手吉时利 195A 数字万用表从 80 年代初。这是一个 5-1/2 数字台式数字万用表，我的设备安装了 1950 型交流/安培选项。

## 行动（或活动、袭击）计划

在四处搜索的时候，我找到了[Thomas Klima]的一篇[论文(德语)](http://elektronomikon.org//Bakkarbeit%20RasPi-GPIB%20Thomas%20Klima.pdf)关于在 Raspberry Pi 或 Pi Zero 上使用易于构建的 GPIB 接口屏蔽与实验室仪器进行通信。他的项目是开源的，并在 GitHub 页面(这里是 Raspberry Pi 版本，这里是 Pi Zero 版本)和他的 [elektronomikon 网站](http://elektronomikon.org)上有很好的文档。

这是一个简单的电路，支持我的直觉断言，GPIB 没有那么复杂，你可能用 8051 来实现它。我组装了这个项目，我已经准备好了一个树莓派 Zero-W。

 [![GPIB Interface Module Installed on Rear of DMM](img/5e1cf2abd4aef40d5078cb0a8c28ccc0.png "gpib-keithley-with-gpib-interface")](https://i0.wp.com/hackaday.com/wp-content/uploads/2022/01/gpib-keithley-with-gpib-interface.jpg?ssl=1) GPIB Interface Module Installed on Rear of DMM [![GPIB + Raspberry Pi Zero Interface Module](img/87a22e29d55df29a703f199b8af3b176.png "gpib-interface-module-assembly")](https://i0.wp.com/hackaday.com/wp-content/uploads/2022/01/gpib-interface-module-assembly.jpg?ssl=1) GPIB + Raspberry Pi Zero Interface Module

软件方面，shield 利用了现有的 Linux 内核模块 [linux-gpib](https://linux-gpib.sourceforge.io/doc_html/index.html) 。它看起来很容易安装并在 Pi 上快速运行。在花了几个小时安装了 [PyVisa](https://pyvisa.readthedocs.io/en/latest/) 和一些特定于仪器的库之后，我应该可以在不到一天的时间内用 Python 脚本自动记录数据。唉，现实并不总是符合我们的期望。

## GPIB 架构

[![](img/04a17aaac1fdfbe6b63e7429d3de7f92.png)](https://hackaday.com/wp-content/uploads/2022/01/mr-fancy-pants-bob-stern.png)

Bob “Mr Fancy Pants” Stern Operating a Rack of HP-IB Equipment in 1980

一点背景知识将有助于理解 GPIB 的概念。如果我们在 60 年代参观一个电子实验室，使用计算机来控制重复的测试序列是一个例外，而不是规则。相反，你可能会看到磁带、纸带、磁卡，甚至是用铅笔标出命令的卡片。对于某些设置，甚至不需要计算机控制。例如，温度传感器可以直接在带状图记录器上绘图，或者将数值保存在磁带驱动器上。如果你记得这是惠普工程师沉浸其中的世界，这个架构是有意义的。

[![](img/7b47995e77f335eafb2da6f9fd8b3d80.png)](https://hackaday.com/wp-content/uploads/2022/01/programming-card-yellow.png)

OMR for the HP-3260A Marked Card Programmer (from Prof Jones’s Punch Card Collection, Univ of Iowa)

GPIB 是一种灵活的互连总线，使用 15 个信号:8 位数据总线和 7 位控制线。总线上的任何设备都可以是被动的收听者或主动的讲话者。一个讲话者可以同时对多个设备讲话，如果设备有需要服务的事件，它们可以发出中断。设备使用当时很小的电缆和连接器互连，但与今天的 USB、以太网和串行电缆相比是一个麻烦。24 引脚 Centronics 连接器可以轻松实现设备的菊花链连接，但它是一个庞大的庞然大物，必要时，您可以将 GPIB 电缆有效地用作双节棍。

[![](img/c2d960ac372f4e288bfa647d68e05542.png)](https://hackaday.com/wp-content/uploads/2022/01/gpib-cable-002-e1643096265975.jpg)

GPIB Cables Can Serve as Nunchucks in a Pinch

GPIB 的传统用途是一台中央控制计算机连接一个测试设备链或星簇。这在历史上影响了可用的 GPIB 接口硬件。几十年来，ISA 和后来的 PCI 接口卡安装在计算机中，或者如果您使用的是惠普计算机，GPIB 接口可能是集成的。它们往往有点贵，但是因为一个接口板控制所有的仪器，所以在给定的测试设置中你只需要一个卡。National Instruments 已成为 GPIB 领域接口卡和支持驱动程序及软件的领导者，但他们的专有软件和高昂价格的声誉对许多小公司和家庭实验室来说有点令人不快。

您当然可以完全使用 70 年代风格的 GPIB 布线来实现自动测试设置。事实上，许多这样的遗留系统仍然存在，并且仍然需要维护。但更有可能的是，我们目前对 GPIB 的使用将是调整一两种仪器，以便它们可以在您的非 GPIB 测试设置中使用，无论是 LAN、USB、串行还是它们的某种组合。这使经济状况发生了天翻地覆的变化，也是为什么只为一种仪器寻找低成本 GPIB 适配器的原因。

 [![GPIB PCI Card from National Instruments](img/21e4c831d18f3fe27d11bf16a156af16.png "gpib-pci-ni-card")](https://i0.wp.com/hackaday.com/wp-content/uploads/2022/01/gpib-pci-ni-card.jpg?ssl=1) GPIB PCI Card from National Instruments [![GPIB USB Interface Module from Keysight](img/612e5a1a033b1bc5e60dda27bb9089f3.png "gpib-usb-keysight-box")](https://i0.wp.com/hackaday.com/wp-content/uploads/2022/01/gpib-usb-keysight-box.jpg?ssl=1) GPIB USB Interface Module from Keysight

## 让问题开始吧

Pi Zero-W 有内置 WiFi，事实上，这是唯一的局域网连接，除非你连接外部电路。但我无法让它连接到我的无线路由器。很长一段时间，我认为这是一个操作失误。我有相当多的树莓 Pi 3s 和 4 使用 WiFi 模式没有问题。当我开始解决这个问题时，我发现 Debian / Raspberry Pi 操作系统中的网络管理工具已经改变了很多年。有很多教程展示了不同的配置方式，其中一些已经过时了。

没有任何局域网连接，一个无头的 Pi Zero-W 真的死了，所以我组装了一个 USB 电缆和 HDMI 适配器的老鼠窝，这样我至少可以得到一个提示，并订购了几个 USB-LAN 适配器，让我暂时在线。几个小时的搜索和测试，我终于找到了几个模糊的帖子，表明 Pi Zero-W 的收音机在一些国家出现了连接问题——韩国就在名单上。

事实上，这就是问题所在。我可以暂时将我的路由器的 WiFi 国家更改为美国，Pi Zero-W 可以正常连接。我不能就这样离开，所以我回到了韩国，继续使用有线局域网来完成我的工作。然而，这个特殊的问题确实有一个好的结局。在 [Raspberry Pi 论坛](https://forums.raspberrypi.com/viewtopic.php?t=314361)上，他们的一名工程师证实了这个错误，并向 Cypress Semiconductors 提交了更改请求。几个星期后，我们得到了一个建议的更新固件来测试。它解决了这个问题，并有望在即将发布的版本中添加。

### 路由器发疯了

此时，我有几个 Pi 零点、一个 Pi 4B 和几个 USB-LAN 适配器都工作正常。由于这些 USB-LAN 适配器可以四处移动——一个适配器今天可能在 ABC 电脑上，明天可能在 XYZ 电脑上——我仔细标记了每个适配器，并将其详细信息输入到路由器上的/etc/hosts 和/etc/ethers 文件中。我的网络很快就瘫痪了。这很难解决，因为令人惊讶的是，当网络冻结时，从路由器提取信息是很困难的。我最终发现我在路由器的表中错误地交叉了 USB-LAN 适配器的两个条目，这让 OpenWRT 抓狂。

[![](img/12865ec5ebdf33d570e04351a684ac38.png)](https://hackaday.com/wp-content/uploads/2022/01/gpib-usb-lan-gets-labels.jpg)

USB-LAN Interfaces Get MAC Address Labels

发现和解决这个问题花了很长时间，事后看来我的解决方案有点过头了。首先我把路由器彻底擦了一遍，从头重新装了固件。我还花时间更好地组织了我的主机名和静态租赁数据。我从[Krzysztof Burghardt]中找到了[这个要点](https://gist.github.com/burghardt/d97fa4196ca4cd99bb706e8cebc05231),它将您的`/etc/hosts`和`/etc/ethers`转换成 OpenWRT 的`/etc/config/dhcp`文件，并对其进行了调整以适应我的需要。我买了第二台备用路由器，如果这种情况再次发生，我可以迅速更换。最后，但同样重要的是，我崩溃了，买了一台标签打印机，清楚地标记这些 USB-LAN 适配器的 MAC 地址。

## 准备好了吗

[![](img/1766e8986de4d3e2ba9d84514ddf9cf7.png)](https://hackaday.com/wp-content/uploads/2022/01/gpib-ready-to-go.jpg)

Let’s Measure!

最后，我准备好为我的项目做真正的工作了。忽略背景中的飞线只是为了好玩——它们会进入 Analog Discovery 2 逻辑分析仪以观察 GPIB 信号。手表是对我懒惰的一种认可——我在实验室里把一部旧智能手机放在三脚架上观察电表，并在测试 Python 脚本时从我的办公室台式电脑上监控它。每隔一段时间，视频就会锁定，我用秒针作为事情是否顺利运行的标志。在这个故事的第二部分，我将总结测量的故事，给出更多关于 GPIB 及其修订版的信息，并展示我的自动化测试设置的图表。