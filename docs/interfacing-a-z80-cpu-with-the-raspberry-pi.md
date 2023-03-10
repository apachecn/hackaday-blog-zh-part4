# Z80 CPU 与 Raspberry Pi 的接口

> 原文：<https://hackaday.com/2021/02/09/interfacing-a-z80-cpu-with-the-raspberry-pi/>

Z80 在 20 世纪 70 年代和 80 年代是一件大事，虽然它不再是今天的主导架构，但它的遗产仍在。[詹姆斯·安德鲁·菲茨约翰]是 Z 的粉丝，他决定将真正的硅与树莓派结合起来，总的来说是为了好玩！

Z80 的地址和数据线以及时钟通过几个 MCP23017 GPIO 扩展器连接到 Raspberry Pi。当然，Pi 的 GPIO 线路并不以速度著称，而且在 I2C 使用扩展器也不是很快。然而，速度并不是必要的，因为时钟只会随着树莓派的意愿而加快，因为它控制着时钟和其他一切。还有一个液晶显示器用于查看 Z80s 的状态，以及一些适合时代的闪光灯。

这种设置允许 Pi 直接在 Z80 上运行代码，同时通过 Python 脚本在自己的内存中管理 CPU 的 RAM。这是一个有趣的技巧，让你在不使用模拟器的情况下在复古芯片上运行复古代码。像这样的技术对于发现处理器的未记录的或边缘情况的性能是有用的。如果这个博客还不足以让你满意，那么也考虑在你的口袋里放一个吧！