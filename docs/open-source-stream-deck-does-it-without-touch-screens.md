# 开源 Stream Deck 无需触摸屏即可实现

> 原文：<https://hackaday.com/2020/07/09/open-source-stream-deck-does-it-without-touch-screens/>

[Adam Welch]过去已经用预制的关键矩阵和一把樱桃 MX 克隆体构建了宏垫。但是，世界上所有的贴纸和定制键帽都不会让这些宏垫像 stream deck 一样多功能——这些视觉快捷面板上的每个按钮都有微型触摸屏，一些 stream 用来改变 A/V 设置或在应用程序之间切换。

让我们面对它，流甲板是昂贵的。但 0.96 英寸的有机发光二极管显示器不是，SMD 触觉按钮也不是。为什么不模仿廉价的屏幕面板，让屏幕启动背后的按钮呢？[Adam]基于[Kilian Gosewisch]的[FreeDeck](https://github.com/koriwi/freedeck-hardware)的巧妙设计设计了这个宝贝，他们最终合作用一个专用的 PCB 来改进它。

操作的大脑是 Arduino Pro Micro，它通过两个 74HC4051 mux ICs 分别处理每个屏幕。由于 SD 卡模块，没有必要每次你想改变一个快捷方式或它的图片时都刷新“duino”。即使这副牌撑不了多久，也不会倾家荡产再建一副。戳过去的构建视频，其中有你需要自己制作的所有链接，包括一个方便的配置器。

有多种方法可以实现可视化宏面板。这里有一个使用单个屏幕，并将其分割成*布雷迪·邦奇*风格，以匹配矩阵。

 [https://www.youtube.com/embed/-3Zw8hbpVq4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/-3Zw8hbpVq4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢提示，[arturo182]！