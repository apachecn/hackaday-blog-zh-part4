# 旋转控制器调节电脑音量

> 原文：<https://hackaday.com/2020/06/04/rotary-controller-dials-in-pc-volume/>

尽管机械键盘很棒，但大多数预制和团购模式都没有媒体控制。如果你想让旋转编码器和有机发光二极管屏幕显示你在哪个功能层工作，你可能需要从头开始构建你自己的键盘。

Hackaday 的校友(卡梅伦·科沃德)通过为他的键盘建造一个机电伙伴来解决这个问题，作为音量控制。既然我们不再依赖它们来打电话，旋转式拨号盘是一种有趣的回归，因为它基于其强大和初级的技术，看起来更简单。这一个是从一个可爱的燃烧橙色贝尔 Trimline 电话，这是峰值旋转拨号和一个想法的最后喘息之前，音频拨号完全接管。

从操作上来说，[卡梅伦]正在用 Arduino Nano 读取表盘的脉冲，并使用 Python 脚本来监控串行连接，并将脉冲转换为音量控制。我们喜欢这不是传统意义上的音量旋钮——这是一个百分比游戏。拨“2”将所有程序的音量调到 20%，拨“8”将音量调到最大值的 80%。需要静音？只要拨“0”，你就会开始理解为什么人们想放弃旋转拨号。不会花*那么*长时间，但也不是瞬间。休息后请欣赏演示。

这不是我们第一次看到用于控制音量的旋转拨盘，但这是这款旋转手机的次要卖点之一。

 [https://www.youtube.com/embed/fksdtyq7Ruo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/fksdtyq7Ruo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

