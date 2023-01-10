# 万德尔用乐高和树莓皮将废物武器化

> 原文：<https://hackaday.com/2019/05/09/wandel-weaponizes-waste-with-lego-and-a-raspberry-pi/>

在 3D 打印机之前，有乐高。这些小砖块仍然有助于快速组装东西。证据就是 YouTuber [Matthias Wandel]的令人敬畏的[瓶盖射手 build](http://woodgears.ca/lego/shooter_aimer.html)，它使用基本的 DIY 计算机视觉来跟踪你，然后向你发射一连串的塑料片。

这是一个了不起的项目，对每个人都有点意义。让我们从乐高开始。[Matthias Wandel]从制作一个弩设计的发射器开始，他做了一件很棒的工作，用视频向我们展示了它是如何工作的。该机制是一个自动重新加载和发射系统，可以连接到步进电机。接下来是平移和倾斜机制，允许炮塔更好地瞄准移动目标:更多的乐高和步进电机。

目标跟踪器在一个奇怪的不使用 OpenCV 的程序中使用颜色匹配。它比较连续的帧，然后过滤出红色的物体-最大的红点就是它。由于在 Raspbery Pi 相机上使用鱼眼镜头会增加失真，因此[Matthias Wandel]使用更多乐高积木制成的夹具来校准图像。

最后的测试包括让他自己的孩子在房间里走来走去，但是自动机器。孩子们确实喜欢玩具，即使他们试图向他们扔瓶盖。

想要更多乐高灵感？用 ESP8266 检查[乐高四轴飞行器模型](https://hackaday.com/2019/02/10/make-your-lego-fly/)和[乐高坦克。](https://hackaday.com/2018/11/01/mini-lego-technic-tank-patrols-your-desk-under-esp32-control/)

 [https://www.youtube.com/embed/AWhQNQoWo9s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/AWhQNQoWo9s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

