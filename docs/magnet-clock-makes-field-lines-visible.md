# 磁铁时钟使磁力线可见

> 原文：<https://hackaday.com/2022/12/14/magnet-clock-makes-field-lines-visible/>

可视化磁场的传统方法，你的科学老师可能在某个时候演示过，是在一张纸上撒一些铁屑，然后把它放在磁铁上。这是一个有点麻烦的过程，现在有了一种更现代的方法，那就是磁观片。这些工作归功于悬浮在油性介质中的微小镍颗粒，如果你想检查，比如说，DC 电动机的磁场模式，这非常方便。然而[Moritz v. Sivers]对这种神奇的材料有另一个想法，并用它来制作一个[磁铁观察钟](https://hackaday.io/project/188637-magnet-viewing-clock)。

[![A DIY clock, opened up](img/3f2a074d7ca6547d0b85027246c84ab5.png)](https://hackaday.com/wp-content/uploads/2022/12/Magnetic-viewing-clock-inside.jpg) 时钟的前面板看起来很像一个大型单色液晶显示器，但实际上是一大块磁性观看膜。四个磁盘安装在它的后面，每个都带有数字形状的磁性标签，它们被巧妙地隐藏起来。Arduino Uno 通过实时时钟来记录时间，并操作四个步进电机来旋转数字轮。当它们移动到位时，它们的磁性标签透过薄膜变得可见，你可以读出时间。

时钟的机械部件是 3D 打印的，而数字是用乙烯基切割机从一张粘性磁性箔片上切割下来的。如果你想尝试做类似的东西，你很幸运:[Moritz]在他的 GitHub 页面上提供了设计文件和 Arduino 草图。无论如何，磁性观片都是很好的玩物，甚至可以用来阅读[隐藏的信息](https://hackaday.com/2019/04/04/hiding-messages-in-magnets/)。

 [https://www.youtube.com/embed/SXfRbrCcM_Y?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/SXfRbrCcM_Y?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

