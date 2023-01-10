# 3D 打印您的 3D 扫描仪

> 原文：<https://hackaday.com/2020/02/19/3d-print-your-3d-scanner/>

[QLRO]想要一台 3D 扫描仪，但不喜欢任何现有的设计。有些太复杂了。有些很简单，但是需要你手工操作。这让他设计了自己的被他称为 AAScan 的。你可以在下面的视频中看到这个东西在运作。

通常，您可以在对象周围移动相机，或者在相机保持固定的情况下移动对象。本设计选择了后者。你需要一个带驱动板的步进电机和一个 Arduino 来使转盘旋转。你还需要一台运行 Python 和 Meshroom 的电脑。这款手机还必须运行 Python ,( QLRO)在 Android 设备上使用 QPython。

转盘底座背景很疯狂。据推测，这有助于 Meshroom 计算出事物的方向何时改变。我们想知道某种对数标度的网格是否会工作得更好。

[源代码](https://github.com/QLRO/AA-Scan/tree/master)包括两个 Python 文件:一个用于客户机，一个用于服务器。如果你用的是 Windows 而不是 Linux，或者你的 Arduino 没有显示出和他的设置相同的端口，你需要做一些改变。Python 代码出奇的简单。PC 只需通过网络向手机发送字符串“chez ”,并通过串行端口向 Arduino 发送“go”。手机看到那根线并拍照，同时 Arduino 将平台旋转 1/180 圈。如你所料，整个过程重复了 180 次。

手机支架是印刷的，但老实说，它看起来像任何一种铰接式手机三脚架都可以工作。我们甚至可能会尝试用步进电机从纸板上切割出平台，然后就此收工。尽管如此，如果你想做这个，你可能有一台 3D 打印机，那么为什么不使用它呢？

如果你想变得更复杂，你可以试试这个 3D 打印扫描仪。或者，试试 [OpenScan](https://hackaday.com/2019/04/27/this-3d-scanner-is-your-ticket-to-photogrammetry/) 。

 [https://www.youtube.com/embed/ZAbJcA6COqw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ZAbJcA6COqw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

