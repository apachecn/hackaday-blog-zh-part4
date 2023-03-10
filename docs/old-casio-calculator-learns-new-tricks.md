# 旧卡西欧计算器学习新技巧

> 原文：<https://hackaday.com/2022/04/06/old-casio-calculator-learns-new-tricks/>

[乔治·斯塔格]最近发现自己在禁闭期间被空闲时间的负担所刺痛。需要一个项目让他忙起来，他决定[升级他的 90 年代卡西欧 CFX-9850G 计算器以运行定制机器代码](https://threadreaderapp.com/thread/1510649920042283021.html)。

所有[乔治]真正想要的是让他的老式计算器理解反向波兰符号(RPN)。有问题的计算器已经可以运行自己的 BASIC 版本，但是定制的日立 CPU 在复杂程序的性能方面存在问题，并且在计算器上使用 RPN 不是一种现实的方式。用汇编语言编写的 RPN 解释器要快得多。

打开这个计算器的第一步是 ROM 转储，然后编写反汇编程序。令人难以置信的是，MAME 框架已经实现了计算器 CPU 的“部分实现”,这是编写全功能仿真器时急需的一针强心剂。

随着整个计算器在软件中模拟，从这里开始的计划包括用新代码替换 rom 中的一个基本命令，新代码将跳转到 RAM 中的一个地址。有了 32KB 的内存，最终就有了足够的实验空间，而且通过使用卡西欧的原始备份软件将内存转储到 PC 上，将程序上传到内存变得简单了。在这里，RAM 的内容可以很容易地用定制代码修改，然后上传回计算器。

随着 RAM 的使用，创建了新的例程来将自定义字符写入屏幕，并且创建了新的字体来将比正常情况下更多的字符挤压到显示器上。[George]最终移植了一个默认为 RPN 风格的 Forth 解释器，以最终实现他卑微的目标。他还设法让康威的《生活游戏》的一个版本运行起来，休息后看看视频。

我们这里的计算器黑客还不够多，所以一定要看看这个老式苏联计算器上的 [CPU 移植。](https://hackaday.com/2022/01/27/upgrading-a-soviet-calculator-with-a-modern-cpu/)

 <https://hackaday.com/wp-content/uploads/2022/04/QkVtqTBZRVAqDL_p.mp4?_=1>

[https://hackaday.com/wp-content/uploads/2022/04/QkVtqTBZRVAqDL_p.mp4](https://hackaday.com/wp-content/uploads/2022/04/QkVtqTBZRVAqDL_p.mp4)

[非常感谢 Adrian 提供的热门提示]