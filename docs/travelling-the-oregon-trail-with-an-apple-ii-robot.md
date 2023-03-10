# 带着苹果 II 机器人在俄勒冈小道上旅行

> 原文：<https://hackaday.com/2019/02/18/travelling-the-oregon-trail-with-an-apple-ii-robot/>

出于这样或那样的原因，我们将采用复古的未来 80 年代美学，在这种情况下， [[Mike]决定将苹果 IIe 变成一个机器人。如果你一定要问为什么，你永远不会知道，但这个项目确实有一些有趣的事情。有一个语音合成器，一个全新的电源，它可以在地板上滚动，这要归功于 Apple BASIC。](http://www.mikekohn.net/micro/apple_iie_robot.php)

因为这是一个移动机器人，所以在某个地方需要一个电源。Apple II 有一个很棒的开关电源，但是它用的是市电电压。为了让这款苹果使用 14.8 V 的 LiPO 电池，[Mike]需要重新设计这个电源，以提供+5、+12、-5 和-12 伏的电压。最简单的是正电压，为此，他为+5 V 线路使用了 big 'ol LM1084 线性稳压器。这会产生大量的热量，可能不是最好的解决方案，但这是一个可行的解决方案。+12 线也是另一个线性调节器，LM7812CV。由于这是将 14.8 V 降至 12V，因此效率并没有那么差，而且由于没有软盘驱动器，它无论如何也不会消耗太多电流。负电压是一个 MAX764 / MAX765 反相开关稳压器。这完全取代了 Apple II 中的原始电源，对于任何想制作便携式 Apple II 笔记本电脑的人来说，这是一个不错的参考设计。

为了移动这个东西，马达依靠自己的 11.1 V LiPO 运行，一堆 Pololu 齿轮将所有东西绑在一起。基本代码写在仿真器上[，用](https://github.com/linappleii/linapple)[软盘 Emu](https://www.bigmessowires.com/floppy-emu/) 传输。运动通过操纵杆端口上的输出引脚控制，并且有一个[文本到语音模块](https://www.parallax.com/product/30016)，这显然是需要的，并将这个项目奇妙地联系在一起。你可以看看下面的视频演示。

 [https://www.youtube.com/embed/MPA4GHndOHE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/MPA4GHndOHE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

