# 简单而时尚的数字时钟可以显示时间，日期和温度

> 原文：<https://hackaday.com/2021/11/22/simple-but-stylish-numitron-clock-can-display-time-date-and-temperature/>

虽然在制作复古风格的显示器时，谢妮电子管似乎得到了所有的关注，但还有很多其他显示技术可以做出好看的复古设计。以 Numitron 显像管为例:由 RCA 在 20 世纪 70 年代早期推出，这些显像管可能表面上看起来与 Nixies 相似，但工作方式完全不同。Numitron 使用白炽元件组成七段显示器。

与 Nixes 相比，Numitrons 的主要优势在于它们不需要高压电源，这使得它们更容易连接到现代低压电子设备。[mircemk]利用这一点，他用四个数码管制造了一个简单的时钟，可以显示时间、日期和环境温度。

该设备的大脑由 Arduino Nano 和 DS3231 电池供电的实时时钟模块组成。目前，必须通过将 Arduino 连接到 PC 并重新编程来同步时间，但[mircemk]计划用按钮更新设计，允许用户手动设置时间。

由于它们的低电压操作，四个移位寄存器是微控制器与显示管接口所需的全部。它们确实需要相当大的电流，所以[mircemk]使用了高功率的 TPIC6C595，而不是普通的 74HC595 芯片。我们想知道电子管的高功耗是否是他的实验室温度似乎徘徊在 30 摄氏度左右的原因。

一个简单但时尚的塑料外壳完成了设计。由于 Numitron 电子管成本相对较低，不需要其他专门的组件，这可能是制作复古显示电子管时钟最便宜、最简单的方法之一。虽然我们之前已经见过几款 Numitron [时钟](https://hackaday.com/2011/03/13/sleek-numitron-clock-tells-the-time-and-temperature/)甚至[手表](https://hackaday.com/2018/08/16/a-surprisingly-practical-numitron-watch/)，但今天的设计是一个很好的例子，说明了这样的设计实际上可以有多简单。

 [https://www.youtube.com/embed/JyVWJg691L4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/JyVWJg691L4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

