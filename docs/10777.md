# 提取 WiFi 固件并放回键盘记录器

> 原文：<https://hackaday.com/2021/07/20/extracting-the-wifi-firmware-and-putting-back-a-keylogger/>

出于简化或抽象的考虑，我们喜欢将餐桌上的笔记本电脑视为一个独立的处理单元。事实上，除了构成处理器的众多内核之外，还有数量惊人的小型处理器。[8051 爱好者]潜入他笔记本电脑上的 [Realtek rtl8821ae WiFi 芯片，提取固件](https://8051enthusiast.github.io/2021/07/05/002-wifi_fun.html)。Realtek rtl8821ae 芯片是一个相当标准的 Realtek 芯片[，正如在这个拆箱](https://www.youtube.com/watch?v=no1wF5FJp6Y)中看到的那样(这是主图像的来源)。

果然不出所料，[8051 热情者]很高兴地发现 rtl8821ae 显然是基于英特尔 8051 的。固件在启动时从已知的文件路径加载，并加载到位于 M.2 插槽中的芯片上。仔细考虑，[8051enthusiast]推断固件使用的是 RTX51 Tiny，这是一个小型实时内核。

固件在 0x4000 加载，但它调用该地址下的代码，这意味着芯片上有一个包含一些代码的 ROM。提取它的最简单方法是编写一些自定义代码，通过共享内存映射配置空间将屏蔽 ROM 复制回主 CPU，但固件会被屏蔽 ROM 代码校验和。然而，校验和只是一个 16 位的异或运算。随着内核允许从用户空间访问共享配置空间的调整，[8051enthusiast]正在走向一个完整的固件映像。

[![](img/b089602eaa1015a6f0a8c6401691bf22.png)](https://hackaday.com/wp-content/uploads/2021/07/8051enthusiast-laptop-ec-board-diagram_had.jpg)

接下来，[8051 热情者]看看他新发现的黑客能力可以做些什么。键盘矩阵由嵌入式控制器(EC)读取，嵌入式控制器恰好是另一个基于 8051 的微控制器。从 EC 到 m.2 插槽(rtl8821ae 所在的位置)恰好还有一条 RX 和 TX 走线。这与来自处理器的 0x80 邮政编码通过 EC 被路由到某个可访问的地方有关。由于在 EC 和 WiFi 芯片上都有一些定制代码，[8051enthusiast]有一个键盘记录器，它不在主处理器上运行，将 PS/2 击键作为 UDP 包进行广播。

当然，还有许多其他基于 8051 的设备正等着被发现。像这个[基于 8051 的电子墨水显示控制器](https://hackaday.com/2021/05/15/reverse-engineering-an-unknown-microcontroller-in-e-ink-displays/)。

[主要图片来源:Realtek RTL8821AE 在 YouTube 上由[евгенийгорохов](https://www.youtube.com/watch?v=no1wF5FJp6Y)]