# 电阻分压器键盘的改进技术

> 原文：<https://hackaday.com/2021/06/09/improved-technique-for-resistive-divider-keypads/>

[Swiss Knife of Electronics]频道的[Lauri Pirttiaho]在 Hackaday.io 上解释了如何简化电阻分压器键盘设计。

通常的方法是构建一个电阻阶梯，为每次按键提供唯一且等距的电压。如果你只有四五个独立的按钮，这并不是很难，但是如果你有一个 12 或 16 个键盘的矩阵，事情就复杂了。[Lauri]回顾过去，想出了一个更好的方法，特别是 1990 年的一本 646 页、1 公斤重的教科书— *模拟 Ic 设计:电流模式方法* ，作者是 Toumazou、Lidgey 和 Haigh。他了解到，有时在电压域很难做到的事情在电流域很容易做到。

通常情况下，根据所按下的键，您会加入一些电阻来形成不同的分压器，并通过 ADC 读取分压器产生的电压。但这意味着使用分压方程，按键之间的电压差可以变得非常小。降低分压器并测量通过电流镜的电流，会在其输出负载电阻上产生一个线性电压，微处理器可以轻松读取该电压。[Lauri]已经在他的 GitHub 库上发布了一个 Arduino 程序的例子。

沉重的模拟电子设备，当然，但如果你正在阅读超过 12 个键的东西要记住。你有通过研究旧的和/或不常用的技术来解决问题的例子吗？请在下面的评论中告诉我们。

 [https://www.youtube.com/embed/pQMzIPOyPKk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/pQMzIPOyPKk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

