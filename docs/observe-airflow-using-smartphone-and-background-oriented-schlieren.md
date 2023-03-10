# 使用智能手机和面向背景的纹影观察气流

> 原文：<https://hackaday.com/2022/07/17/observe-airflow-using-smartphone-and-background-oriented-schlieren/>

最近，许多人与我们分享了这个激动人心的演示([nitter](https://nitter.net/kambara/status/1546830410021146626))——使用智能手机可视化气流，称为“面向背景的纹影”。在炎热的夏天，[你可能会看到空气中的波动](https://eu.pressconnects.com/story/news/local/2016/05/19/why-do-we-see-waves-hot-objects/84598570/)——这是由于空气变暖时密度发生变化，从而对光线产生不同的折射。[纹影摄影](https://en.wikipedia.org/wiki/Schlieren_photography)是一套用于可视化流体流动的通用技术，但当然，它也可以应用于气流。在这种情况下，使用一些聪明的光学识别技巧，这种纹影方法可以让你只使用 Android 智能手机的高分辨率摄像头和已知图案的打印背景来可视化空气流动！

这个技巧背后的科学论文很好地描述了这种方法的工作原理——推荐查阅。简单来说，由于背景是高对比度的，并且为智能手机应用程序所知，因此您可以放大相机预期看到的和相机看到的之间的差异——角落中的 datamatrix 代码可以帮助智能手机识别背景图像的位置，以便进行更精确的映射。热空气和[冷空气流](https://mobile.twitter.com/kambara/status/1546832554925314048)在视觉上是最明显的，不清楚有多少常规气流会被注意到。然而，[Android 应用源代码](https://github.com/kambara/air-visualizer)和[可打印模式](https://github.com/kambara/air-visualizer-background/tree/master/images)在 GitHub 上是免费提供的——你可以试试这个方法，看看效果如何！

这是一个非常好的执行和可访问的黑客，我们想知道我们的黑客同伴会把它用于什么目的。在某种程度上，这是一个穷人的气流目的的热感相机！几年前，我们报道过一个基于镜子的纹影设置，也是使用智能手机。也许这些无处不在的高分辨率相机设备可以比我们意识到的更有用！

> 试着制作了只通过智能手机的照相机就能看到空气流动的 APP。 [pic.twitter.com/XaQ7lgmVJ1](https://t.co/XaQ7lgmVJ1)
> 
> —神原(@神原)[2022 年 7 月 12 日](https://twitter.com/kambara/status/1546830410021146626?ref_src=twsrc%5Etfw)