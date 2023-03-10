# 动手操作:GreatFET 是一款嵌入式工具，可以完成所有工作

> 原文：<https://hackaday.com/2019/07/02/hands-on-greatfet-is-an-embedded-tool-that-does-it-all/>

现场有一个新的嵌入式黑客工具，它为你提供了一个交互式 Python 接口，在一个具有大量 GPIO 的板上提供了一个快速的芯片，能够伪装成不同的 USB 设备，并保留了一些技巧。这是 GreatFET，深受爱戴的 GoodFET 的继任者。

大约一年前，我第一次听说这个板即将推出，并要求提前看看。4 月底开始发货时，他们给我发了一个。让我们来亲自体验一下来自 Great Scott Gadgets 的 GreatFET】。

## 大量快速 I/O，可从您的计算机直接访问

GreatFET 是嵌入式项目的折叠刀——它意味着在开发过程中代替多种工具和组件，以便您可以立即解决眼前的问题，并在以后解决其他问题。例如，考虑测试一个新的芯片。你可以把它连接到你最喜欢的微控制器上，编写并刷新一些测试代码，看看你测试的芯片第一次是否能工作。但是很有可能你把 I2C 的地址搞错了，或者你把 TX/RX 或者 MISO/MOSI 接反了，或者其他很多常见的错误。

最简单地说，GreatFET 旨在为您提供一个交互式 Python shell 来控制板上的大量 IO 引脚。您运行命令并以最快的速度获得反馈。但这只是伟大 FET 的冰山一角。在更高级的方面，该板可以用来仿真 USB 设备，作为构建定制仪器仪表的数据采集设备，用于 MSP430 闪存和调试，或者作为制造环境中的自动测试设备。

官方命名为 GreatFET One，该板在可用引脚、马力和软件交互性方面是一个巨大的飞跃，MSRP 为 89.99 美元。

## GreatFET 硬件概述

 [![GreatFET top view](img/44816e3be4f1284070084816a322df6d.png "GreatFET-front-square")](https://hackaday.com/2019/07/02/hands-on-greatfet-is-an-embedded-tool-that-does-it-all/greatfet-front-square-2/)  [![GreatFET bottom view](img/a3eff65481a44b4e4b9a9bb9cce2ad28.png "GreatFET-back-square")](https://hackaday.com/2019/07/02/hands-on-greatfet-is-an-embedded-tool-that-does-it-all/greatfet-back-square-2/) 

GreatFET 的核心芯片是采用大规模 LQFP-144 封装的恩智浦 LPC4330。在电路板的两侧，您可以看到大部分 144 引脚已经断开，带有 40 引脚母接头。一侧还有一个“奖励行”SIL-20 引脚接头。这里的愿景是能够使用 shields 向电路板添加硬件，Great Scott Gadgets 称之为“邻居”,作为对设计原始 GoodFET 的[Travis Goodspeed]的致敬。

LPC4330 与 HackRF 上的芯片相同；32 位 ARM Cortex-M4，时钟速度高达 204 MHz。HackRF 已经成为软件设计无线电领域的佼佼者，你可以将它视为一个类似的设备，没有模拟无线电电路。该板有一个高速 USB 端口，用于与您的计算机接口，还有一个全速 USB 端口，因此它可以用作 FaceDancer 来模拟 USB 设备，但受 Python 控制。

 [![Labels on underside of board](img/661ade738d649e14ef9812873aafb462.png "GreatFET-superb-labels")](https://hackaday.com/2019/07/02/hands-on-greatfet-is-an-embedded-tool-that-does-it-all/greatfet-superb-labels-2/) Labels on underside of board [![Pin headers labelled on edges](img/94de273894fa66195edde68bad6708fb.png "GreatFET-USB0-and-jtag")](https://hackaday.com/2019/07/02/hands-on-greatfet-is-an-embedded-tool-that-does-it-all/greatfet-usb0-and-jtag-2/) Pin headers labelled on edges [![USB1 label has "(Connect to target)" hint. There s 3.3V pin tolerance reminder too!](img/6f7fa9c16ef541940fb750489f4633b6.png "GreatFET-winbond-and-USB1")](https://hackaday.com/2019/07/02/hands-on-greatfet-is-an-embedded-tool-that-does-it-all/greatfet-winbond-and-usb1-2/) USB1 label has “(Connect to target)” hint. There s 3.3V pin tolerance reminder too!

我必须对这块板上的标签上伟大的斯科特小玩意表示敬意。使用开发板进行原型制作的一个烦恼是，将一束跳线连接在工作台上，然后必须移动它才能读取板底部的引脚标签。GreatFET 引脚的两侧都有标签，顶侧标签位于外侧边缘。SDA、SCL、MISO 或 MISO 等常用信号都有单独的标签。两个 USB 端口都标有提示，告诉你你在找哪一个，底部的所有测试垫都有描述性标签。在 KiCon 和其他现场活动中，一种形状和尺寸与电路板~~相同的贴纸~~被分发出去，用来定位特殊用途的引脚。

 [![Daffodil "Neighbor" board and "wiggler" lever tool to separate it from the GreatFET](img/ee5b54a2615ee0f487cc4fcfe21b8c96.png "GreatFET-Daffodil-neighbor-board")](https://hackaday.com/2019/07/02/hands-on-greatfet-is-an-embedded-tool-that-does-it-all/greatfet-daffodil-neighbor-board/) Daffodil “Neighbor” board and “wiggler” lever tool to separate it from the GreatFET [![GreatFET-pinout-sticker](img/7f84da9d898050928136ccb8db33a0cb.png "GreatFET-pinout-sticker")](https://hackaday.com/2019/07/02/hands-on-greatfet-is-an-embedded-tool-that-does-it-all/greatfet-pinout-sticker/) 

您可以轻松跳线您需要的信号，但对于更强大的应用，您可能需要购买或建立一个邻居。我的评估套件包括一个水仙花邻居，它给聚会带来了一个无焊试验板。由于间距可预测为 0.1 英寸，您可以使用 protoboard 和两个双排引脚接头轻松构建自己的邻居。构建邻居时，额外的引脚行是可选的。每个 GreatFET One 都明智地包括一个“wiggler”，这是一个由 PCB 制成的简单工具，用于在不弯曲引脚的情况下撬开两块电路板，你需要它来克服连接两块电路板的 100 个引脚。

## 软件提供强大的多功能性

是的，这块板上的硬件是个庞然大物，但软件最有希望实现多功能性。我不知道这是软件极客的硬件工具还是相反，但它肯定以一种好的方式模糊了界限。

软件的当前状态还不太成熟，文档和 API 都在开发中。我一开始遇到了一些问题，但是一旦解决了，我测试的部分就简单了，使用的 API 部分也简单明了。

首先抓到你了。我试着为 Python 2.7 安装这些库，但没有成功；你必须使用 Python 3，这很好，因为 Python 2。x 从现在起六个月后到达寿命终点。接下来，我在可靠地连接到电路板上时遇到了问题，并且愚蠢地认为我有 udev 问题，而实际上我有一根不可靠的 USB 延长线。最后，我没有进行固件升级，这是你在新硬件上应该做的第一件事。幸运的是，如果你遵循[入门指南](https://greatscottgadgets.github.io/greatfet-tutorials/getting-started.html)，所有这些事情实际上都非常简单。

```
$ sudo pip3 install --upgrade greatfet

$ gf info
Found a GreatFET One!
  Board ID: 0
  Firmware version: git-2019.5.1.dev0
  Part ID: a0000a30654364
  Serial number: 000057cc67e630187657
$ gf fw --auto
Trying to find a GreatFET device...
GreatFET One found. (Serial number: 000057cc67e630187657)
Writing data to SPI flash...
Written 84812 bytes of 84812.
Write complete!
Resetting GreatFET...
Reset complete!

```

![Python document help for DAC on the GreatFET](img/8439550552cd91a4a8e2461ac3123bde.png)

Python doc for GreatFET DAC API

在这里，您可以通过命令行界面来控制电路板，在 Python shell 中输入命令，或者编写并运行自己的 Python 脚本。这里有一点学习曲线。[在线文档](https://github.com/greatscottgadgets/greatfet/wiki)和[教程](https://greatscottgadgets.github.io/greatfet-tutorials/)现在都有点稀缺，大部分可用信息都在 greatfet Python 包本身中。例如，输入`help(gf.apis.dac)`可以帮助我判断 DAC 输出要探测哪个引脚。

也就是说，许多现有的功能都被移植到 GreatFET 上，所以如果你习惯于将 GoodFET 与 MSP430 一起使用，或者将 Facedancer 用于 USB 开发，我想你会有宾至如归的感觉。让我们试开一下这个。

## 试运行:I2C、DAC 和 Facedancer

[![](img/aceaf6fcf81b7f702b37e9beabdaa70e.png)](https://hackaday.com/wp-content/uploads/2019/06/greatfet-oled-i2c-test.jpg)

我经常使用交互工具(主要是一个巴士海盗)的地方之一是在尝试新的屏幕。这是因为它们通常有一长串启动它们所必需的初始化命令，我想在开始为项目编写和编译代码之前确保我有这个权利。

### I2C 有机发光二极管展示

事实证明，使用 GreatFET 非常容易。仅仅几分钟后，我就连上了一个屏幕，显示出一个交叉影线图案。board 是我们在上面安装的 greatfet 库中的一个 Python 对象，使用 tab 补全时会出现该库中的文档。我用扫描功能找到了地址。I2C 命令可以通过将 0x80 或 0x40 添加到字节数组的开头来发送，以表示命令写入或数据写入。

![Python help for GreatFET I2C API](img/9077e2759e7dabbd023c7db8a2ee79bf.png)

Python’s help() function provides the most verbose documentation

这是我使用的代码。我真的很喜欢快速编写这样一个脚本的能力，因为提交给 GitHub 供我(或其他人)将来使用非常简单。

```

from greatfet import GreatFET

ssd1306init = [0xA8, 0x1f, 0xd3, 0x00, 0x40, 0xa0, 0xc0, 0xda, 0x02, 0x81, 0x7f, 0xa4, 0xa6, 0x20, 0x00, 0x21, 0x00, 0xff, 0x22, 0x00, 0x03, 0xd5, 0x80, 0x8d, 0x14, 0xaf]

gf = GreatFET()

addrscan = gf.i2c.scan()

addr = 0

for i in range(len(addrscan)):
    if addrscan[i][0] != False:
        # i is both the index of the array
        # and the address tested in the scan
        addr = i

if addr != 0:
    #Initialize the OLED
    gf.i2c.write(addr, [0x80] + ssd1306init)

    #Make screen buffer and fill with hash pattern
    screenbuff = list()
    screenbuff += 128*[0xCC,0xCC,0x33,0x33]

    #Write screen buffer to OLED
    gf.i2c.write(addr, [0x40] + screenbuff)

```

### 10 位分辨率的 0-3.3V 数模转换器

[![](img/1d393364fb2a706bebad56a501d77ec0.png)](https://hackaday.com/wp-content/uploads/2019/06/greatfet-dac-test.jpg)

接下来，我测试了 DAC。这里没什么可报告的。Python help(gf.apis.dac)函数告诉我们如何设置电压以及哪个引脚用于输出:“设置 ADC0_0 (0-1023)上的 dac 值”。查看 wiki 上[巨大的引脚函数列表，我看到 J2 引脚 5 映射到 ADC0_0。您可以看到，我的 DMM 验证了将值设置为 512 (50%的分辨率)会产生 50%的 3.3 V 供电轨:](https://github.com/greatscottgadgets/greatfet/wiki/GreatFET-One)

```
&gt;&gt;&gt; gf.apis.dac.set(512)
```

### Facedancer USB 仿真

GreatFET 产品页面链接到一个可以用来模拟 USB 设备的 Facedancer repo ,所以我决定也尝试一下。自从 Travis Goodspeed 在 2012 年开始展示原型以来，我就知道这个工具[，但这是我第一次尝试它，它真的很棒。](https://hackaday.com/2012/07/05/facedancer-board-lets-your-python-programs-pretend-to-be-usb-hardware/)

![GreatFET Facedancer emulation](img/068092531290bdac766bbd4ae9f4d1e7.png)

您使用两条 USB 电缆，它们都通过 microUSB 连接到电路板，并通过 USB Type-A 连接到计算机(不一定是同一台计算机)。Facedancer 软件是用 Python 编写的，我还必须安装 pyserial，它包括几个不同的示例。环顾四周，我发现最简单的方法是使用主板挂载 ISO 文件。这使得 GreatFET 看起来像一个存有文件的 u 盘。我手头上有一个旧版本的 Mint，是我在测试中使用的。

```
$ git clone git@github.com:usb-tools/Facedancer.git
$ sudo pip3 install pyserial
$ cd Facedancer
$ ./facedancer-umass.py /Marge/linuxmint-18.3-cinnamon-64bit.iso

```

[![](img/35df48f8d691ed7a733c9606f3b0f320.png)](https://hackaday.com/wp-content/uploads/2019/06/GreatFET-spoofing-Mint-install-ISO.png)

## 完全失败:您可以从中恢复过来！

greatfet 类有一个函数叫做 onboard_flash。不要玩这个功能。我没有仔细阅读 doc 对此的评论，只是顺其自然地将“Hackaday”写到这个 flash 的第一个地址空间。当然，我一重启主板，它就不再枚举了。此功能允许您覆盖编程到主板的固件。回过头来看这个错误，这显然是一个警告:

![Python document help for onboard_flash on the GreatFET](img/6aadac55cd9a96a508a1f0fdcb664150.png)

故事的简短版本:在你的计算机上安装的 greatfet Python 包中内置了一个 DFU 模式。长的版本是，我从源代码编译，无法得到我的二进制文件来复活板。在 GitHub 上打开一个问题后，我被引导到正确的命令。首先，您不应该运行的代码:

```

In [46]: #Do Not Run This Code!
In [47]: arr = bytes("Hackaday",'utf-8')

In [48]: gf.onboard_flash.write(arr,address=0x00,erase_first=True)

In [49]: gf.onboard_flash.read(0x00,8)
Out[49]: array('B', [72, 97, 99, 107, 97, 100, 97, 121, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0])

```

如果你碰巧这样做了，或者做了任何其他愚蠢的事情来破坏你的主板，恩智浦芯片有一个非常简单的硬件 DFU 模式，可以在大约 20 秒内让你重新启动并运行。只要按住板上的“DFU”按钮，按下并释放“重置”按钮，然后运行以下命令:

```
$ gf fw --dfu --autoflash
dfu-util 0.9
Copyright 2005-2009 Weston Schmidt, Harald Welte and OpenMoko Inc.
Copyright 2010-2016 Tormod Volden and Stefan Schmidt
This program is Free Software and has ABSOLUTELY NO WARRANTY
Please report bugs to http://sourceforge.net/p/dfu-util/tickets/

dfu-util: Invalid DFU suffix signature
dfu-util: A valid DFU suffix will be required in a future dfu-util release!!!
Opening DFU capable USB device...
ID 1fc9:000c
Run-time device DFU version 0100
Claiming USB DFU Interface...
Setting Alternate Setting #0 ...
Determining device status: state = dfuIDLE, status = 0
dfuIDLE, continuing
DFU mode device DFU version 0100
Device returned transfer size 2048
Copying data from PC to DFU device
Download [=========================] 100% 52736 bytes
Download done.
dfu-util: unable to read DFU status after completion
Trying to find a GreatFET device...
libgreat compatible board in flash-stub mode found. (Serial number: 000057cc67e630187657)
Writing data to SPI flash...
Written 84812 bytes of 84812.
Write complete!
Resetting GreatFET...
Reset complete!

```

## 如果你选择使用它，这个工具可以做所有的事情

对 GreatFET 的最终裁决是什么？如果你决定全力以赴，把这块板作为你的工具箱，它将名副其实，成为一个伟大的工具。

几乎所有的工作台工具都是如此，对吗？如果你真的很擅长使用示波器，但又需要使用一个朋友的不同制造商的示波器来执行一些高级的技巧，这将需要你花一些时间来搞清楚。GreatFET 有一个学习曲线，但是如果你投入时间并把它作为你的首选工具，你可以用它做的事情将会是无限的。然而，如果你很少使用它，你就需要每次都回头看一下教程。

对我来说，这个工具非常有意义，因为我经常在桌面上使用 Python。我可以将我的 GreatFET 脚本提交给 repo，然后作为我自己的教程来回顾它们。这是我以前的首选工具，巴士海盗，它有自己的生活终端语言，我必须不断重新学习，没有同样容易保存和引用以前的黑客会话的能力。Python 的可扩展性如此之大，以至于您需要做的任何数据处理、日志记录或 IO 操作都是可能的，而且相对容易。

这个主板上的芯片的能力是疯狂的，但老实说，你为什么不去寻找一个强大的芯片在 IO，速度，内存等方面。很有可能你永远不会超越这个芯片的功能。电路板的标签和接口方法都是经过深思熟虑的，并且执行得很好。我看不出 GreatFET 的硬件有什么比这更好的了。

我唯一犹豫的是文档和 API 的状态。目前，我看不到读取 ADC 的方法，也不确定 ADC 是否只有一个引脚，或者是否可以复用多个引脚。这只是教程和快速入门信息的 alpha 状态的一个例子。但我完全期待这种情况会有所改善。该项目是完全开源的，该团队擅长应对 GitHub 问题，我认为随着越来越多的人开始使用该板，用户贡献的例子将会越来越多。