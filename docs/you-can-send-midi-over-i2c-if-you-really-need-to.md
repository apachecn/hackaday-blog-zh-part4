# 如果你真的需要，你可以把 MIDI 发送到 I2C

> 原文：<https://hackaday.com/2022/02/15/you-can-send-midi-over-i2c-if-you-really-need-to/>

乐器数字接口有一个很棒的首字母缩写词，说起来很好听，描述也很清晰。与乐器对话的标准依赖于 31250 bps 的串行信号，这使得使用任何具有可设置波特率的老式微控制器 UART 进行传输都很容易。然而，[凯文]已经开始探索通过 I2C 发送 MIDI 信号的实用性。

通过对 Arduino MIDI 库的一点黑客攻击，[Kevin]能够让微控制器通过 I2C 接口输出 MIDI 数据，并为该平台开发了一个有用的通用 I2C MIDI 传输。他的第一次测试涉及使用这项技术与 Gravity [双 UART 模块。](https://www.dfrobot.com/product-2001.html)在成功运行一个之后，[Kevin]意识到可以将四个连接到一个 Arduino 上，这样就有了 8 个串行 UARTS，或者用另一种方式来说，8 个 MIDI 输出。

在其最大的发展水平上，[Kevin]展示了他的 I2C MIDI 印章，获得了一个单一的 Raspberry Pi Pico [向 I2C 各地的 8 个 arduino](https://diyelectromusic.wordpress.com/2022/01/18/raspberry-pi-pico-i2c-midi-interface-part-4/)发送 MIDI 信号。所有的 Arduinos 都以菊花链形式连接在一起，它们的 5V 和 I2C 线连接在一起，该系统基本上将传统的 MIDI 通道换成了 I2C 地址。

这方面没有太多明显的杀手级应用，但如果你想将 MIDI 数据发送到一堆微控制器，你可能会发现用菊花链连接 I2C 比用经典的 MIDI-IN/MIDI-THRU 方式用串行线跳来跳去更容易。

我们以前也看过[凯文]的作品，比如美妙的高保真管弦乐队。休息后的视频。

 [https://www.youtube.com/embed/fsxN6XvLzmM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/fsxN6XvLzmM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

