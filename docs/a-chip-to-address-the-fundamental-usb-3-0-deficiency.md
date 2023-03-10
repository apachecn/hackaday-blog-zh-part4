# 弥合 USB 2–USB 3 鸿沟的芯片

> 原文：<https://hackaday.com/2022/03/07/a-chip-to-address-the-fundamental-usb-3-0-deficiency/>

在 Twitter 上，[whitequark]发现并强调了一个有趣的设计——[VL 670](https://twitter.com/whitequark/status/1410207408371245062)的分线板，伴随着一篇广泛而[非常容易理解的关于其用途和内部工作方式的文章](https://notabug.org/niconiconi/vl670)。VL670 芯片解决了一个令人惊讶的问题——将 USB 2.0 信号转换为 USB 3.0 信号。

如果你有一个 USB 2.0 设备和一个只有 USB 3.0 信号的主机，这个芯片就是为你准备的。这可能令人困惑——为什么需要这样做？这是关于 USB3 鲜为人知的黑暗秘密，任何人都可以推断出他们是否必须处理 9 针 USB 3.0 连接器，其中三个差分对中的一个不完全接触。

当你看到一个蓝色的“3.0”端口时，它实际上是 USB 2 *和*USB 3——两个独立的接口连接到一个连接器上。USB 3 使用两个单向差分对，类似于 PCI-E，而 USB 2 使用一个双向差分对，蓝色连接器上的两个接口基本上相互独立工作。如果你简单地把“USB 3.0”当成“更快的向后兼容 USB”，这有许多违反直觉的含义，并且它们有[痛苦的后果](https://www.reddit.com/r/AskElectronics/comments/7meqrg/weird_usb_31_problem_looking_for_existing_device/)。

例如，USB 3 集线器 IC 内部有两个独立的集线器实体，一个用于 USB 3，一个用于 USB 2。即使你有一个 USB 3 集线器插在 USB 3 端口上，多个 USB 2 设备插在上面仍然无法突破 USB 2 上行 480 MBps 的限制。如果你曾经认为一个具有更快上行链路的更快集线器可以解决你的 USB 2 设备速度问题，那么显然，USB-IF 工程师的想法不同。您可能必须为您的“许多便宜的 SDR 和 Pi 4 在一个盒子里”设置找到一个变通办法。

作为一个有趣的聚会技巧，由于 [USB 3 设备枚举仅使用 USB 2 作为后备](https://electronics.stackexchange.com/questions/297031/usb-3-x-ss-enumeration/297373#297373)，理论上，您可以将八个设备连接到一个四端口 USB 3 集线器——四个 USB 2 设备和四个 USB 3 设备。事实上，[有些 USB 设备专门使用 USB 3 线](https://twitter.com/WifiCable_/status/1497934328868884492)，甚至不连接 USB 2 线。是的，这也意味着你可以将六个 USB 设备连接到一个 Raspberry Pi 4，如果你将 OTG 端口切换到主机模式，甚至可以连接七个。

所以如果你发现自己卡在 USB 2 和 USB 3 之间， [VL670 是一个功能性的解决方案](https://twitter.com/whitequark/status/1415999233136680960)。但是因为它解决了标准中的一个缺陷，所以它本身并不完全符合标准。(并不是说不符合 USB 标准曾经阻止过任何人。)

有一个开源的 devboard，你可以订购零件并进行构建，淘宝上似乎可以买到 VL670 芯片。这个芯片最初是用来做什么的？显然，VirtualLink 是相当多的人[乐于见到死亡](https://twitter.com/noazark/status/1416076534964756483)的标准。前面提到的大量文章[确实谈到了更多相关的用例](https://notabug.org/niconiconi/vl670/src/usb-b/README.md)，但是，例如，事实证明 USB 3 信号更容易进行电流隔离！

我们已经顺便讨论了 USB 3 和 USB 2 的特性，但是它需要更清楚地建立它的含义。如果你想知道 USB 的其他不为人知的部分，你会想看看我们和凯特·坦金的[黑客 USB 聊天](https://hackaday.com/2020/02/24/hacking-usb-hack-chat/)！