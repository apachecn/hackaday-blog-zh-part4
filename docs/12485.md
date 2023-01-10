# 用 PicoEMP 逆向工程荣耀你的路

> 原文：<https://hackaday.com/2022/01/15/glitch-your-way-to-reverse-engineering-glory-with-the-picoemp/>

在某种程度上，我们的大多数项目都是减少故障的一种实践。无论它们是自己造成的软件或硬件错误，或者即使问题中的故障来自我们无法控制的来源，事情的全部要点是让它平稳地和可预测地运行。

然而，情况并非总是如此。有时候，故意引起一个小故障可能是一个有用的工具，尤其是在逆向工程的时候。这就是[这个低成本电磁故障注入工具](https://github.com/newaetech/chipshouter-picoemp)可以派上用场的地方。EMFI 是一种扰乱嵌入式系统上运行的程序正常流程的方式；如果应用得当，运气好的话，它可以让系统进入可利用状态。科林·奥弗林称他的 EMFI 工具为 PicoEMP，是他以前的[芯片设计者](http://www.chipshouter.com/)工具的一个更驯服的版本。PicoEMP 专注于用户安全，这是一个重要的考虑因素，因为其业务端可以在其输出端施加约 250 伏的电压。安全特性包括:为高压部分产生 PWM 信号的 Raspberry Pi Pico 的隔离、高压元件上方的安全外壳，以及一个用于对电容放电并防止不愉快意外的开关。

在使用中，高压脉冲施加在注射尖端上，该尖端基本上是铁氧体磁心天线。尖端将磁通量集中在一个小区域，这有望在目标系统中引起预期的毛刺。下面的视频显示了 PicoEMP 被用来干扰比特币钱包，以及对高压脉冲的一些测试。

如果你对皮电磁脉冲和一般故障感兴趣，一定要留意[科林]2021 年关于这个主题的远程演讲。在此之前，你可能想调查一下对任天堂 DSi 和 T2 的故障攻击，以及 Wacom 平板电脑的 USB 故障。

 [https://www.youtube.com/embed/nB5arJi-tVE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/nB5arJi-tVE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



这个帽子提示给【leo60228】。谢谢！