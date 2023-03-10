# 瓶子填充物完美地覆盖在你的杯子上

> 原文：<https://hackaday.com/2021/02/26/bottle-filler-perfectly-tops-your-cup/>

你知道那些学校和机场的灌瓶工吗？如果你家里有一个呢？

我们知道你会说什么:“我的冰箱里有一个！”好吧，我们的没有，即使[克里斯课程的]冰箱有，他选择的瓶子不适合垂直挑战的水和冰的储藏柜，也不能自动填充。解决方案是在他的厨房里建造一个放置可疑，但却很棒的定制灌装机。

这个项目的管道系统再简单不过了:一个 5 年的水槽下滤水器、电子驱动阀、一些管道和一个 T 形接头，以连接到通往冰箱的现有水管。橡胶接触路面的地方让它看起来很漂亮。[克里斯]花了很多时间印刷面板，灌注树脂作为扩散器，以及后期处理。在一种树脂配方失败后，第二种达到了一个漂亮的外观，这个单元经过了大量的打磨、填充、油漆、祈祷，并被批准安装。

对于电子设备，[克里斯]去了一个树莓 Pi 来监控四个按钮，并根据他最喜欢的饮用器皿分配精确的配额。当分配器工作时，三排发光二极管播放动画图案。我们开始挠头的地方是下面的演示，它显示分配器下面没有排水管或滴水盘——看起来像是等待发生的事故。

我们剩下的问题是关于自动化封顶过程。乍一看，你可能想知道为什么没有传感器来自动关闭灌装机。但是这怎么可能呢？分配器需要确定瓶子的高度，这是一项重要的任务，也许最好用计算机视觉[或 CCD 线传感器](https://hackaday.com/2014/01/05/image-sensor-for-filling-wine-bottles/)来完成。你会怎么做？

> 我做了一个自动饮水机，可以把我的水瓶灌到正好的尺寸来自[r/某物制造](http://www.reddit.com/r/somethingimade)