# 具有经典风格的微控制器显示屏

> 原文：<https://hackaday.com/2020/05/08/a-microcontroller-display-with-a-classic-twist/>

在一阵锁定引起的无聊中，[Peter Z]通过 Android 应用程序(德语，[谷歌翻译链接](https://translate.google.com/translate?client=ubuntu&client=tw-ob&channel=fs&oe=utf-8&um=1&ie=UTF-8&hl=en&sl=auto&tl=en&u=https%3A%2F%2Fwww.mikrocontroller.net%2Ftopic%2F494974%23new))将他的智能手机变成了 LCD 屏幕(模拟)，这样移动设备就可以插入你最喜欢的微控制器，经典的 HD44780 LCD 外观可以在它的屏幕上复制。

它不是标准的 HD44780，而是一个定制的 UART 串行协议，所以如果你想找一个东西来代替一个坏了的 LCD，这不是你的包。但是，如果你正在寻找一个大的 UART 终端进行调试，一个漂亮的美学，你赢了。

我们猜测，只要稍加努力，串行-蓝牙转换器也能发挥作用。该协议也很简单，这意味着几乎任何微控制器都可以使用它。所有的代码和 APK 都可以从上面链接的论坛获得，下面有一个 YouTube 视频。

评论中的头号抱怨将是这没有模仿 HD44780，所以如果这真的是你想要的，[阅读这篇深入研究 HD44780](https://hackaday.com/2017/04/28/manual-lcd-makes-information-display-tedious-educational/) 并获得黑客攻击。

 [https://www.youtube.com/embed/ndMXhO3ZwDM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ndMXhO3ZwDM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

