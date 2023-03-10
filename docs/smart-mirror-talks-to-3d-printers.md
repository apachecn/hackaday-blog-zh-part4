# 智能镜子与 3D 打印机对话

> 原文：<https://hackaday.com/2021/07/19/smart-mirror-talks-to-3d-printers/>

随着时间的推移，制作魔镜只会越来越容易。你知道，一面连接到互联网的镜子，可以显示新闻、天气或任何你想要的信息，就在你迷人的脸庞上。在[Forsyth Creations]的案例中，这些数据包括网络上的 3D 打印机活动——这比关于金正恩减肥进展的头条新闻更与日常生活相关。[构建视频嵌入在](https://www.youtube.com/watch?v=miltuOLWDFQ)下方。

[![](img/39e940a08be2a65c59d8f2cbfa4414f5.png)](https://hackaday.com/wp-content/uploads/2021/07/printer-mirror-bracket.jpeg) 多亏了像[【mich】的 MagicMirror](https://github.com/MichMich/MagicMirror) 这样的项目，一切都是用模块完成的，包括真正有用的东西，比如 [OctoMirror](https://github.com/shbatm/octomirror-module) ，它可以让你用 OctoPrint 监视你的 3D 打印机。

这里的电子设备非常简单——[ Forsyth Creations]使用一个旧显示器的内部来显示，并使用一个树莓 Pi 来提供作为网页的模块。唯一棘手的部分是电源，因为 LCD 将需要比 Pi 和边缘周围绝对必要的 led 多得多的电压，但几个降压转换器就可以做到这一点。

在剥离显示器上所有不必要的塑料后，[Forsyth Creations]切割前后框架以支撑电子设备。那不是一块镜子玻璃，它实际上是单向丙烯酸树脂，更轻，也更便宜。[Forsyth Creations]设计并打印了一些角支架，这些支架可以兼作调平螺丝固定器，以使亚克力面板刚好可以拨入，你可以自己从 GitHub 获得这些。我们认为这将是一个很好的早期木工项目或长周末的东西。[Forsyth Creations]用最少的工具在公寓阳台上用三天时间建造了这个。

我们尤其钦佩的是，一旦完成，他用一个法国楔子把它挂起来。那些太有用了。

 [https://www.youtube.com/embed/miltuOLWDFQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/miltuOLWDFQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

