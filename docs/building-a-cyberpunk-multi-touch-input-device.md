# 构建赛博朋克多点触摸输入设备

> 原文：<https://hackaday.com/2019/10/06/building-a-cyberpunk-multi-touch-input-device/>

这款由[thiagesh D] 打造的[多点触控触摸面板可能看起来像是来自于*银翼杀手*或*外星人*的复古未来世界，但由于详细的制作视频和相当短的所需部件列表，它可能是你的下一个周末项目。](https://hackaday.io/project/167866-led-touch-matrix-raspberry-pi)

[![](img/cd7d57d1c48492343c2577285263377b.png)](https://hackaday.com/wp-content/uploads/2019/10/touchpanel_detail.jpg) 这个建筑始于一张亚克力板，上面刻有网格图案，使用的工具无非是一把刀和一把尺子。不过，如果你*有某种数控路由器，这将是一个完美的时间来打破它。然后将裸线放入凹槽内，用 CA 胶固定，焊接在一起，形成一个大的导电阵列。这是附在一个电容传感器模块上的，所以只要有人把手指放在塑料上，它就会启动。*

 *通过在边缘添加 RGB LED 条，您可以在这里停下来，拥有一个看起来非常酷的照明触摸感应面板。但最终，它只是一个美化了的按钮。这样一个小玩意有很多有趣的应用，但是把它附加到你的电脑上就没什么用了。

为了将它变成一个可行的输入设备，[thiagesh D]正在使用一个 Raspberry Pi 及其相机模块，通过 Python 和 OpenCV 从丙烯酸树脂的另一侧跟踪指尖的数量和位置。他的代码甚至可以识别特定的手势，比如在下面的视频中，三个手指的拖动会相应地改变 led 的颜色。不幸的是，相机的视野意味着面板安装的盒子必须相当深，但如果凹进桌子的表面，我们认为它可能看起来不可思议。

定制多点触控面板多年来一直是黑客们最喜欢的项目，我们已经有了可以追溯到过去黑白时代的例子。但是像这样的[更大更现代的化身](https://hackaday.com/2017/11/04/diy-multi-touch-all-the-surfaces/)有潜力[改变我们日常与科技的互动方式](https://hackaday.com/2010/12/03/benddesk-multi-touch-furniture/)。

 [https://www.youtube.com/embed/uB6KFTe89AM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/uB6KFTe89AM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

*