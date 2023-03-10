# 纯文本的编译器也播放音乐

> 原文：<https://hackaday.com/2019/01/17/readable-file-compiles-plays-a-compiler-in-plain-text-also-plays-musicmusic/>

作为一个阅读一些数学分支的外行人，数学家似乎只是真正喜欢创造和解决难题的人。而且，知道计算机科学与数学有许多共同的基础，我们可以假设大多数计算机科学家也是解谜者。这个来自[tom7]的最新项目展示了他的拼图创作和解决技巧，其中有一个[可读文件，也是一篇论文，也是 C 程序的编译器，还可以播放音乐](http://tom7.org/abc/)。

[tom7]从英特尔 8086 处理器的指令集开始。在可用的指令中，他只想使用在文本文件中也可读的指令。这极大地限制了该文件能够执行的内容，同时也设置了难题。他通过仅使用也编码为文本的指令克服了他发现的每个障碍，包括有限的存储空间、一旦程序完成就没有明显的退出方式、不能在程序中向后跳转(即循环)，以及一旦指令集以这种方式受到限制就会出现的一系列其他问题。

其结果是一种 C 编译器，这可能不是执行程序最有效的方式，但肯定是炫耀[tom7]计算机科学博士学位的最有效方式。作为奖励，该文件还可以播放一种过时的声音文件，因为其中一个可用的指令是调用处理器与 I/O 进行交互。如果您想了解更多关于编译器的信息，您可以[查看我们的初级读本](https://hackaday.com/2018/11/06/warnings-are-your-friend-a-code-quality-primer/)来研究它们的一些功能。

感谢[Greg]的提示！

 [https://www.youtube.com/embed/LA_DrBwkiJA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/LA_DrBwkiJA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

