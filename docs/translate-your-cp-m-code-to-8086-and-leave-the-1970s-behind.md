# 把你的 CP/M 代码翻译成 8086，把 70 年代抛在脑后！

> 原文：<https://hackaday.com/2021/06/13/translate-your-cp-m-code-to-8086-and-leave-the-1970s-behind/>

“让我们的家庭计算走出 20 世纪 70 年代，进入 20 世纪 80 年代甚至更远”是 [8088ify](https://github.com/ibara/8088ify) 的创造者做出的不可抗拒的承诺，这是一款将 CP/M 可执行文件从基于 8080 的原件翻译成汇编代码的软件，这些代码应该在 MS/DOS 下的 8088 上运行。在 2021 年，我们怎么能拒绝这样一个未来的承诺呢，尽管代码不是为唐娜·萨默之声或村民写的，而是在 2021 年为 [PCjam，](https://pcjam.gitlab.io/)庆祝最初的 IBM PC 40 周年而写的。

正如该代码的作者[ibara]指出的那样，英特尔打算将 8088 作为 8080 的现成升级途径，并在不直接兼容的情况下设计其指令集，以使两者之间的转换成为一个简单的过程。当时有用于这项任务的商业软件，但直到今天，仍然没有开源许可。为了跨平台和编译器的可移植性，它是用 ANSI C 编写的，甚至可以在 CP/M 下编译。

PCjam 非常值得一看，如果你们中的任何人想为最早的 MS-DOS 机器写点东西，我们建议你们为它写点东西。同时，如果你想探索 CP/M，[你可以在 Raspberry Pi](https://hackaday.com/2016/10/12/raspberry-pi-boots-cpm/) 上运行一个裸机仿真器。

表头:托马斯阮， [CC BY-SA 4.0](https://commons.wikimedia.org/wiki/File:Intel_D8088.jpg) 。