# 动手操作:威士忌海盗 DC29 硬件徽章 Blings 与 RISC-V

> 原文：<https://hackaday.com/2021/08/06/hands-on-whiskey-pirates-dc29-hardware-badge-blings-with-risc-v/>

威士忌海盗队再次为 DEF CON 29 掉落了一枚出色的电子徽章。当然，这是非正式的，但肯定是今年迄今为止最热门的定制珠宝。

我不能亲自去现场，但海盗们还是送来了一个徽章让我先看看。这是华丽的，凝视着电路板，很容易认为芯片短缺不是这个徽章上的东西。但这仅仅是因为一些非常有创意的零件采购和大量有灵感的设计工作。

## 审美

[![](img/a56d5e57f65e1f37d80081a351ef7a2c.png)](https://hackaday.com/wp-content/uploads/2021/08/whiskey-pirates-dc29-edge-bling.jpg)

我通常从硬件概述开始，但拜托，这东西看起来很壮观！先说审美。这是硬件徽章更精致的外观之一，类似于[queer con 15 徽章](https://hackaday.com/2018/08/11/teardown-queercon-15-badge-and-the-game-hidden-within/)，它使用 PCB 面板和背面，由边缘发光的丙烯酸树脂隔开。[TrueControl]将 PCB 夹在两片丙烯酸树脂之间，其中一片用作具有蚀刻和半透明区域的面板，一片透明背板将侧发光 RGB LEDs 带到可以看到它们的地方。

[![](img/3dfe8dd73db4ce843040b25996feaeca.png)](https://hackaday.com/2021/08/06/hands-on-whiskey-pirates-dc29-hardware-badge-blings-with-risc-v/whiskey-pirates-dc29-button-caps/)[![](img/9f5eb777394c6e61a76cc5434cb17b39.png)](https://hackaday.com/2021/08/06/hands-on-whiskey-pirates-dc29-hardware-badge-blings-with-risc-v/whiskey-pirates-dc29-menu/)[![](img/c3fa3c78538b090c233f0ef85895f453.png)](https://hackaday.com/2021/08/06/hands-on-whiskey-pirates-dc29-hardware-badge-blings-with-risc-v/whiskey-pirates-dc29-nametag-rotate/)

在每个交叉骨骼的末端有一个黑色矩形。起初我以为这是某种红外反射传感器，但它们实际上是按钮帽。它看起来像是从丙烯酸树脂中切割出来的，厚度大小正好与面板平齐。它们被强力胶粘在板上的瞬时按钮开关上。

这些帽子看起来棒极了。这个功能有点粗糙，因为开关的投掷非常浅。我不小心把其中一个弄掉了，可能是压得太紧了。一点胶水就把它粘好了。

[![](img/9b4967ab29a6833c87b3af08dfc3352f.png)](https://hackaday.com/wp-content/uploads/2021/08/whiskey-pirates-dc29-back-bling.jpg)

一个有机发光二极管显示器透过面板的前额发光。徽章作为一个姓名标签，可以从菜单中定制。其中一个不错的地方是，[TrueControl]再次使用了他的奇特固件技巧，即倾斜你名字的字母，以匹配徽章的角度。相当光滑！

## 拆除硬件

[![](img/f5abd99b1021858b719b5db55e5b035e.png)](https://hackaday.com/wp-content/uploads/2021/08/whiskey-pirates-dc29-pcd-populated-rotated-e1628188732961.jpg)

你必须有雄心壮志才能看清楚组装板，因为它通常被丙烯酸板和 AAA 电池座覆盖。拆焊并拆除梅花头螺钉后，我们就剩下一个非常漂亮的组装板了。

我们在这里找到了一些创造性的零件来源。主芯片是 giga devicesGD 32 VF 103([PDF 数据表](http://www.gd32mcu.com/data/documents/shujushouce/GD32VF103_Datasheet_Rev%201.1.pdf))，它是一个 RISC-V 内核(不要与 GD32F103 混淆，它是一个 ARM Cortex-M3)。[TrueControl]推测这可能是第一个采用硬件 RISC-V 内核的非官方徽章项目—[2019 年的 Hackaday Supercon 徽章](https://hackaday.com/2019/11/04/gigantic-fpga-in-a-game-boy-form-factor-2019-supercon-badge-is-a-hardware-siren-song/) 在 FPGA 上运行 RISC-V 软件内核。板上还有一个 PDK13(红木芯片之一——看看我们不久前介绍过的指南中的[)和一个基于 8051 的 USB 芯片(CH552T](https://hackaday.com/2019/09/09/everything-you-wanted-to-know-about-padauk-mcus-and-more/) [PDF 数据表](https://datasheet.lcsc.com/lcsc/2008191734_WCH-Jiangsu-Qin-Heng-CH552T_C111367.pdf))靠近电路板底部，用于调试。

 [![whiskey-pirates-dc29-PCB-front](img/17ac12cedb8485b6a65579c7bbc010a3.png "whiskey-pirates-dc29-PCB-front")](https://hackaday.com/2021/08/06/hands-on-whiskey-pirates-dc29-hardware-badge-blings-with-risc-v/whiskey-pirates-dc29-pcb-front/)  [![whiskey-pirates-dc29-PCB-rear](img/318dbd31c043a4c4214ec4b078fc2e8c.png "whiskey-pirates-dc29-PCB-rear")](https://hackaday.com/2021/08/06/hands-on-whiskey-pirates-dc29-hardware-badge-blings-with-risc-v/whiskey-pirates-dc29-pcb-rear/) 

一侧有一个硬电源开关。我还发现电池座旁边有两个自上而下的 USB 端口。我尝试了每一个；一个枚举并激活徽章，另一个不枚举但激活徽章。当在串行端口上探测时，我看到了字符的回声，但除此之外我没有探索太多。

组成眼睛的两个 RGB leds 似乎在闪烁，我怀疑那里有一些数据传输。如果你仔细观察右下角按钮附近的电路板，会发现有两个焊盘，面板上的一个切口为它扫清了道路。这可能是某种类型的光传感器，尽管它可能只是一个红外 LED，因为我希望接收器有三条腿。

[![](img/1d672aa996e9ff03e78510b210e7e5c0.png)](https://hackaday.com/2021/08/06/hands-on-whiskey-pirates-dc29-hardware-badge-blings-with-risc-v/whiskey-pirates-dc29-usb-connectors/)[![](img/eae4b317f2a50bc5ea3b25302ba3e976.png)](https://hackaday.com/2021/08/06/hands-on-whiskey-pirates-dc29-hardware-badge-blings-with-risc-v/whiskey-pirates-dc29-oled-trick/)

这里还有另一个窍门，那就是如何廉价地采购有机发光二极管银幕。仔细观察这张图，你会发现它允许引脚接头的尾部桥接至 PCB 上的一些焊盘。这些模块既便宜又丰富，但你有没有尝试过采购裸屏并放置自己的组件来驱动它们？

## 威士忌海盗队的又一次精彩表演

[![](img/122b06d71066bfd342e92037a0e8e865.png)](https://hackaday.com/wp-content/uploads/2021/08/whiskey-pirates-dc29-whats-in-box2-rotated-e1628277599659.jpg)

制作硬件徽章的最重要的方面很容易在这一点上找到:激情。让流行病和芯片短缺见鬼去吧，[TrueControl]执行了伟大的想法，让这个想法越过了终点线。电子设计非常有趣，外观达到了每个人都会为之着迷的水平。

包裹里有几个版本的面板。我很荣幸他花时间把我的名字刻在不止一个，而是三个盘子上。看一下它的那一部分——它没有以蚀刻结束，那些字母用白色油漆填充以使它们突出。

如果你参加今年的 DEF CON 29，请留意穿这些的人。那是威士忌海盗团，和他们在一起很开心。希望我在 DC30 上有机会再次这样做！