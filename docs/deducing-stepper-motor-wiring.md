# 推导步进电机接线

> 原文：<https://hackaday.com/2019/07/25/deducing-stepper-motor-wiring/>

你可以用从旧打印机或磁盘驱动器中回收的步进电机做很多有趣的项目。然而，并不总是清楚如何连接到一些没有标记或原理图的奇怪电机。[Corvetteguy50]有一个[视频](https://www.youtube.com/watch?v=FYYmuUJyPes)展示了他轻松解决连接的技巧，你可以在下面看到。

基本想法很简单。他使用一种特殊的夹具，将一个 LED 连接到两个随机的引脚上，然后旋转马达。如果 LED 灯亮了，你就找到了一个线圈。你只是还不知道是哪个线圈。你也可以短接两根电线，当你旋转转轴时感觉到阻力时，记下来。

对于某些类型的电机来说，这就有点棘手了，例如那些编码器输出不会驱动电机。其他的有外壳地线。步进器有 4、5、6 或 8 根驱动线，所以如果你有一根以上的驱动线，很可能是地线。

还有其他方法来识别引出线，特别是如果电机有 4 或 6 根线。对于 4 线电机，您可以测量电阻，直到您找到一对读数相对较低的电阻。然后你只需猜测哪个是 A，哪个是 b，如果你猜错了，电机会反转，因为这些都是双极电机。

对于 6 线设备，额外的两根线是中心抽头，5 线电机将两个中心抽头连在一起。测量两根导线之间的电阻应该会给出三个读数中的一个。如果你读一个开路，你是在两个不同的线圈上。如果你读到一个电阻，你可以记录下来，并测量更多的线对。电阻读数将聚集在两个不同的值周围。具有较高值的线对是线圈末端。剩下的两根电线是中间的抽头，你可以通过它们连接到哪一端来判断哪一根是哪一根。当然，在 5 线电机中，你将只剩下一根线。这些电机只能用于单极配置，但 6 线或 8 线电机都可以。

如果你想了解更多关于这类电机的信息，我们已经[讨论了](https://hackaday.com/2011/12/01/an-introduction-to-stepper-motors/)很多年了。[手动控制](https://hackaday.com/2016/03/03/get-really-basic-with-steppers-and-eight-buttons/)一个也很有用。还有步进电机上的经典[琼斯](http://homepage.divms.uiowa.edu/~jones/step/)。

 [https://www.youtube.com/embed/FYYmuUJyPes?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/FYYmuUJyPes?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

