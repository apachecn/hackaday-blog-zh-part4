# 护士呼叫系统变得完整

> 原文：<https://hackaday.com/2019/03/09/a-nurse-call-system-becomes-turing-complete/>

英国著名登山家乔治·马洛里曾提出，爬山是没有用的。相反，他认为，爬山的唯一原因是因为它就在那里。同样，当你成为医院护士呼叫系统的专家时，你可能会发现你可以用它们做类似的事情。[做一个图灵完整的护士呼叫系统](https://eriknl.github.io/hack/2019/02/02/Netrix-computer.html)是你可以做的事情，因为你可以。

[Erik]一直在研究这种特殊的呼叫系统，称为 Netrix，并使用 Wireshark 来探查它的所有协议。有了这些信息，他意识到有可能使用系统的路由功能来执行任何图灵完整系统都可以完成的所有任务:条件分支和内存访问。他设置了一个虚拟机，并开始使用护士呼叫系统的功能实现所有这些任务。

这个项目的设置令人印象深刻，并掩盖了对这个专有系统以及一般计算机科学的广泛了解。有趣的是，我们可以看到一些东西是如何从原本不能使用的部分组成一个工作的计算机系统的。甚至[非电子的东西](https://hackaday.com/2011/03/25/mechanical-turing-machine-can-compute-anything-slowly/)也可以用作图灵完全计算机。

[通过维基媒体共享的照片](https://commons.wikimedia.org/wiki/File:Nurse_Call_Button_at_Hospital_(17238701230).jpg)