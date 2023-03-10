# 使用 TL494 的等离子扬声器

> 原文：<https://hackaday.com/2018/08/05/a-plasma-speaker-using-a-tl494/>

我们习惯于将扬声器作为圆形组件，带有一个纸盆和一个大磁铁，磁铁内部悬挂着一个连接到音频放大器的线圈。但是动圈扬声器并不是用电创造声音的唯一方式，音频设计师的武器库中还有一两种其他的武器。

其中一个更引人注目和有趣的是等离子扬声器，这是[Marcin Wachowiak]一直在试验的。两个电极之间放电形式的连续等离子体被音频信号调制，等离子体体积的快速变化产生了声音。等离子扬声器的价值在于产生声音的元件的尺寸和质量非常小，这意味着虽然它只能有效地再现高频，但它比其他类型的高音扬声器更接近点声源。由于这个原因，它受到一些音响发烧友的喜爱，你会在高端音频市场发现一些商业化生产的等离子高音扬声器。

[Marcin]不是为了听音癖，相反，他对等离子体的特性感兴趣。他的等离子扬声器确实做得很好，特别是他在驱动电路的设计上花了很多心思。其核心是无处不在的 TL494 PWM 控制器，您可能更熟悉开关电源，该控制器将音频驱动作为 PWM 应用于 MOSFET 的栅极，开关反激式变压器的初级线圈。他增加了一些改进，比如栅极放电电路和带有续流二极管的第二个初级绕组。

结果是一个有效的等离子扬声器。很难从他的 YouTube 视频中判断他是否达到了发烧友的纯度，但幸运的是这不是重点。我们已经向你展示了我们这个时代的一些其他等离子扬声器，如果你对这个主题感兴趣，那么看看这个[旋转等离子涡旋](https://hackaday.com/2016/04/12/rotating-plasma-vortex-speaker/)，或者[一个使用 555 定时器的版本](https://hackaday.com/2016/03/27/555-plasma-speaker/)。

 [https://www.youtube.com/embed/LLL9y9h0Qw0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/LLL9y9h0Qw0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

