# 这张图片是方波发生器

> 原文：<https://hackaday.com/2020/02/08/this-pic-is-a-squarewave-generator/>

当我们使用微控制器来翻转几个 GPIOs 或与外设芯片进行 SPI 对话时，我们经常会忽略它通常包含一系列内置外设，这些外设曾经是额外硬件的专属。模拟端口、定时器、UARTs 和时钟发生器等等。[Giovanni Bernardo]一直在试验其中的一个，许多 PIC 微控制器上的内部频率合成器，他制作了一个方便的方波发生器[，他将代码放在 GitHub](https://github.com/Cyb3rn0id/Microchip_Curiosity_Nano_Examples/tree/master/16F15376_Curiosity_Nano_Square_Wave_Generator.X) 上，并制作了[一篇文章](https://www.settorezero.com/wordpress/un-generatore-di-onda-quadra-da-1hz-a-16mhz-con-un-microcontrollore-pic/)(意大利语，[谷歌翻译链接](https://translate.google.com/translate?sl=auto&tl=en&u=https%3A%2F%2Fwww.settorezero.com%2Fwordpress%2Fun-generatore-di-onda-quadra-da-1hz-a-16mhz-con-un-microcontrollore-pic%2F))。

所用的板是 PIC16F375 Curiosity Nano，代码从旋转编码器接收输入来设置频率，有一个按钮来选择不同的步长，还有一个字母数字 LCD 显示器来显示当前设置。频率范围为 1 Hz 至 15 MHz，两个 PICs 内部时钟之间的巧妙切换将用作参考频率。稳定性取决于 PIC 使用什么样的源作为自己的时钟，虽然我们怀疑这对大多数用户来说已经足够了，但如果有要求，PIC 可以从 GPS 规定的源或类似的源获得时钟也不是不可想象的。

有很多方法可以从微控制器产生方波。[大多数项目使用波形发生器](https://hackaday.com/2018/09/03/arduino-powered-portable-function-generator/)IC。