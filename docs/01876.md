# DIY 拍板是 20 世纪 80 年代的风格，带有树莓派图案

> 原文：<https://hackaday.com/2019/01/18/diy-clapper-is-1980s-style-with-raspberry-pi-twist/>

家庭自动化并不是什么新鲜事。它只是更加进化了。许多年前，出现了一种叫做 Clapper 的电视产品。如果你没听说过，那基本上是一个声控交流开关。比方说，你把一盏灯插入设备，把拍板插入墙壁，然后你就可以通过拍板打开或关闭灯。如果你不知何故错过了这些——显然你仍然可以得到它们——看看下面视频中 1984 年的广告。[Ash]决定放弃在亚马逊上订购一个，而是用树莓派自己做了一个。

[Ash]的原型使用 LED，理论上可以驱动任何东西。如果你想更换真正的铃锤，你需要一个继电器或其他适合负载的交流开关。实际的拍手检测软件来自[nikhiljohn10]并简单地等待两声巨响。没有花哨的机器学习来区分拍手和打翻花瓶的猫。只是一个门槛和一些时机。

当然，除非您添加麦克风，否则 Pi 听不到任何声音。然而，添加一个 USB 麦克风是很容易的，因为 Linux 内核会很容易地处理它。`pyaudio`库给你一个代码和麦克风之间的接口。

我们认为，由于整个事情是一个脚本，它会很容易也提供一些音频反馈。就此而言，您可以通过电子邮件来监控状态。提供一些其他界面——比如网页——也可以打开和关闭负载，这可能会很有趣。或者对两次、三次或四次拍手做出不同的反应。有很多可能性。

如果你想知道真正的响板是如何工作的，看看这个就知道了。如果你想看超级拍板，就去 [Hackaday.io](https://hackaday.com/2018/07/13/give-the-clapper-a-hand/) 。

 [https://www.youtube.com/embed/MTNuJXi6UUk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/MTNuJXi6UUk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

