# 独特的番茄定时器显示报价，而你的工作

> 原文：<https://hackaday.com/2021/11/05/unique-pomodoro-timer-displays-quotes-while-you-work/>

[zorbash]想出了一个很棒的附带项目，同时设计了一种无需使用 Good Reads 或亚马逊工具即可阅读电子书笔记和高亮部分的方法:[构建一个小工具来显示最喜欢的作者及其书籍的引文](https://zorbash.com/post/elixir-nerves-pomodoro-timer/)。该项目被称为大脑，因为它建立在一个名为神经的物联网平台上。

作为一个额外的奖励，这个小工具可以作为一个番茄定时器——这是一种时间管理方法，你可以工作 25 分钟，中间休息 5 分钟，每四个番茄休息更长时间。Brain 显示一个 25 分钟的报价，然后闪烁屏幕以引起[zorbash]的注意，时间到了。我们认为这是一种很好的、不引人注目的做事方式。没有内置的中断，但这就是[zorbash]滚动的方式。

引用是使用[书虫](https://github.com/zorbash/bookworm)获取的，这是一个【zorbash】编写的脚本，可以在 GitHub 上获得。它使用一个 Raspberry Pi 2 B，一个 SD 卡来存储 JSON 的报价，一个 Wi-Fi 加密狗来允许获取。如果你想知道这个围栏，它是由粘土制成的。

如果你更喜欢你的番茄定时器，这里有一个，只要你把它插入 USB 端口，它就会启动。