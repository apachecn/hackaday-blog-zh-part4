# 在 DIY Forth

> 原文：<https://hackaday.com/2021/07/08/diy-forth-on-arduino/>

在最近一个下雨的下午，[Thanassis Tsiodras]决定为 Arduino 建造他自己的第四个来解闷。一周的紧张黑客攻击后，他称之为完成，并在 GitHub 上发布了他的项目 [MiniForth。[Thanassis]说他受到了几年前我们的](https://github.com/ttsiodras/MiniForth/)[系列 Forth 文章](https://hackaday.com/2017/01/27/forth-the-hackers-language/)的启发，他的目标是从头开始构建一个 Forth 解释器/编译器，并将其放入蓝色药丸微控制器中。完成后，他很自然地决定将其压缩到一个只有 2K 内存的 Arduino Uno 中。

即使你对第四语言有矛盾的想法，[塔尼西斯]的项目也有一些很棒的想法值得一试。例如，他是重复任务的 Makefile 自动化的大力支持者，该项目的 Makefile targets 实现了开发、构建和测试他的代码所需的几乎所有任务。

一些开发和测试任务更容易在主机上执行。为此，[Thanassis]使用 [simavr](https://github.com/buserror/simavr) 模拟器在本地测试他的程序。代码也是可移植的，他可以在主机上本地编译它，并使用 GDB 以及 Valgrind 和 AddressSanitizer 来调试它，以检查内存问题。他选择只用零成本的抽象用 C++编写程序，但发现用 ArduinoSTL 编译太慢，而且占用太多内存。没问题，[Thanassis]编写了自己的极简 STL 并实现了几个节省内存的技巧。作为最后的测试，Makefile 还可以执行 Forth 命令的测试套件，包括一个 [FizzBuzz](https://en.wikipedia.org/wiki/Fizz_buzz) 算法，以检查最终的实现。

这里有一个[MiniForth 在运行](https://youtu.be/xePollbCzow)的短视频，它使一个 UNO 上的 LED 闪烁，中断下方的视频显示了运行中的各个 Makefile 任务。如果你想了解更多，请查看[埃利奥特·威廉姆斯的 Forth 系列](https://hackaday.com/2017/01/27/forth-the-hackers-language/)，它启发了【塔纳西斯】和[这篇 2017 年的文章，讨论了几种不同的 Forth 实现](https://hackaday.com/2017/01/04/browsing-forth/)。你曾经构建过你自己的编译器吗？请在下面的评论中告诉我们。

 [https://www.youtube.com/embed/YNVHa0TBKeI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/YNVHa0TBKeI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

