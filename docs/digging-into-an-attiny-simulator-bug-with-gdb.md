# 和 GDB 一起挖掘一个 ATtiny 模拟器 Bug

> 原文：<https://hackaday.com/2021/08/26/digging-into-an-attiny-simulator-bug-with-gdb/>

能够在堆积如山的源代码中追踪到一个 bug 本身就是一项技能，而且这是一项很难从书本或在线教程中学到的技能。除了在调试自己的项目时不断尝试学习之外，下一个最好的方法就是观察别人的过程。[Uri Shaked]给了我们一个很好的机会来提高我们的调试技能，因为他演示了如何在 Wokwi Arduino 模拟器中追踪并消灭一个 bug。

一位用户好心地报告了这个错误，并附上了令人不快的 Arduino 草图。[Uri]的第一步是将草图缩减到可能产生 bug 的最小程序。

一旦产生了一个最小程序，就该检查问题是出在 Arduino 库中还是 Wokwi 模拟器中了。[Uri]编译了草图，加载到一个 ATtiny85 上，比较了模拟器和实物的行为。结果代码在物理环境下运行良好，所以问题一定出在 Arduino 模拟器本身。

为了找出模拟器中的错误，[尤里]决定拿出一把大枪——GDB。接下来是如何使用 GDB 通过检查源代码、使用断点和打印语句来隔离问题的精彩演示。最后，[Uri]设法将问题隔离到定时器/计数器中断标志寄存器模拟中的一个错误位置。

如果你想了解更多[Uri]的调试能力，可以看看他对 ATtiny 的写保护和配置保险丝的[探究。如果你已经被 GDB 的力量所震撼，并想了解更多，](https://hackaday.com/2020/11/23/the-mystery-of-a-particular-attiny85-fuse/)[看看这个快速教程吧！](https://hackaday.com/2020/11/06/local-and-remote-debugging-with-gdb/)

 [https://www.youtube.com/embed/YUUHw-bU9yk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/YUUHw-bU9yk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

