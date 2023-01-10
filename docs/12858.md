# 真空压力表

> 原文：<https://hackaday.com/2022/02/23/pressure-gauge-built-in-a-vacuum/>

需要可能是所有发明之母，但我们经常发现，这里的发明往往是由昂贵的现成零件驱动的，而且人们不愿意花高价购买它们。我们经常发现人们自己制造工具或零件，好像这些高价格是一个挑战，而不是简单地耸耸肩，从供应商那里订购。最近接受自己制造零件挑战的人是【高级修补】[，他需要一个真空室专用压力计](https://www.youtube.com/watch?v=34ZAHMwtuhs)。

在这种特定情况下，传感器本身的价格并不太高，但它的控制器是交易的破坏者，因此，一旦获得传感器，就可以使用可靠的 Arduino 定制仪表。该器件使用外部模数转换器与 16 位分辨率的传感器接口，并使用一些电路将传感器的约 8 V 输出降至微控制器所需的 5 V。[高级修补]也想要一个定制的实时读数，所以建立了一个 3D 打印外壳，包括一个压力的 LCD 读数和一个压力随时间变化的图表屏幕。

对于其他任何在真空室中进行敏感压力测量的人来说，【高级修补】使[项目代码在 GitHub 页面](https://github.com/AdvancedTinkering/Pirani-vacuum-gauge-)上可用。如果你有时间定制的话，这是一个很好的解决方案。不过，如果你在寻找不那么精致的东西，[看看这个不用电池的压力传感器，它可以骑在自行车轮子上](https://hackaday.com/tag/tire-pressure-sensor/)。

 [https://www.youtube.com/embed/34ZAHMwtuhs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/34ZAHMwtuhs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

