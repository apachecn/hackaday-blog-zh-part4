# Leap Motion 无需手套即可控制双手

> 原文：<https://hackaday.com/2021/05/08/leap-motion-controls-hands-with-no-glove/>

用手套手动控制机器人来模仿用户的动作并不少见。[所有零件组合]有不同的方法。使用跳跃动作控制器，他可以在不戴手套的情况下录制手部动作，然后随意回放给机器人手。你可以在下面的视频中看到这个项目。

这个项目看起来足够简单，但是显然，Leap 文档不是最好的。不过，既然他解决了这个问题，你可能会发现[代码很有用](https://github.com/AllPartsCombined/Leap-Animatronic-Hand)。

一个 8266 运行一切，虽然你可能会得到更少。Leap 提供的数据比手的伺服系统提供的数据多，所以需要进行一些算法开发。

我们收集了一些关于使用加热乙烯管制造柔性手指的技巧。永远不知道什么时候会派上用场——没有双关语的意思。纸板结构不会很漂亮，但手套套很好用。你也可以 3D 打印一些东西。

Unity 应用程序将实时驱动手部，或者可以播放五个录制的套路中的一个。您可以看到录像和回放是如何工作的。

这让我们想起了另一个[机器人手](https://hackaday.com/2015/10/22/leap-motion-wirelessly-controlling-a-prosthetic-hand-with-an-arduino/)项目，这个是 3D 打印的。我们以前也见过[更传统的机械臂](https://hackaday.com/2018/10/01/the-leap-motion-makes-robots-bend-to-your-will/)跳跃移动。

 [https://www.youtube.com/embed/WQq8XFl_ZAI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/WQq8XFl_ZAI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

