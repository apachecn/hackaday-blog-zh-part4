# 用 OpenCV 把乐高积木变成音乐

> 原文：<https://hackaday.com/2018/12/30/turning-lego-blocks-into-music-with-opencv/>

我们不知道它是什么，但当谈到 DIY 音乐项目时，乐高和音乐就像牛奶和饼干一样。[保罗·华莱士]的[乐高音乐项目](https://hackaday.io/project/161277)是一个音序器，它使用彩色塑料片来构建和控制声音，但有一个转折。积木没有被扣在任何东西上；该系统完全是可视化的。运行 OpenCV 的计算机使用网络摄像头来观察块的排列，并将它们叠加到虚拟网格上，在虚拟网格中，块的位置被用作序列发生器的输入。Y 轴代表音高，X 轴代表时间。

下面嵌入的是两个视频。第一个演示了音乐如何根据放置的块和位置而变化。第二个是从软件的角度来看，显示视觉系统如何通过挑选彩色块来处理视频，然后使用它们的位置来改变不同的值，从而对整体构图产生影响。

 [https://www.youtube.com/embed/pwH7z06AvMM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/pwH7z06AvMM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/Y4GvLJoY2Ys?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Y4GvLJoY2Ys?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



这个想法的另一种方法见于 [LegoTechno](https://hackaday.com/2014/05/20/turning-lego-into-a-groove-machine/) ，它使用半透明的基板，下面安装了一个摄像头。另一方面，[乐高积木](https://hackaday.com/2016/09/20/lego-looper-makes-modular-music/)走向了一个完全不同的方向，它的设置类似于旋转木马。很明显，给音乐添加一个物理维度和即时反馈是非常有趣的，而乐高似乎是实现这一点的现成组件。

The [HackadayPrize2018](https://hackaday.io/prize) is Sponsored by: [![Microchip](img/20eb9d92b47da4c15177567c02a65727.png)](https://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey)  [![Supplyframe](img/2d012d9fc9c7873688699aeadb4742d2.png)](https://supplyframe.com/)