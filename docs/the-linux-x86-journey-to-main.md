# Linux X86 的 Main 之旅()

> 原文：<https://hackaday.com/2021/11/05/the-linux-x86-journey-to-main/>

在你的`main`函数执行之前，你有过程序崩溃的经历吗？这种情况很少见，但也有可能发生。当它发生时，您需要理解在操作系统启动您的程序和您的第一行代码在`main`中执行之间的幕后发生了什么。幸运的是[Patrick Horgan]有[关于这个主题的教程](http://dbp-consulting.com/tutorials/debugging/linuxProgramStartup.html)，非常详细。它没有涵盖静态链接库，但是正如他所指出的，如果你理解了他所涵盖的内容，你自己就很容易理解了。

事实证明，操作系统对 main 一无所知。然而，它知道一个叫做 _start 的符号。您的运行时库提供了这一点。该代码包含一些堆栈操作，并最终调用同样由库提供的`__libc_start_main`。

从那里开始，您用一些技巧来管理程序的环境，更多的库调用如`__libc_init_first`和`__libc_init`做更多的设置工作。你可能会认为这已经很接近了，但是还有更多的工作要做，包括设置`at_exit`和转换位置无关代码，更不用说动态链接库了。

这是一个看起来你并不真正需要的话题，除非你真的需要。即使您使用另一种语言来生成可执行文件，它们都必须遵循这些步骤。当然，对于许多语言来说，启动是静态的，不太可能需要你去调试它，但是知道幕后发生了什么仍然是很好的。

如果你想要一个快速的 Linux 汇编教程，[可以看看](https://hackaday.com/2016/06/14/linux-assembly-required/)。如果你喜欢把你的汇编代码放进一个 C 源代码文件，[你也可以这么做](https://hackaday.com/2016/06/08/gcc-some-assembly-required/)。