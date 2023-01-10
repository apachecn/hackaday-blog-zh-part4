# 翻转点示波器棒极了

> 原文：<https://hackaday.com/2021/11/09/flip-dot-oscilloscope-is-flippin-awesome/>

示波器显示器自过去装饰实验室的圆形荧光涂层阴极射线管以来已经有了很大的发展。大多数现代示波器都配有巨大的高清触摸屏，虽然很漂亮，但肯定缺乏经典示波器带来的那种特性。像[bitluni]这样的黑客能够帮助补救这一点是件好事。他的贡献体现在可能是世界上最酷也是最没用的示波器上:一个带翻转点显示的示波器。

是的——一个翻转点显示屏，总之是咔嗒咔嗒，25×16 像素的荣耀。示波器不能触发，它的最大振幅只有几伏，它的刷新率，嗯，是可见的，*但是* *看起来不可思议*。示波器由 ESP32 控制，它读取被测模拟信号。然后，它通过一系列驱动集成电路显示信号，这允许它通过给翻转每个彩色面板的微型电磁铁供电，一次更新一列的点。

更棒的是，[bitluni]直播了整个版本。没错，如果你想看大约 30 个小时的视频，涵盖从[第一次启动显示器上的像素](https://www.youtube.com/watch?v=vQ4dHotO4tg)到[设计和组装 PCB 来驱动它](https://www.youtube.com/watch?v=LcyoqSK7cpk&t=3918s)的所有内容，那么你很幸运。对于我们其他人来说，他做了一个更短的总结视频，你可以在下面看到。当然，这款示波器不会像其他示波器一样[运行*毁灭*，](https://hackaday.com/2018/10/18/playing-doom-on-keysight-oscilloscope-via-windows-ce/)但这可能只是时间问题[。](https://hackaday.com/2018/10/18/playing-doom-on-keysight-oscilloscope-via-windows-ce/)

感谢[赞·阿特金斯]的提示！

 [https://www.youtube.com/embed/8DvH6FiS3sg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/8DvH6FiS3sg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

