# 新零件日:LED 驱动器是伪装的 FPGA 开发板

> 原文：<https://hackaday.com/2020/01/24/new-part-day-led-driver-is-fpga-dev-board-in-disguise/>

我们今天的新部分是 ColorLight 5A-75B，这是一种旨在通过千兆以太网驱动八个无处不在的高密度彩色 LED 面板的板。如果你要建造一面商用 LED 墙，你需要将一堆 LED 面板拧在一起，用菊花链连接一堆这些面板来驱动它们，提供电源，这样就完成了。由于这种高容量的应用，这些主板价格低廉，每块大约 15 美元，而且你可以很快从中国买到。

![](img/75533c99956c3d398f4971eee3a052e6.png)

但我们不是来谈商业应用的。管理快速以太网并实时推送如此多的像素是一项最好由 FPGA 处理的任务，[Tom Verbeure]注意到这些东西本质上是令人惊叹的 FPGA 开发板，并开始在其上进行黑客攻击。[q3k]放在 GitHub 上，你可以跟着 [`chubby75`逆向工程项目](https://github.com/q3k/chubby75/tree/master/5a-75b)一起去挖掘他们的秘密。

虽然这些板的第一代使用的是旧的备用 Spartan 6，但当使用 Lattice ECP5-25 芯片的新版本被发现时，开放 FPGA 工具的粉丝们开始感兴趣，Lattice ECP 5-25 芯片是在[2019 Hackaday super co badge](https://hackaday.com/2019/11/04/gigantic-fpga-in-a-game-boy-form-factor-2019-supercon-badge-is-a-hardware-siren-song/)上使用的强大芯片[Sprite_TM]的小兄弟。如果你想买一个，你要找的是标有修订版 6 或 7 的彩光板。

这是什么意思？只需一个美味汉堡的价格，您就可以获得一个足以运行 RISC-V 软核的 FPGA、两个 166 MHz、2mb SDRAM、FPGA 比特流闪存、5 V 电平转换器上的大量数字输出和两个千兆位以太网端口。JTAG 端口被分成 0.1 英寸的头，它使用 OpenOCD，这非常方便。对于由完全开放的工具链提供服务的预算充足的 FPGA 开发板来说，这如何？

## 工作中的黑客

ECP5 变体的逆向工程工作仍在进行中，但现在开放 FPGA 领域有一些真正的重量级人物正在使用该板，并且进展很快。

上周，为了绘制新 ECP5 变体的引脚排列，[Mike Walters]使用了他从[Claude Schwarz]那里学到的一种特别好的技巧，这种技巧发挥了 FPGA 的优势:bit-bang 串行 UART 同时在所有*引脚上提供引脚编号。然后，输出接头上的每个引脚告诉他它连接到 FPGA 上的哪个引脚。好主意！*

就在昨天，Enjoy Digital 的[Florent]开发了一个带以太网 UART 的 picoRV 内核。

你会用这些野兽中的一个做什么？显然，驱动许多许多发光二极管。(这里有两个关于 Hub75 LEDs 的伟大参考:[一个是 Arduino](https://www.instructables.com/id/Arduino-UNO-Based-HUB75-LED-DISPLAY-DRIVER/) ，一个是树莓 Pi 的[。Sparkfun 的[Nick Poole]也有一个](https://github.com/hzeller/rpi-rgb-led-matrix)[不错的深潜](https://www.sparkfun.com/sparkx/blog/2650)。)但高带宽实时输出还有其他用途。通过以太网控制任意数量的伺服电机？或者见鬼，踏步者！就我自己而言，我对以太网的兴趣不如对内存和引脚感兴趣，但是你不得不承认以太网比特流引导程序是一个很棒的黑客。

[![](img/57232425978d40db91b3939138a31f39.png)](https://hackaday.com/wp-content/uploads/2020/01/DSCF1499_thumbnail.png)

Konrad Beckmann’s Pergola: Too many ECP5 boards, too little time!

虽然这是一项逆向工程工作——撬开封闭的设计——但在过去几年中，我们也看到了伟大的开源黑客 FPGA 板蓬勃发展。从早期的 [Dipsy](https://hackaday.io/project/6592-dipsy) 和 [Upduino](https://www.tindie.com/products/tinyvision_ai/upduino-v21-low-cost-fpga-board/) 项目，通过 [TinyFPGA](https://hackaday.io/projects/hacker/233933) 、 [BlackIce](https://www.tindie.com/products/Folknology/blackice-mx/) 和[破冰船](https://www.crowdsupply.com/1bitsquared/icebreaker-fpga)，到最近的 [Pergola](https://github.com/pergola-fpga/pergola) 和【Greg Davill】的 [OrangeCrab](https://github.com/gregdavill/OrangeCrab) 和 [ButterStick](https://github.com/gregdavill/ButterStick) ，如果你不想挂在流血的地方，你不会为开发板的选择而受伤

如果您刚刚开始使用 FPGAs，您可以支持这些出色的开发人员，这将大大节省您的时间:他们都是开放的、有文档记录的和经过测试的。我肯定我也错过了不少很棒的板子——这些只是我自己手里拿过的。(在评论里贴上你的最爱！)

但是，如果双以太网、一堆 RAM 和太多的 5 V 输出是您的 FPGA 项目所需的外围设备，或者如果您只是想帮助开发工作，ColorLight 5A-75B 可能值得一试。你肯定不能打败这个价格。