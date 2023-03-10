# (下一个)情人节的 3D 打印盛开的玫瑰

> 原文：<https://hackaday.com/2019/03/17/a-3d-printed-blooming-rose-for-next-valentines-day/>

灵感按照自己的时间表运行:伟大的想法并不总是及时出现。这就是[达伦·施文克]为他的情人制作一朵 3D 打印盛开的玫瑰的想法，该计划于 2 月 13 日实现。受[【jiří·普劳斯】的动画线框郁金香](https://hackaday.com/2019/02/12/freeform-wire-frame-tulip-blooms-to-the-touch/)的启发，【达人】认为他可以用 rgb leds 着色的清晰印花花瓣制作一朵玫瑰。24 小时似乎很紧，但足够了，所以他努力开始工作，但经过勇敢的努力，最终不得不延长时间表。现在一个多月过去了，对设计的调整仍在继续，但结果是惊人的。

我们首先在 [Hack Chat](https://hackaday.io/messages/room/2369) 上看到了对这个想法的讨论，然后它演变成了 hackaday.io 上的一个项目。在那里，你可以阅读到为实现这个项目而必须忍受的考验和磨难的全部细节。从一台无法启动的打印机，通过测试 PLA、TPU 和尼龙丝，尝试多种不同的弹簧和铰链方法来操作花瓣，并用电磁线连接精致的 DotStar LEDs，您可以很好地感受到完成这样一个项目所需的实验量。如果你知道有人仍然认为 3D 打印像点击一个按钮一样简单，让他们来阅读这个项目的日志。

[![](img/bb4086cee87e6896cfd7a57139dedc25.png)](https://hackaday.com/wp-content/uploads/2019/03/forming-rose-petals.jpg)

An early try at forming PLA petals

最终实现的是普通黑客技术的完美结合。花瓣被印刷在尼龙平面上，然后在炽热的白炽灯泡上成型。茎和叶也有印刷，但侧茎有一段磁线嵌入印刷中，作为电容式触摸传感器；当叶子被触摸时，玫瑰花开或闭。发光二极管的磁线和机械装置的连杆穿过主杆到达底座，在那里 9g 伺服系统负责控制开花。整个事情自然是由 Arduino 控制的。为了更快地推进这个项目，[达人]寻求了另一位黑客聊天高手[Morning]的帮助。Star]，他在不接触实际硬件的情况下，在软件方面做得非常出色。

休息之后，请务必观看玫瑰行动的视频。

 [https://www.youtube.com/embed/91B1UoI4jn8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/91B1UoI4jn8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



我们以前在这些地方看到过盛开的花朵，[包括这个灯](https://hackaday.com/2016/10/11/blooming-flower-lamp-will-test-your-3d-printer/)。