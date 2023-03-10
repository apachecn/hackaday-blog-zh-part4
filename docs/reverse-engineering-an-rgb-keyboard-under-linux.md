# Linux 下 RGB 键盘的逆向工程

> 原文：<https://hackaday.com/2020/04/14/reverse-engineering-an-rgb-keyboard-under-linux/>

Linux 下的硬件支持比以往任何时候都要好。如今，大多数东西开箱即用，你*可能*不需要编译任何定制的内核模块。与十年前相比，情况当然大不相同。但这并不意味着一切都会发挥出 100%的能力。以[辛西娅·雷夫斯特伦]的鸭子键盘为例。当然，它可以在任何操作系统下作为一个基本的键盘工作，但是[让那些花哨的 RGB LEDs 工作完全是另一回事](https://blog.cynthia.re/post/keyboard-alerts)。

不要误会，[辛西娅]不只是想让键盘随着音乐一起闪烁；目标是使用 Ducky 键盘的 RGB 灯光来发出用户不可能忽略的通知。即使是我们当中最专注于激光的人也很难不注意到整个键盘都在闪烁红光。但是你需要的“DuckyRGB”软件只能在 Windows 上使用，而且显然是通过粗略的 Google Drive 链接发布的。呀。

[![](img/f74b1271f3a6fa5bc53503c6130a57a5.png)](https://hackaday.com/wp-content/uploads/2020/04/duckylinux_detail.png) 创建替代方案的第一步是启动 Windows 虚拟机并安装 DuckyRGB。从那里，Wireshark 可以监听虚拟计算机和 Ducky 键盘之间的内容，以查看软件通过网络发送了什么。在识别出明文发送的版本号后，[Cynthia]能够通过搜索十六进制颜色代码来分离 LED 命令。从那时起，编写一些粘合代码将其连接到警报服务并发出通知就变得相对简单了。

只有一个问题:键盘不再工作了。结果是[Cynthia]编写的控制键盘发光二极管的工具占用了设备，所以内核无法访问它进行正常输入。为了让每个人都能很好地一起玩，HIDAPI 走了一段弯路，现在在 Linux 上改变你的 Ducky 键盘的颜色并不能把它变成一个镇纸。

即使你没有 Ducky 键盘，或者即使你有，也不太想让它的 led 灯向你闪烁，这个项目是实用 USB 逆向工程的一个显著例子。[Cynthia]说这个项目的灵感来自我的朋友[Ben Cox]，[他写了一篇关于创建 USB 用户空间驱动程序的文章，我们去年已经讨论过了](https://hackaday.com/2019/12/30/vga-signal-in-a-browser-window-thanks-to-reverse-engineering/)。如果你有一个旧的 USB 设备，只有 Windows 驱动程序，也许是时候尝试解锁它了。