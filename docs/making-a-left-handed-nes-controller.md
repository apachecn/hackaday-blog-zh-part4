# 制作左手 NES 控制器

> 原文：<https://hackaday.com/2021/08/10/making-a-left-handed-nes-controller/>

最初的任天堂娱乐系统的控制器是一个经典，但也许不是因为它坚持良好的人体工程学原则而闻名。不管怎样，长时间使用它会变得很笨拙。为了帮助缓解这种情况， [[Taylor]发明了一种简单的方法将 NES 控制器转换成左手操作。](https://hackaday.io/project/181146-making-a-left-handed-nes-controller)

![](img/fe21a8583450d68fe4fd5113fa51c8d2.png)

The mod board in question, installed on a NES controller PCB.

黑客的关键很简单，控制器的按钮从左到右交换，使控制器能够上下翻转。在这个方向上，右手使用 D-pad，左手使用操作按钮，与通常的方式相反。因此，D-pad 上的左和右必须交换，A 和 B 也是如此，所以所有的控件都处于逻辑布局中。

这是通过使用[泰勒]自己设计的小 mod 板实现的。原来的 HD14021BP 芯片从控制器的 PCB 上拆下，安装在 mod 板上。然后，可以将 modboard 焊接回控制器，重新布线以交换按钮。还有一个[泰勒]设计的版本，由于一些板载 DIP 开关，可以在右手和左手操作之间翻转。

这是一个干净利落的黑客技术，可以拯救一些狂热的俄罗斯方块玩家。或者，你可以从头开始制作你自己的 NES 控制器。休息后的视频。

 [https://www.youtube.com/embed/6M1fuRN6ixw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=702&wmode=transparent](https://www.youtube.com/embed/6M1fuRN6ixw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=702&wmode=transparent)

