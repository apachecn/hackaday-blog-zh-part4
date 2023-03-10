# 用 20 世纪 30 年代的电传打字机登录 Linux

> 原文：<https://hackaday.com/2020/04/15/logging-into-linux-with-a-1930s-teletype/>

深埋在所有基于 UNIX 的操作系统中的是早期计算的遗迹，那时“硬件”通常意味着带有凸轮、杠杆、滑轮和油脂的实际机械设备。但是仅仅因为 UNIX，甚至 Linux，曾经支持机械终端，并不意味着从 20 世纪 30 年代得到一台电传打字机很容易。

这就是[CuriousMarc]从他最近修复的 15 型电传打字机中学到的教训；我们报道了他解决的一个类似的模型 19 修复。关键问题是，他们所说的五位博多码比 ASCII 的发展早了几十年，这就需要一个转换器。像这样的任务对于 Arduino 来说是一个完美的工作——[Marc]在这方面投入了大量的工作——但是电传打字机的界面证明更具挑战性。设计用于通过电话线将两个或更多单元连接在一起，高压 60mA 电流环路接口需要一些定制硬件。测试过程令人着迷，因为它依赖于一个旧的惠普串行信号发生器来抛出一个五位串行脉冲流。

当他使用电传打字机在一台(或多或少)现代机器上登录 Linux 时，重要的时刻到来了。在解开了`stty`命令的秘密后，他能够登录了，这是一个 45.5 bps 的痛苦而缓慢的过程，但仍然是一个最令人满意的攻击。ASCII 艺术——还是波德艺术？—是一个不错的奖励。

我们喜欢这样的修复，几乎可以闻到这个设备周围的油脂和微弱的臭氧气味。我们对当前的世界形势并不感到兴奋，但我们很高兴[CuriousMarc]能够利用这段时间完成一项伟大的黑客技术，以纪念我们计算机历史上的另一项成就。

 [https://www.youtube.com/embed/2XLZ4Z8LpEE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/2XLZ4Z8LpEE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



谢谢你的提示，[亚历克斯]！