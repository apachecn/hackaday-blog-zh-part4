# PiFX，Pi 驱动的踏板

> 原文：<https://hackaday.com/2019/05/27/pifx-the-pi-powered-pedal-board/>

自从 Raspberry Pi 开始以来，[tibbbz]就想自己动手制作吉他效果板和放大器模拟器。像这样的设备，以及 Boss 和 Kemper 出售的类似设备，将大量处理能力放在一个金属外壳内，该外壳带有一些脚踏开关和一对 1/4 英寸的输入和输出插孔。捣碎一些按钮，然后从另一端出来。现在这实际上可以用 Pi 来实现，听起来也很棒。

因为这是一个音频应用程序，所以延迟非常关键。当你滚动浏览你的脸书馈送时，如果你有 200 毫秒的延迟，这真的没有关系，但是对于实时音频处理来说，任何超过 5 毫秒的延迟都是令人迷惑的，几乎是不可用的。[tibbbz]使用标准的现成 USB 音频适配器，将延迟降低到大约那个水平。Raspberry Pi 的延迟永远不会像模拟效果踏板中的几个晶体管那么低，但已经足够接近了。

对于音频系统，这一切都是关于[插孔音频:](http://jackaudio.org/)一个 Linux 音频系统的美妙前端。实际的踏板模拟正在用[吉他 ix](https://guitarix.org/) 进行。对于这个构建的硬件部分，除了 USB 声卡和触摸屏显示器之外，这里实际上没有太多东西。脚踏开关是最有趣的，因为它们在重新设计的 USB 键盘控制器板上连接成按钮。这种 USB 键盘的再利用相当有趣，因为它极大地简化了整个构建。所有这些都包裹在一个楔形胡桃木踏板中，这个踏板足够坚固，至少部分时间可以在舞台上使用。[你可以在这里查看演示。](https://soundcloud.com/anthony-tippy-1/pi-fx-guitarix-demo)