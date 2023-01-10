# 基于函数发生器的 USB 协议逆向工程

> 原文：<https://hackaday.com/2021/02/09/reverse-engineering-usb-protocols-on-a-function-generator/>

当使用示波器和信号发生器等测试设备时，截屏会很有用。历史上，这是通过螺栓固定的宝丽来相机来完成的，但现在可以通过简单的 USB 连接来完成。[Majenko]不喜欢他们的天马 72-14110 函数发生器附带的 Windows 专用软件，但是，[开始对 USB 协议进行逆向工程来创建他们自己的软件。](https://majenko.co.uk/blog/hacking-tenma-72-14110-functionarbitrary-waveform-generator-usb-protocol)

黑客是通过在 Windows 虚拟机中运行原始软件，同时在主机 Linux 操作系统中运行 Wireshark 来捕获 USB 流量的。一旦捕获了足够的数据，[Majenko]就开始计算函数发生器在将屏幕数据发送到 PC 时是如何格式化屏幕数据的。基于数据长度根据显示器上的内容而变化的事实，推测数据不是原始的，而是以某种方式压缩的。直觉表明这可能是某种形式的游程编码，这被证明是正确的。通过更多的挖掘和实验，[Majenko]能够将一些代码组合在一起，从设备中捕捉到清晰的图像。

这是对图像数据进行逆向工程的有用指南，如果您在其他硬件上处理类似的问题，它可能会很有用。这些年来，我们已经看到了一些伟大的逆向工程努力，从旧视频硬件到 T2 世嘉土星。[如果你自己一直在深入研究软件或硬件的秘密，一定要给我们写信。](http://hackaday.com/submit-a-tip)