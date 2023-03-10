# 用微控制器解码 S/PDIF 带来了一些麻烦

> 原文：<https://hackaday.com/2021/04/04/decoding-s-pdif-with-a-microcontroller-brings-a-few-headaches/>

普通玩家定期使用模拟 3.5 毫米电缆、RCA 插孔或蓝牙来分流音频。一个有用的标准是 S/PDIF，代表索尼/菲利普斯数字接口，它并没有真正困扰我们大多数人。这是一种通过铜缆或光纤传输数字音频的有效方式。[Andrew Jeddeloh]在考虑了他家中的一些长电缆线路后，对该标准感到好奇，并决定尝试解码。

[Andrew]开发工作的目标是 STM32L476 Discovery，它没有 SPDIF 解码硬件。相反，[安德鲁]修补外围设备，他必须看看什么会工作。最终，一系列内部定时器以菊花链形式连接起来，允许微控制器从自定时 S/PDIF 信号中恢复时钟。然后用它来产生一个时钟，以同步片上 SPI 硬件，从而从 S/PDIF 信号中实际读入 16 位 PCM 数据。

[Andrew]最初更广泛的计划是将 S/PDIF 数据通过管道传输到板载 I2S DAC，尽管他很难操纵 STM 芯片上的剩余资源来成功做到这一点。任何想要破解的人都可以在 GitHub 上看看[Andrew]的代码。如果完成，STM32L476 将成为 S/PDIF 流的一个有用的模拟端点，允许您远距离数字泵送调谐，而不会出现信号衰减。如果你知道完成这件事的关键，请在评论中发表意见！或者，如果你需要更快地启动和运行，[Teensy 平台已经满足了你！](https://hackaday.com/2015/06/09/teensy-adds-spdif-to-library/)