# 使用 Arduinos 驱动未记录的显示器

> 原文：<https://hackaday.com/2021/10/04/using-arduinos-to-drive-undocumented-displays/>

对于我们这些年龄足够大的人来说，还记得 VCR(以及编程的困难)，无处不在的真空荧光显示器(VFD)已经深深印在我们的记忆中，主要是因为与表面相似的 LCD 相比，它们的亮度和对比度。尽管除了录像机，这些显示器非常普遍，而且很容易找到它们，几乎不花什么钱，但是如果你只是从一台 30 年前的录像机中拿出来，要弄清楚如何驾驶它是需要一些努力的。在这个版本中，[mircemk]向我们展示了他如何使用 Arduino 驱动未知的 VFD 显示器，以便建立自己的天气预报站。

为了这次演示，[mircemk]决定将一个 VFD 变成一个天气预报站。不过，首先，他必须让 VFD 启动并运行。对于这个来自销售点(POS)终端的单元，只需将电源连接到设备上，就可以打开显示器的演示模式，让他了解一些相关信息。从那时起，凭借对大多数 POS 终端使用 RS232 进行通信的了解，他能够专注于板载微控制器上的 Rx 和 Tx 引脚，并将其与 Arduino 接口。从那以后，他就可以向这个显示器输出任何他想要的东西了。

在这个项目中，[mircemk]希望显示器输出关于天气的信息，但他不是简单地从一些天气 API 中提取数据，而是实际上使用连接到 Arduino 的传感器套件来测量诸如气压之类的东西，以便做出 12 小时的预测。这一设计的灵感来自于旧的 Zambretti 天气预报员，他们使用模拟轮子来输入当地的天气数据。这是一个有趣的构建，不仅对于 VFD 实现，而且对于试图用一个微小的传感器集直接预测天气，而不是下载预测来显示。为了让你自己的预测做得更好，你可能需要自己的气象站。

 [https://www.youtube.com/embed/5c4GLb2gdhI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/5c4GLb2gdhI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/FZi8vyAs57w?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/FZi8vyAs57w?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

