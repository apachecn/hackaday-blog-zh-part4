# 转储小米智能水壶的静态加密固件

> 原文：<https://hackaday.com/2022/05/04/dumping-encrypted-at-rest-firmware-of-xiaomi-smart-kettle/>

[aleaksah]给自己买了一个 Mi 智能水壶 Pro，一个带蓝牙连接的水壶，以及一个与之配套的智能手机应用程序。尽管很聪明，但它不能远程打开。他憧憬着一个理想的智能家庭，在那里他可以在早上醒来时打开水壶，他开始纠正这种不公平。(俄语，[译](https://habr-com.translate.goog/ru/post/663312/?_x_tr_sl=auto&_x_tr_tl=en&_x_tr_hl=en)先是把水壶拆了，打算把固件转储，修改一下，再闪回去。听起来很简单，难在哪里？

这个水壶是围绕 QN9022 控制器构建的，来自相当开放的 [QN902X 系列芯片。](https://www.nxp.com/products/wireless/bluetooth-low-energy/qn9020-21-22-ultra-low-power-bluetooth-le-system-on-chip-solution:QN902X#overview) QN9022 需要一个外部 SPI 闪存芯片来编码，与其兄弟产品 QN9020 和 QN9021 不同，后者具有类似于 ESP8285 的内部闪存。你可能会认为转储固件只是读取闪存的问题，但固件是静态加密的，每个 MCU 都有一个唯一的密钥，并存储在内部。当微控制器读取闪存芯片内容时，它们在执行前被透明地解密。因此，必须找到一些其他方法，将 MCU 本身作为唯一可以访问解密密钥的实体。

![The board from the kettle, with a USB-UART connected to it](img/a86545896b8958f9314420582a08d8b6.png) [aleaksah]考虑了 SWD 接口，这是一个功能强大的调试接口，也是许多 MCU 内部数据访问的常用接口。遗憾的是，这种微控制器有锁定位，用于阻止 SWD，在您的产品离开工厂时进行设置。当然，并不是每个厂商都设置那些位，但无论如何检查 SWD 接口后，它不会响应，他决定走另一条路。他欣喜地发现了 MCU 内部引导程序的文档，并决定将自己的代码加载到 RAM 中，从内部转储闪存内容。然而，read 命令似乎触发了引导装载程序对闪存进行加扰或擦除，给他留下了一个死单元。

他坚持不懈，并决定研究引导程序代码本身，加载另一个 RAM 存根来转储引导程序代码。在反编译 bootloader 之后，除了几个没有记录但没意思的命令，他发现加载任何类型的程序，确实会向闪存芯片发送执行闪存擦除的命令。从这里开始，他理论上可以用镊子破解，通过短路数据引脚对闪存进行写保护——然而，他决定找到一种适当的转储方法，如果内置闪存的芯片出现在我们的办公桌上，这种方法将扩展到内置闪存的芯片。

此后不久，他有了重大发现。不同的 SPI 闪存芯片系列具有不同的读/写/擦除和其他操作命令，引导加载程序公开了一个结构，您可以修改该结构，以针对所连接的闪存芯片类型使用不同的命令。简单地用无害的东西替换该结构中的 flash erase 命令，即使新代码从外部加载到 RAM 中，flash 内容也保持不变。因此，[aleaksah]发现了一种从任何 QN902X 系列 MCU 中转储加密静态固件的方法，只需使用 USB-UART、芯片的内置引导加载程序和一个小型代码转储存根 [(GitHub)。](https://github.com/aleaksah/qn902x-dump)

又一天，另一个固件读出保护机制规避！找到这样的漏洞对很多有趣的旅程都有好处，比如最近的黑客攻击帮助我们接入无数基于 STM32 的设备。你甚至可以用丰富的 ST-Link 程序员[作为你的训练场！](https://hackaday.com/2016/12/10/reverse-engineering-an-st-link-programmer/)如果你的设备上的 SWD 接口没有解锁，看看这个关于[使用 SWD 改装第三方 Xbox 控制器的教育之旅。](https://hackaday.com/2020/02/11/xbox-controller-provides-intro-to-swd-hacking/)想知道怎么修改自己甩的固件？我们刚刚报道了一个黑客[用 Ghidra 修改了他们库兹韦尔合成器的固件](https://hackaday.com/2022/05/03/patching-the-kurzweil-k2500-synthesizer/)！