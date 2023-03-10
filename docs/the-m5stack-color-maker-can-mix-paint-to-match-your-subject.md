# M5Stack 制色机可以根据您的主题混合颜料

> 原文：<https://hackaday.com/2021/10/11/the-m5stack-color-maker-can-mix-paint-to-match-your-subject/>

我们在小学美术课上都学过，蓝色和黄色组成绿色，在一种颜色中加入一点黑色会使它变得更暗。但是如果你想用一种和其他颜色完全匹配的颜色来画画呢？通常，这需要大量的试验和错误(和绘画)，最终结果可能不是你想要的样子。

为了帮助有抱负的艺术家，[Airpocket]制作了 [M5Stack 彩色打印机](https://hackaday.io/project/182021-m5stack-color-maker)。这是一种可以读出颜色传感器的设备，它会自动按照正确的比例混合水彩颜料，以匹配它所感测到的内容。它将青色、品红色、黄色和黑色颜料(CMYK)滴到一个小碗中，然后用画笔涂抹。

颜色传感器的使用类似于大多数图形程序中的拾色器(或“滴管”)工具:只需将它指向具有正确颜色的东西，它就会为您生成正确的值。它基于 AMS TCS34725 颜色传感器，该传感器位于 3D 打印的外壳中，该外壳还包括白色 LED。该传感器输出红色、绿色和蓝色(RGB)值，这些值通过 Raspberry Pi Pico 转换为相应的 CMYK 值。触摸屏允许用户在启动涂料泵之前进行调整。

这些泵是管式泵，经过专门设计(也是 3D 打印的)，允许它们移动微量液体，同时最大限度地减少这种类型泵的典型脉冲运动。它们由 Pi Pico 控制的步进电机驱动。

虽然许多艺术家可能更喜欢手动混合他们的颜色，但 M5Stack 使混合精确的蓝色阴影变得更加容易。我们还可以想象它可能会帮助那些色盲和无法清楚区分不同颜色的人。我们已经看到了简单的[颜料混合器](https://hackaday.com/2020/08/31/a-3d-printed-paint-mixer/)用于大量的颜料，甚至还有[机器人可以为你做真正的颜料](https://hackaday.com/2013/11/26/robot-painter-works-like-a-photobooth/)。如果你需要颜色理论的复习，[我们也为你准备了](https://hackaday.com/2018/03/30/color-spaces-the-model-at-the-end-of-the-rainbow/)。

 [https://www.youtube.com/embed/hvE0cxE2VmE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/hvE0cxE2VmE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



The [HackadayPrize2021](https://prize.supplyframe.com) is Sponsored by:[![Digi-Key](img/e7d13a315fd6226594212ca8f8762832.png)](https://www.digikey.com/)[![Supplyframe](img/fdb8a432506edeeafacfef227b3d3b33.png)](https://supplyframe.com/)