# 定制的钢琴使钢琴发痒

> 原文：<https://hackaday.com/2022/01/28/custom-piano-tickles-the-ivories/>

“黑客”的核心精神通常被解释为修改某样东西，使之用于它原本不适合的用途。许多构建是对现有技术的修改或改进，但有时这还不够。有时我们不得不一路走下去，完全从零开始建造一些东西，而[【巴尔塔萨】最近的类似钢琴的乐器](http://bicyclesonthemoon.info/klavirko/)正好属于这一类。

这个电子键盘完全是从零开始设计和建造的，包括乐器的结构和按键本身。[巴尔塔萨]用木头手工制作每一个，然后为他们建造一个行动机制来登记印刷机。虽然它们不检测速度或压力，但该乐器能够定义任何音符的波形和包络，能够在每个键上演奏多个音符，并能够改变单个八度音阶。这得益于连接到 STM32 微控制器的定制 6×12 矩阵。[Balthasar]选择这种微控制器的部分原因是，它可以在单个时钟周期内完成制作音乐所需的一些计算，这是该平台的一个令人印象深刻但报道不足的功能。

所有的东西都组装在一起，键盘的功能多得惊人。使用自定义矩阵，可以很容易地将钢琴上的单个八度音阶切换到任何可编程的范围，使 61 键钢琴听起来像完整的 88 键钢琴。任何声音都可以被编程，进一步增加了它的多功能性，这对于从头开始构建来说更加令人印象深刻。虽然这个版本更侧重于键盘的电子设备，但我们已经看到其他版本也复制了传统原声钢琴的物理动作。

 [https://www.youtube.com/embed/fG8-jLbbbjQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/fG8-jLbbbjQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

