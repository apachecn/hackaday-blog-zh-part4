# 直接从卫星上获取天气图像

> 原文：<https://hackaday.com/2020/03/14/get-your-weather-images-straight-from-the-satellite/>

[Josh]有一个叫做业余无线电速成班的系列节目，最近的一期节目讲述了如何直接从气象卫星获取[卫星图像。由于软件定义无线电(SDR)，这在过去比现在更具生产性。乔希还有另一个项目，利用](https://www.youtube.com/watch?v=PWWGDL5tC_I)[的 3D 打印机制作适合这项工作的天线](https://www.thingiverse.com/thing:3665516)。你可以看下面的视频。

该软件是古老的 WXtoImg 程序。这是一个废弃的软件，但是社区仍然保留了这个软件。该程序可以在 Linux、Windows 和 Mac 上运行。讨论中的卫星运行在 137 MHz 左右，但这很容易在即使是便宜的 SDR 加密狗的范围内。[Josh]展示了如何在 Windows 上使用虚拟音频电缆将收音机的输出连接到 WXtoImg 程序的输入。在 Linux 下，你可以用 Pulse 或 Jack 非常容易地做到这一点，不需要任何额外的硬件。

这个软件需要一些设置和校准。你还需要当前的轨道数据，程序会告诉你什么时候可以找到下一颗经过头顶的卫星。一般来说，你会希望你的天线在外面，这一点[Josh]通过把所有东西都带到户外并在传递期间吃点午餐来解决。将数据后处理成图像和音频也需要一些时间。

我们知道[这不是新的](https://hackaday.com/2015/08/02/downloading-satellite-images-via-fm-radio/)。但我们确实喜欢(乔希的)清晰和最新的指南。我们记得看着 [NOAA 15](https://hackaday.com/2019/08/12/the-death-of-a-weather-satellite-as-seen-by-sdr/) 开始失去它的电子思维。

 [https://www.youtube.com/embed/PWWGDL5tC_I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/PWWGDL5tC_I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

