# 教一个 USBasp 程序员说 TPI 语

> 原文：<https://hackaday.com/2021/05/03/teaching-a-usbasp-programmer-to-speak-tpi/>

去年秋天[Kevin]想用他放在实验室里的一个旧 USBasp 编写一些新的 TPI 专用 AVR 程序。发现“奇怪的信息匮乏”和“论坛充斥着不正确的信息和图表”，他决定澄清事实，正确记录事情。他发现了细节，并成功地对 USBasp 进行了重新编程，尽管在这个过程中他最终买了第二个。

使用 AVR 微控制器的设计人员不缺乏编程接口，我们至少有五种不同的方法:ISP/SPI、JTAG、TPI、PDI 和 UPDI。我们不确定这种变化是好是坏，但事实就是如此。[Kevin]发现对于他正在使用的 Attiny 设备的特定系列，the ATtiny20 是唯一可用的选项。

虽然他通常围绕 ARM Cortex-M 芯片进行设计，但[Kevin]需要一些粘合逻辑，并决定采用 ATtiny20，尽管它有独特的编程要求。他注意到去年秋天 ATtiny20 的价格为 0.53 美元，比他需要的同等逻辑门要便宜。这种特殊的芯片也非常小，只有 3 平方毫米(20 针 VQFN)。我们不希望在一块电路板上使用不同的 MCU 和工具链，但有时便利性和经济性会将设计引向那个方向。

如果你不熟悉 USBasp，我们自己的[Mike Szczys]报道了十多年前的突发事件。如果你有很多空闲时间，抛弃所有这些包装精美的解决方案，使用一个旧的 USB 集线器和一个 74HCT00 与非门对你的芯片编程，正如 Teensy 开发者[Paul Stoffregen]在这个奇怪的黑客中描述的[。](https://hackaday.com/2010/06/07/usb-hub-used-for-in-system-programming/)