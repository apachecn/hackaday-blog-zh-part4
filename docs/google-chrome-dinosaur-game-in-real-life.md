# 现实生活中的谷歌 Chrome 恐龙游戏

> 原文：<https://hackaday.com/2020/08/06/google-chrome-dinosaur-game-in-real-life/>

[Ryan]想黑掉谷歌 Chrome 恐龙游戏，这样他就可以用自己的动作控制恐龙。游戏只需要按两次键盘(上下箭头键)，所以用 Arduino 键盘库控制游戏只需要几个简单的函数调用。

他在构建中使用 Arduino MKR 板，但他指出任何数量的其他板也可以工作。一个力传感器检测他的跳跃，一个拉伸传感器检测他的躲避。拉伸和力传感器都是电阻式传感器，因此需要两个简单的分压器电路(每个传感器一个)将力的变化转换为电压。你可能需要调整传感器阈值，以确保代码响应你的运动，但[Ryan]在软件中很容易做到这一点，因为两个阈值都存储为全局变量。

这是一个非常简单的技巧，但可以带来一些有益的社交距离的乐趣。你还喜欢哪些可破解的谷歌 Chrome 扩展？

 [https://www.youtube.com/embed/9Gm4fwFOh_A?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/9Gm4fwFOh_A?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

