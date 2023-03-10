# 你现在能听到我吗？农历版

> 原文：<https://hackaday.com/2022/05/16/can-you-hear-me-now-lunar-edition/>

尽管在电影里看起来像什么，但很难与来自地球的宇航员交流。有延迟，太空飞行器通常不会有很多多余的动力。加上一切都在移动，多普勒频移和法拉第旋转。即使在今天，这也很棘手。但是在 1969 年，阿波罗是如何设法发回电视、遥测和声音的呢？[Ken Shirriff]和他的朋友在最近的一篇文章中告诉我们这个故事的一部分，在这篇文章中，他看了看[阿波罗预调制处理器](http://www.righto.com/2022/05/talking-with-moon-inside-apollos.html)。

像重量和体积这样的东西在航天器中总是很重要，动力也是如此。当你看这个超过 14 磅重的固体盒子的照片时，你会惊讶地发现在一个相对小的地方塞进了多少东西。请记住，如果这个盒子是在 1969 年飞行的，它必须更早建造，所以没有办法指望密集的集成电路和现代封装。连印刷电路板都没有。这些部件以点对点的方式连接到金属钉上。整个东西都在指挥舱下层设备舱的底部附近。

处理器，或 PMP，在不同配置中多路复用不同的流并将它们传递到(或从)板载 S 波段发射机中发挥了关键作用。在盒子里，[Ken]找到了四个贴有精美标签的组件，并连接到一个薄背板上。除了分立元件，这些模块还采用了先于 IC 的现成组件，并在一个方便的封装中提供滤波器或振荡器等功能。

使设计更加复杂的一点是需要冗余。例如，里面有两个开关调节器——是的，一个开关调节器在 60 年代的一个齿轮上——船员可以在两个电源之间选择。

[Ken]带我们浏览每个模块。语音和数据检测器模块提取 30 kHz FM 副载波上的语音。还有一个双相调制器、语音剪辑和一个中继模块，用于将信号从登月舱传回地球。

如果你想近距离观察阿波罗通信系统，[CuriousMarc] [有一个关于它的系列](https://hackaday.com/2022/01/21/apollo-comms-flight-hardware-deep-dive/)，并且是该小组的一部分，并拆除了这个 PMP。无线电信号当然很有趣，但最好的镜头还是以胶片的形式出现了。然而，[现代技术已经锐化了一些旧镜头。](https://hackaday.com/2020/07/21/apollo-missions-get-upgraded-video/)