# 维纳比利是你买不到的令人愉快的键盘

> 原文：<https://hackaday.com/2019/03/19/venabili-is-the-delightful-keyboard-you-cant-buy/>

如果你编码或写了很多，你的生活或死亡与你的键盘。Venabili 网站称 Venabili 为“令人愉快的键盘”,这引出了一个问题:是什么让键盘令人愉快？该网站继续说道:

> “Venabili 是一个 40%机械的、可编程的、符合人体工程学的、可黑客攻击的计算机键盘。
> 
> 作为一个完全可编程的键盘，它使您能够创建功能层，声明可以作为修饰键和普通键操作的多功能键，控制鼠标，定义宏，等等。"

听起来至少有 40%令人愉快，对吧？你在哪里买一个？你不知道。键盘是一套计划，就像绝地光剑一样，你必须自己打造。

键盘的核心是 STM 32 f 103“blue pill”Maple Mini 克隆，我们之前已经看过很多次了。机械装置是 48 个 Cherry MX 开关和一个键盘外壳，您可以使用提供的 PDF 文件进行激光切割或以其他方式制作。如果您喜欢更改物理布局，也可以修改 SVG 源文件。除了蓝色药丸和开关，你还需要一堆二极管。

对黑客来说，用层和宏来配置键盘很容易，但不完全是用户友好的。你修改一个 C 文件，重新编译并刷新键盘中的固件。你可以在[构建指南](https://docs.venabili.sillybytes.net/building)中获得关于构建和配置的所有细节。

我们已经看到 3D 打印机用来[修改机械开关](https://hackaday.com/2018/12/07/better-mechanical-keyboards-through-3d-printing/)。如果你想了解更多关于[蓝色药丸](https://hackaday.com/2017/03/30/the-2-32-bit-arduino-with-debugging/)的信息，我们也已经做了。