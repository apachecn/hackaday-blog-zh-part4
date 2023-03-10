# 大众 DIY LED 魔方

> 原文：<https://hackaday.com/2021/08/22/diy-led-cube-for-the-masses/>

无论 LED 的大小或形状如何，它都会激发每个硬件爱好者的好奇心，是全球徽章生命的命脉。接下来是 LED 立方体，它将 LED 带到各个方向——毫不夸张。[Tomverbeure]有他自己的冒险经历，通过将 Pixel 钱包和 Cisco3G 调制解调器拼凑在一起，创造了一个 LED 立方体。

在互联网上快速搜索 Pixel 钱包，可以发现一款玩具女士手袋，一侧嵌入了 LED 矩阵。[tomverbeure]拆掉了其中的 12 块，以便为他的作品的每一面提供两块面板。在对 PCB 角支架做了一点点实验后，他终于做对了，他能够将这些部分合并在一起形成立方体。

接下来是大脑和被选中的设备，来自 HWIC 3G CDMA 调制解调器的 FPGA。思科路由器有扩展插槽，这个特殊部件上的 HWIC 连接器有可用的 GPIOs，直接连接到 Altera FPGA。在 FPGA 内部，RISC-V 软 CPU 用于生成图像，并在硬件模块中进行处理和调度。[Tomverbeure]详细解释了用 SpinalHDL 编写的所有模块的实现。下面的视频展示了该项目的实际情况。

我们喜欢[Tomverbeure]提供的细节，希望它不会过分抬高 pixel 钱包的价格。如果你正在寻找一个更精细的立方体，看看这个就知道了。如果你最终制作了自己的，一定要给我们发一个链接。

[https://player.vimeo.com/video/551242661](https://player.vimeo.com/video/551242661)