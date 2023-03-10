# Arduino 的电视输出—80 年代风格！

> 原文：<https://hackaday.com/2020/09/11/tv-output-from-arduino-1980s-style/>

我们承认，我们都被宠坏了。现在几块钱就能买到一台在 20 世纪 70 年代末或 80 年代初人人羡慕的电脑。所以毫不奇怪[krallja] [能够使用老式的视频输出芯片来驱动带有 Arduino](https://www.youtube.com/watch?v=QYom_OBcBCY) 的电视。TMS9918A 是一个古老的输出设备，如果旧计算机可以驱动它，那么现代计算机也可以。你可以在下面看到整个实验的视频。

互联网也宠坏了我们，因为几乎任何东西都很容易找到数据表，甚至是这些旧芯片。这种老化芯片的唯一真正问题是，他们通常希望处理器具有数据和地址总线，但大多数微控制器现在都保留了所有这些内部总线。但是有了足够快的 I/O，你可以很好地模拟一辆公共汽车。目前，该实验只是在颜色输出中循环。

试验板上的电路工作正常，即使它看起来不会经受太多的运输。下一步，我们预计将在下一个视频中进行，当然是将数据写入视频 RAM，这样实际的文本就会出现在屏幕上。

我们过去最喜欢的一个项目做了相反的事情:它在 Z80 的地址和数据总线上使用了与设备一样多的 Arduino 设备。我们还看到这种相同的 TI 芯片用于 RC2014 计算机的[图形卡。](https://hackaday.com/2018/06/22/theres-rc2014-life-in-the-tms9918a-display-chip-yet/)

 [https://www.youtube.com/embed/QYom_OBcBCY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/QYom_OBcBCY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

