# Arduino 计步器计算您的步数

> 原文：<https://hackaday.com/2020/01/10/arduino-pedometer-counts-your-steps/>

美国企业界有一种趋势，让员工戴上计步器——技术上来说是计步器——然后分组比赛，看谁能走得最多。我们想知道有多少人把这个装置安装在电钻上，并轻松赢得比赛。然而，如果你想自己做测量，[Ashish Choudhary]计划制作一个带有 Arduino 的计步器。这个设备并不小，但正如你在下面的视频中看到的，它似乎是有效的。

对于额外的尺寸，你会得到一些功能。首先，它有一个 16×2 LCD 显示屏和一个 ADXL335 加速度计，你可能会想到这样一个设备的其他一些很酷的功能。

Arduino 会计算加速度的大小，如果超过某个阈值，它会在步数中增加一步。老实说，这是一个有趣的项目，但它迫切需要一个更紧凑的外形。例如，ESP8266 可以摆脱显示器，通过 WiFi 连接到您的手机。话说回来，你的手机可能也能做同样的工作，更不用说许多智能手表了。但是这些都没有这个项目有那么多的极客信誉。

这对仓鼠来说有点大。另一方面，在你数完步数之后，你可以用加速度计做很多事情[。](https://hackaday.com/2016/06/24/taming-robot-arm-jump-with-accelerometers/)

 [https://www.youtube.com/embed/kRySCgWXJnA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/kRySCgWXJnA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

