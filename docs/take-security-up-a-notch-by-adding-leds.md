# 通过添加 led，将安全性提升一个档次

> 原文：<https://hackaday.com/2020/01/12/take-security-up-a-notch-by-adding-leds/>

所有的计算机都容易受到病毒或黑帽的攻击，但是可以采取许多措施来降低风险。最极端的情况是拥有一台根本不连接网络的“空气间隙”计算机，但这并不能保证它不会受到攻击。在某些情况下，甚至用 USB 驱动器将文件传输到计算机也有风险，但多亏了[罗伯特·菲斯克]驱动器上的一些 LED 灯，这种攻击媒介至少可以被监控到。

使用带有单个 LED 的 USB 驱动器在读取或写入操作期间发光是相当常见的，但由于有可能在不知不觉中通过 USB 驱动器传输恶意软件，具有专门用于写入操作的单独 LED 的 USB 驱动器将有助于提醒用户任何可能试图在雷达下飞行的写入操作。[【Bruce Schneier】](https://www.schneier.com/blog/archives/2013/10/air_gaps.html)最近的一篇文章指出了 USB 驱动器的这一缺陷，【Robert】接受了挑战。他的构建通过向用户显示他们的驱动器何时被访问以及以何种方式被访问，将更多的控制权归还给用户，这也可以用于发现用户所选操作系统的独特之处。

[Robert]对 USB 驱动器及其起伏非常熟悉。几年前，他建造了一个 [USB 防火墙](https://hackaday.com/2017/03/02/good-usb-protecting-your-ports-with-two-microcontrollers/),能够降低 BadUSB 类型攻击的可能性。不过，进入设备安全的兔子洞时要小心，否则你会发现潜在的攻击[隐藏在几乎所有地方](https://hackaday.com/2015/01/14/keystroke-sniffer-hides-as-a-wall-wart-is-scary/)。