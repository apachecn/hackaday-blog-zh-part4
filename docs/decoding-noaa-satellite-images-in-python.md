# 用 Python 解码 NOAA 卫星图像

> 原文：<https://hackaday.com/2021/01/27/decoding-noaa-satellite-images-in-python/>

如果你认为从轨道卫星接收数据传输需要一系列复杂的硬件和软件，这是情有可原的，因为很长一段时间以来确实如此。这些天来，我们受益于廉价的软件无线电(SDR ),让我们的计算机可以轻松调谐到任意频率。但是软件方面呢？正如[Dmitrii Eliuseev]所示，[解码卫星向地球发射的数据可能比你想象的要容易得多](https://medium.com/swlh/decoding-noaa-satellite-images-using-50-lines-of-code-3c5d1d0a08da)。

至少在这种情况下。这些数据碰巧是由美国国家海洋和大气管理局(NOAA)运营的一个相对较老的卫星群广播的。这些鸟(NOAA-15、NOAA-18 和 NOAA-19)有些独特，因为它们飞得相当低，并利用以 137 MHz 传输的简单模拟信号。这使它们成为那些刚刚涉足卫星接收领域的爱好者的特别好的目标。

[Dmitrii]在这篇文章中没有花太多时间谈论硬件，只是说他使用的 SDRPlay 的天线很差。他提供了一个关于制造更合适的天线的信息链接，但信号足够强，一副旧的“兔子耳朵”在必要时也能派上用场。在那里，他讲述了如何预测 NOAA 的一只鸟何时会从头顶飞过，并解释了如何配置 SDR 软件来捕捉产生的信号。从那以后，这是一个如何理解录制的 WAV 文件的逐步指南。

[![](img/a5ff0d4e09875f5eaed7dac3770ea531.png)](https://hackaday.com/wp-content/uploads/2021/01/noaacode_detail.png)

在`scipy`库的帮助下，加载 WAV 文件并在其中生成一些信号的可视化非常容易。因为它是模拟的，所以只需要用 Python 图像库(PIL)多做一点工作就可以将其转换成 2D 图像。[Dmitrii]指出使用`putpixel`函数并不是最有效的方法，并给出了一些关于如何大大加快这个过程的技巧，但是为了演示的目的，它使代码更容易理解。

当然，已经有[个成熟的软件包为你解码这个数据](https://hackaday.com/2020/03/14/get-your-weather-images-straight-from-the-satellite/)。但是你自己做还是有好处的，特别是因为这些 NOAA 卫星不会永远存在。取代它们的新卫星肯定会使用更复杂的协议，所以如果你想尝试这种独特的编程练习，那么[的时钟正在滴答作响。](https://hackaday.com/2019/08/12/the-death-of-a-weather-satellite-as-seen-by-sdr/)