# 让雨刷随着节拍摇摆

> 原文：<https://hackaday.com/2022/03/31/making-windshield-wipers-rock-to-the-beat/>

当你在开车的时候，你可能会偶尔注意到你的指示器或者挡风玻璃刮水器偶然地与音乐同步。[Cranktown City]想要确保他的雨刷能一直配合节拍，然而，[开始着手让它这样做。](https://www.youtube.com/watch?v=DB4GHDJvdEg)

拆卸刮水器电机后，原来的控制器 PCB 被撕掉，仅用于帮助确定刮水器位置的原始位置触点。然后，在破损的板上钻孔，安装一个旋转编码器，以跟踪雨刷的整个运动过程。

Arduino 用于读取来自雨刮器杆的信号，以了解雨刮器应处于何种模式，并使用电机控制器来驱动雨刮器。它还读取编码器和原始位置触点来跟踪雨刮器的移动，并使用比例控制器来控制雨刮器的位置。MSGEQ7 频谱分析仪用于跟踪音乐的低音，以确定同步的节拍。

最终的构建确实可以工作，尽管与我们见过的其他设计方式不同。它不是测量 BPM 和同步四到地板的脉冲，而是简单地跟踪低频带输出，因此对时髦的鼓点更敏感。

这是一种改装汽车的有趣方式，即使它需要从引擎盖上切下一大块。如果你正在编写你自己的厚颜无耻的汽车黑客，一定要给我们写信。休息后的视频。

 [https://www.youtube.com/embed/DB4GHDJvdEg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/DB4GHDJvdEg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

