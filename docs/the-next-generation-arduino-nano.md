# 下一代 Arduino Nano

> 原文：<https://hackaday.com/2019/10/10/the-next-generation-arduino-nano/>

虽然我们确实喜欢 Arduino Nano 的低成本和多功能性，但无可争议的是，每个工具都有它的缺点。尤其是对一个制造商来说，有足够多的抱怨值得对整个董事会进行重新设计。虽然 Arduino 可能有兴趣也可能没有兴趣将这些变化纳入开发板的重新设计中，但肯定有新制造商介入并改进某些功能的空间。

[ [Kevin Timmerman](https://hackaday.io/oPossum) ]对中国制造的 Nano 的低成本克隆产品进行了研究，强调了一些有趣的关键差异，这些差异使克隆产品——更便宜但仍与传统系统兼容——更具吸引力。

Arduino Nano 的 PCB 制造目前将元件放置在电路板的两面，需要锡膏、取放和回流两个操作。这自然会增加成本，简单地设计一个顶部有元件的两层 PCB 会降低制造成本。

![](img/65e567794383dbf9269ce96670be2abe.png)

自 ATmega328PB 发布以来，它已被证明是比目前 Arduino Nano 和 clones 使用的 MCU atmega 328 p 更好、更便宜的制造 MCU。虽然较新的 MCU 不像其前身那样向后兼容，但它具有额外的 UART、GPIO、计数器和其他功能，允许用户利用新的库和外设。

与 Arduino 板使用的典型电压调节器(用于允许板由 5V 以上的电压源供电)不同，开关调节器允许更少的能量损耗，但元件成本更高。比这两种方法更好的解决方案是干脆不要稳压器。虽然这可能有争议，但这种设计有足够的电池电源(4 节 AA 或 AAA NiMh 电池或一个手机充电器)。

![](img/9913491196c7af58f52ad522a0acab71.png)

Arduino Nano 使用引导加载程序来处理 MCU 编程，这需要将 USB 到串行桥从任何可能干扰编程的地方断开。因此，使用计算机上 COM 端口的程序必须释放该端口，包括串行监视器。除了使用引导加载程序，ICSP(在线串行编程)和 DebugWire 是将 ICSP 引脚连接到 CH551 开发板或通过 reset 引脚编程的可行替代方案。

文章中还建议了许多其他规格和固件改进，以及 Arduino Nano、Arduino Every 和 Chinese 克隆产品之间的比较。绝对值得一看！

The [HackadayPrize2019](https://prize.supplyframe.com) is Sponsored by: [![Supplyframe](img/79a7db035b8a2b6c2b7b0895c45b7de8.png)](https://supplyframe.com/)  [![Digi-Key](img/ba094a14c430ab81591a2abdc54a5363.png)](https://hackaday.io/digikey)  [![Microchip](img/5023ef0b7ff1aee311cba9b54a3ac9fe.png)](https://hackaday.io/microchip)