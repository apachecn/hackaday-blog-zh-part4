# 编译器资源管理器，浏览

> 原文：<https://hackaday.com/2019/09/30/compiler-explorer-explored/>

不久前，我们向您介绍了一个网站，Godbolt 编译器资源管理器，它允许访问者使用大量编译器编译代码并比较它们的输出。我们怀疑一些读者说，“哇！我可以用那个！”，而其他人可能会说，“嗯？”如果你是第二组，你应该看看下面的视频【什么是克里尔】，他[使用网站](https://www.youtube.com/watch?v=ysaBmhMEyUg&feature=share)走过。他使用四种不同的编译器研究了四种不同的算法，这是一个很好的例子，说明如何使用该工具来决定如何编写软件。

如果您错过了我们关于该工具的原始帖子，您仍然可以[赶上](https://hackaday.com/2019/09/13/peek-into-the-compilers-code-lots-of-compilers/)。即使您不太关心编译器资源管理器，这也是一个机会，可以在一个有经验的程序员查看一些 C 代码和生成的汇编代码时，从他的肩膀上看过去。

结果可能会让你吃惊。在第一个例子中，CLANG 做了一些很好的优化，但是相比之下，其他编译器创建了很多代码。其中一个编译器，微软编译器，指定了一个不正确的选项，所以它不太好，但如果有正确的选项，可能会做得更好。如果你感兴趣的话，你可以自己尝试一下。

我们很乐意看到为[FPGA](https://hackaday.com/2015/07/21/learn-fpgas-in-your-browser/)做这样的事情。如果你会运行 Docker，你可能也会对[企鹅号](https://hackaday.com/2019/05/09/examine-source-code-to-assembly-mapping-with-penguintrace/)感兴趣。

 [https://www.youtube.com/embed/ysaBmhMEyUg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ysaBmhMEyUg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

