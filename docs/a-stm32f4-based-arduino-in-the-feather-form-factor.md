# 羽毛外形中基于 STM32F4 的 Arduino

> 原文：<https://hackaday.com/2019/12/01/a-stm32f4-based-arduino-in-the-feather-form-factor/>

[minh7a6]喜欢 Adafruit 羽毛，但看到了一些[改进的空间](https://hackaday.io/project/163853-minhf4-an-stm32f4-arduino-compatible-board)。

首先是 5V 容差的问题。虽然现在 3.3v 范围内几乎什么都有，但有时不必担心也挺好的。羽毛上的主控制器非常强大，但它的不耐引脚就是不行，所以它被换成了曾经流行的 STM32F4 系列的芯片。

然后，他希望在使用电池时有更高的能效。为了实现这一点，他从线性调节器切换到降压升压转换器。他还觉得需要一个单独的 SWD 适配器来进行调试似乎是不必要的，所以他在。

他刚刚完成了对电路板的 Arduino IDE 支持，这很酷。没有打算生产这种加强羽毛，但所有的文件可供任何感兴趣的人。

The [HackadayPrize2019](https://prize.supplyframe.com) is Sponsored by: [![Supplyframe](img/79a7db035b8a2b6c2b7b0895c45b7de8.png)](https://supplyframe.com/)  [![Digi-Key](img/ba094a14c430ab81591a2abdc54a5363.png)](https://hackaday.io/digikey)  [![Microchip](img/5023ef0b7ff1aee311cba9b54a3ac9fe.png)](https://hackaday.io/microchip)