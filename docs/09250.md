# Raspberry Pi RP2040 微控制器上的位碰撞 DVI

> 原文：<https://hackaday.com/2021/02/12/bitbanged-dvi-on-a-raspberry-pi-rp2040-microcontroller/>

当我们上个月第一次看到 Raspberry Pi Pico 及其 RP2040 微控制器时，很明显，它不仅仅是又一个 ARM 芯片，它需要一些特殊的东西，这似乎是以其板载 PIO 外设的形式出现的。我们急切地等待社区如何使用它们来推动 RP2040 功能超越其宣传的极限。现在[Luke Wren]为我们提供了一个例子，[他推动 RP2040 产生适合驱动 HDMI 监视器的 DVI 信号](https://github.com/Wren6991/picodvi)。

芯片可以超频并不奇怪，但是令人印象深刻的是，它可以达到产生 DVI 时序所需的 252 MHz。使用适当的终端，GPIO 线路可以模拟规范要求的差分信号。创建了一个带有 RP2040 和 HDMI 插座的 PCB，还提供了几个用于扩展的 PMOD 连接器。所有代码和软件都可以在 GitHub 库中找到。

结果是一个可用的 DVI 输出，虽然它是一个相对较低的分辨率 640×480 像素，60 Hz，仍然是一个重大进步，超过了微控制器项目通常提供的复合视频。随着显示器上的复合支持成为一个传统项目，看到一条无需使用 FPGA 的 HDMI 或 DVI 输出的可访问路径是一个受欢迎的景象。

感谢[BaldPower]的提示。