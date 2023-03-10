# 一个 4 美元的超声波特雷门琴故意看起来很俗气

> 原文：<https://hackaday.com/2018/11/10/a-4-ultrasonic-theremin-looks-cheesy-on-purpose/>

当我们说“[穷人的特雷门琴](http://www.bleepbit.com/2018/11/05/the-poor-mans-theremin-arduino-project-ultrasonic-sensor/)”看起来很俗气时，我们不认为【哔哔声】会生气——毕竟，它是在奶酪容器中制造的。事实上，对于一个简单的设备来说，这不是一个坏的情况，正如你在下面的图片和视频中看到的那样。与传统的特雷门琴不同，该设备使用超声波来检测你的手离你有多远，并基于此修改声音。

还有两个按钮——一个关闭声音，另一个循环播放一些效果。不过，我们喜欢它看起来像复古磁带的样子。该设备使用廉价的 Arduino 克隆，但即使有真正的 Arduino，价格也不会太差。然而，所报的价格标签不包括原理图中出现的几个连接器或扬声器。有一点需要注意的是，模型使用了一个插孔而不是一个扬声器，但如果能同时包含两者并使用那种在插入扬声器或耳机时可以断开扬声器的插孔，那就更好了。

代码很简单，有四种可能的效果，你可以用其中一个按钮来循环。与真正的特雷门琴不同，你可以用超声波传感器看到的任何东西来触发它。Arduino 的音频质量当然不是一流的，但它仍然是一个有趣的雨天项目。

我们不禁认为 32 位 Arduino 可能使用了复杂的音频库之一。然而，[即使使用 8 位处理器，也有其他库](https://playground.arduino.cc/Main/LibraryList#Audio)可能会有所改进。

诚然，这不是真正的特雷门琴，但我们也见过很多这样的琴。我们甚至用同样的传感器[来控制电脑](https://hackaday.com/2015/10/07/bootstrapping-motion-input-with-cheap-components/)。

 [https://www.youtube.com/embed/p9VxNfN3M9U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/p9VxNfN3M9U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

