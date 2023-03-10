# 被赋予新生命的工业机器人及其控制器

> 原文：<https://hackaday.com/2020/04/08/industrial-robot-given-new-life-and-controller/>

我们都认为我们可以不时地使用第三只手臂，但当我们实际在大脑中进行这个思维实验时，我们最终会遇到[卡尔塔达尼尔]发现的相同障碍，即缺乏控制器。然而，他的第三只手臂不仅仅是一个想法。这是一个安川工业机器人，他能以相当便宜的价格买到，但它缺少一些零件，他一直在慢慢更换。

机器人手臂没有控制器或软件，也没有任何类型的原理图，所以第一步是逆向工程布线图，以了解手臂内部的情况。从那里一些驱动器是为伺服系统，但关键是所有这一切是自制的控制器。逆运动学数学是在 Python 中完成的，并在工业 PC 上运行。一旦最终组装完成，[卡尔塔达尼尔]就有了一个可以完成他能想到的任何任务的功能性机械臂。

有趣的是，在他展示机器人为他刷牙的同时，他还设置了机器人来拨动一台[无用机器的开关，这台机器的存在只是为了关闭](https://hackaday.com/2018/08/17/multi-switch-useless-box-is-useless-in-multiple-ways/)。一个巨大的工业大小的机械臂被用来打开一个 20 美元的设备，它会立即自动关闭，这有点超现实主义，但这种荒谬值得一看。

 [https://www.youtube.com/embed/_P4xiNx-hc4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/_P4xiNx-hc4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

