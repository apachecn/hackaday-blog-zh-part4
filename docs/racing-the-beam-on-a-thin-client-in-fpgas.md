# 在 FPGAs 中的瘦客户机上运行光束

> 原文：<https://hackaday.com/2018/12/07/racing-the-beam-on-a-thin-client-in-fpgas/>

几年前，一家名为 Pano Logic 的公司推出了一系列基于 FPGA 的瘦客户端。可悲的是，市场并没有出现，这些股票的大部分最终在易贝，最终被急切的黑客抢购一空。[[Tom]就是这些黑客中的一员，他决定用硬件尝试一些光线追踪实验。](https://tomverbeure.github.io/rtl/2018/11/26/Racing-the-Beam-Ray-Tracer.html)

[Tom]拥有早期的 Pano Logic 客户端，具有 VGA 输出和 Xilinx Spartan-3E 1600 FPGA。由于 FPGA 中的 RAM 有限，并且希望避免为板上的存储器编写定制的 d RAM 控制器，因此没有空间容纳帧缓冲区。相反，人们决定光线跟踪器将改为“与光束赛跑”——快速计算每个像素，超过显示器的刷新率。

这种方法意味着资源管理是关键，而且[Tom]指出，即使对光线跟踪环境看似微小的改变也需要极大地增加计算量。简单地添加一个阴影和方向灯就可以将核心逻辑利用率从 66%提高到 92%！

虽然该项目可能不可扩展，但[Tom]能够实现经典的反射球，它在棋盘上反弹，甚至通过板载 CPU 内核添加了一些相机运动来活跃气氛。这是一个关于如何在 FPGA 平台上利用有限资源的实际演练。如果你想深入了解一下，可以在 Github 上找到代码。

如果您是 FPGA 新手，[为什么不参加我们的 FPGA 训练营呢？](https://hackaday.com/2018/08/06/learn-fpga-fast-with-hackadays-fpga-boot-camp/)