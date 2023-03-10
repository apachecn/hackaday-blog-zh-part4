# IC 时钟使用电流表来显示独特的时间

> 原文：<https://hackaday.com/2021/09/10/ic-clock-uses-ammeters-for-a-unique-time-telling-display/>

对于黑客来说，用传统的非时钟物品制作时钟是一种成人礼。无论是闪烁的发光二极管还是移动指针的伺服系统，我们都有自己的方式来知道现在是什么时候。[SIrawit]采取了一种新的方法，通过[使用电流表来显示时间](https://www.reddit.com/r/electronics/comments/phxmxo/my_amp_meter_clock_is_now_completed/hblo8yx/)。

该时钟主要使用 CMOS ICs 构建。CD4060 产生 1HZ 时钟信号，然后传递给并行计数器，以记录小时、分钟和秒。[SIrawit]决定保持电流表的预期功能，而不是更换内部元件，只保留指针和表面。为了将数字信号转换为变化的电流，他使用了一系列并联到电流表低端的 MOSFETs，以及不同尺寸的限流电阻。通过适当调整这些电阻的大小，可以通过开启或关闭 MOSFETs 来实现指针的精确移动。你可以在[项目的 GitHub 页面](https://github.com/Sirawit7205/ampmeter-clock)上看到原理图并了解更多关于这是如何实现的(在撰写本文时，最近的提交是‘PCB’分支中的[)。](https://github.com/Sirawit7205/ampmeter-clock/tree/pcb)

除了容纳所有电子器件的定制 PCB 之外，PCB 也有助于构成外壳。虽然外壳的主体是由重新利用的接线盒制成的，但[SIrawit]的前面板在铝制基板上有一个 PCB。虽然电路板没有实际的走线或电气意义，但这是为您的项目获得精确切割的铝片的一种廉价而简单的方法，并配有外观锐利的白色阻焊膜。

我们喜欢看到很酷很独特的报时方式，比如用[谢妮管用二进制拼出时间](https://hackaday.com/2021/08/28/binary-clock-lets-the-nixies-glow/)！

 [https://www.youtube.com/embed/0dg1gIumV6I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/0dg1gIumV6I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[通过[遥控/电子](https://www.reddit.com/r/electronics/comments/phxmxo/my_amp_meter_clock_is_now_completed/)