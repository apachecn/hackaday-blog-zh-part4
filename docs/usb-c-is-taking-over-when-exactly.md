# USB-C 正在接管…具体是什么时候？

> 原文：<https://hackaday.com/2020/06/23/usb-c-is-taking-over-when-exactly/>

USB 是有史以来最受欢迎的计算机接口之一。它于 20 世纪 90 年代中期发展起来，缓慢但稳步地迈向顶峰。它提供了一个具有良好速度的接口和一个紧凑的连接器，成为连接接口设备和存储器的标准，甚至成为谈论老式串行接口的事实方式。

2014 年末，USB 实施者论坛最终确定了 USB-C 插头的标准。它的第一个主要应用是在 Nexus 5X 这样的智能手机上，它已经主导了智能手机市场，至少如果你把 iPhone 放在一边的话。然而，它还没有真正发送 USB-A 包装，特别是在桌面上。怎么回事？

## 外设就在那里

![](img/aea3d7db3fdd36f9a5a7709b8c7fdd83.png)

USB-C peripherals are hard to find, but they are out there. They’re primarily aimed at the laptop market, as desktops lag in implementing USB-C.

从根本上说，这一切都归结于外设。即使在 2020 年，普通电脑都有一堆经典的 USB-A 端口，有时在配置良好的台式机上有 10 个或更多。与此同时，仍然有可能买到没有 USB-C 端口的笔记本电脑。如果普通用户从货架上拿起一个新键盘，带回家发现一个 USB-C 连接器，他们会完全不走运——可能会非常愤怒。制造商还没有调整他们的产品线来适应 USB-C 的未来。因此，与此同时，商用外设——键盘、鼠标等——将继续配备经典的 USB-A 连接器。

还有兼容性的问题。例如，英特尔 NUC NUC8i7HVK 是一款紧凑的计算系统，内置 11 个 USB 端口。有五个 USB 3 端口(类型 A)，两个 USB 3.1g2 端口(类型 A)，两个 USB 3.1G2 端口(类型 C)，还有两个 USB 3.1g2 端口也支持雷电 3(类型 C)。

![](img/52b785a7984d51ee6c15bcdc1409e557.png)

Flash drives are actually a solved problem. SanDisk have been shipping drives with both connectors for several years now, and as a bonus, they can plug straight into your smartphone for added storage.

这导致用户可以将设备插入合适的端口，但不支持所连接的硬件。例如，Thunderbolt 转 HDMI 连接器可以插入任何一个 C 类端口，但只能在支持 Thunderbolt 的两个端口中工作。即使对于有经验的用户来说，这也是一个绝对令人头疼的问题，他们中的大多数人没有时间去记住大量晦涩难懂的规范以及哪些端口支持哪些接口。彩色编码和标签有所帮助，但从根本上说，这是从旧世界的倒退，在旧世界中，你插入 USB 端口，事情就可以工作了。

即使在智能手机领域，USB-C 也占据了滩头阵地，事情仍然不确定。新标准允许更高的电流和更高的电压，使充电比以往更快。然而，[并不是所有的 USB-C 电缆都能胜任](https://hackaday.com/2019/07/29/usb-c-one-plug-to-connect-them-all-and-in-confusion-bind-them/)的工作，许多省略了几条线路或组件来实现这一操作。将一个连接器用于数据和充电很方便，但它将市场分成了“仅数据”和“数据和充电”USB-C 电缆。此外，笔记本电脑也可以使用电源传输标准，这再次创造了一种更高等级的 USB-C 电缆，可以处理高达 100 W 的功率。

对于外行人来说，这些看起来都一样。需要对硬件和电子设备有扎实的理解，才能梳理出每种设备的不同功能。这些标准如此令人困惑，甚至树莓基金会在第一次尝试时也犯了错误。

不管怎样，硬件社区继续适应。黑客像飞蛾扑火一样飞向一个良好的电源，我们已经看到许多 mod 利用 USB-PD 标准。 [USB 烙铁现在很普遍，](https://hackaday.com/2019/11/01/adding-usb-c-to-the-ts100/)和[其他人已经把它用于给电池充电。](https://hackaday.com/2019/02/23/charging-lipos-with-usb-power-delivery/)我们也开始看到 staples 接手这一事业，Arduino 板随着新连接器的到位开始发芽[。](https://hackaday.com/2019/09/04/an-arduino-pro-micro-with-usb-c/)很明显，社区已经为新标准做好了准备，尽管行业还没有跟上。

## 一个真正的解决方案–给我们端口！

![](img/31d251d45326909b1e483c898b675858.png)

An ASUS gaming motherboard launched in late 2019 – featuring just one USB-C port.

实际上，外设制造商还不打算开始生产带有 USB C 接口的键盘和鼠标。笔记本电脑最多只有一个或两个端口，通常需要一个来充电，这是不可行的。台式机的情况更糟，甚至高端主板通常只有一个 USB-C 连接器。正常的设置通常包括键盘、鼠标、网络摄像头，还经常包括耳机，一根电缆根本不够用。

集线器、加密狗和适配器是最坏的解决办法，而不是一种生活方式。相反，向前发展需要硬件公司的承诺。如果我们要看到向单一连接器生态系统的过渡，笔记本电脑和台式机需要开始配备三个或更多 USB-C 端口，并慢慢减少 USB-A 端口的数量。一旦有了安装基础，工厂很快就会转而使用 USB-C 连接器来运输硬件。传统电脑将能够通过 USB-A 到较新的 USB-C 硬件的适配器，在那里做出这样的妥协更容易被接受。像现有打印机这样的设备甚至不需要升级——一根简单的 USB-C 到 USB-B 电缆就可以让它们无缝地与新电脑配合工作。

此外，USB-IF 应与英特尔合作，尽一切可能为端口带来稳定的功能集。随着 USB 4 的出现，这个时机再好不过了。显然，用一根电缆处理高功率充电、高带宽视频和一般接口任务，总会出现混淆。当他们的口袋大小的 USB 电源无法运行他们的 Macbook Pro 时，技术倾向较低的人会仰望天空并哭泣——我要补充的是，这是理所当然的。然而，木已成舟，至少还有空间让这一过程变得更加容易。让尽可能多的 USB-C 端口可用，并让尽可能多的端口彼此行为相同，以便用户知道会发生什么。到那时，也只有到那时，我们才会知道和平——世界其他地方也会加入这个行列！