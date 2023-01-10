# 特别提款权传输获得权力

> 原文：<https://hackaday.com/2020/08/29/sdr-transmitting-gets-the-power/>

大多数业余爱好级软件定义的无线电设置不传输。在少数几个这样做的国家中，大多数都发出大约 1 毫瓦的微弱水平。如果你想在实验室之外做一些事情，你需要一个放大器，这就是[Tech Minds] [在最近的视频](https://www.youtube.com/watch?v=yOkdg1lGfes&feature=emb_logo)中展示的方法。(嵌在下面。)

视频涵盖了 LimeSDR、HackRF 和 Pluto SDR，但放大器应该可以与任何发射机配合使用。SPF5189Z 模块非常便宜，覆盖 50 MHz 至 4 GHz，放大你扔给它的一切。缺点是，它会放大你扔给它的一切，甚至是你不想要的信号部分，如杂散和谐波。

根据您的需求，还有其他模块。CN0417 的覆盖范围非常窄，从 2.4 GHz 到 2.5 GHz。(如果可以称 100 MHz 带宽为“窄”。)RF2126 将覆盖 400 Mhz 至 2.7 GHz 的频率范围。

这些都不是强国。最大 20 dB 增益只能为您提供 1 瓦左右的功率，而大多数 SDR 发射机的驱动力最小。但是对于很多应用来说，这已经足够了，特别是在进行一些过滤的情况下。

不幸的是，增益不稳定，我们想知道会影响某些调制模式的线性度。周围有这些器件的数据手册，比如这份关于 [SPF5189Z](https://www.qorvo.com/products/d/da001910) 的数据手册。

如果你真的对 SDR 感兴趣，SDR 学院今年虚拟化了。你可能也会喜欢[这本书](https://hackaday.com/2018/06/29/free-e-book-software-defined-radio-for-engineers/)。

 [https://www.youtube.com/embed/yOkdg1lGfes?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/yOkdg1lGfes?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

