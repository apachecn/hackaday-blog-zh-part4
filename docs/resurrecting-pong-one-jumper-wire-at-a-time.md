# 复兴 PONG，一次一根跳线

> 原文：<https://hackaday.com/2022/12/14/resurrecting-pong-one-jumper-wire-at-a-time/>

1976 年至 1978 年间，Coleco Telstar 视频游戏机的销量超过 100 万台。让他们如此受欢迎的黑仔应用程序？*乓*。是的，那两个拍子在一个块状的网球场上拍球风靡一时，并帮助开创了一个新时代。正如*戴夫车库*的【戴夫】在[休息](https://www.youtube.com/watch?v=BKkNiic4tzY)下面的视频中向我们展示的那样，让旧游戏机起死回生证明比预期的要简单！

令人欣慰的是，该游戏机是围绕[戴夫]非常恰当地称为“PONG on a chip”的通用仪器 AY-3-8500 构建的，该仪器旨在使游戏机的大规模生产成为可能。该芯片实际上包含了几个游戏，尽管 *PONG* 是 Coleco 上唯一使用的游戏。

[![](img/516c91d70634f760fa47701610d0e5d8.png)](https://hackaday.com/wp-content/uploads/2022/12/pongboard_detail.jpg) 从无法正常工作的控制台上取下 CPU 后，【戴夫】通过提供一个由 Arduino 产生的 2 MHz 时钟信号给它注入了生命。典型的 2N2222 放大音频，快速加电显示芯片正在工作并产生音频。

通过用 4072 或门组合各种信号，视频就像在原始设计中一样得到了巧妙的处理。随着各种视频元素和同步模式组合成一个复合视频信号，[戴夫]能够在屏幕上看到游戏，但后来意识到他需要设计一些“桨”。我们将让您在视频中观看，但请务必查看评论部分以了解有关设计的更多信息。

一个试验板 *PONG* 控制台对你来说不够复古吗？然后看看这个在旧货店被发现的[老派机械版本](https://hackaday.com/2022/03/23/old-school-mechanical-pong-still-amazes/)。

 [https://www.youtube.com/embed/BKkNiic4tzY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/BKkNiic4tzY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

