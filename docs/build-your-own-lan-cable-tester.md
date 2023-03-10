# 建立自己的局域网电缆测试仪

> 原文：<https://hackaday.com/2018/10/10/build-your-own-lan-cable-tester/>

当然，你可以买一个电缆测试仪，但这有什么意思呢？[Ashish]发布了一个好看的[线缆测试器](https://diy-projects4u.blogspot.com/2018/09/diy-lan-cable-tester.html?_sm_au_=iVVHnM6F3ZRkm6MH)，你可以使用或不使用板载 Arduino 来构建它。如果您不使用 Arduino，该项目使用 555 芯片来测试以太网电缆中的八根导线。读数很简单。测试导体时，8 个 led 中的一个将会亮起。如果有一个不亮，说明电缆开路。如果一个以上的灯亮起，则存在短路。混淆的针脚会导致指示灯不按顺序亮起。你可以在下面的视频中看到这个设备。

555 设备很适合这个设计，我们很惊讶这个项目规定 Arduino 只不过是一个脉冲发生器。它可以取代大部分相当简单的电路。一个十进制计数器将脉冲转换成 8 个脉冲(接线的改变使其在第 9 次计数时复位)。电路的其余部分只不过是发光二极管、电阻和二极管。

这是一个很好的例子，说明了几个简单的组件可以一起做一些有意义的事情。使用 Arduino 创建 8 或 9 个输出脉冲，然后对其进行测量，这很有吸引力，但对于小型 Arduino 来说，这将需要大量的 I/O。不过，您可以观察模拟输入的返回，这样可能会进一步完善电路。甚至还有一个优点是允许对每个引脚进行更详细的分析。

然而，这样的奇思妙想远没有那么简单，这首先是一个简单而愉快的项目。当然，它不会取代价值 12，000 美元的电缆测试器，但也没必要。另一个对电缆测试有用的简单电路(如果不算示波器的话)是一个[时域反射仪](https://hackaday.com/2015/07/27/hackers-measure-cable-lengths-with-time-domain-reflectometers/)。

 [https://www.youtube.com/embed/PSK5Aa-byHA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/PSK5Aa-byHA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

