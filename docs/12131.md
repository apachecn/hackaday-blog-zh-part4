# 精心设计的试验板会自动绘制您所构建的任何东西的示意图

> 原文：<https://hackaday.com/2021/12/06/tricked-out-breadboard-automatically-draws-schematics-of-whatever-you-build/>

就电子设计而言，电路试验是有趣的部分——创意源源不断，元件来来去去，跳线变得一团糟，但当电路最终投入使用时，这一切都是值得的。然后是“我做了什么？”阶段，在这个阶段，你必须回溯电路，记录你是如何建造它的。要是有更好的方法就好了。

多亏了[Nick Bild]，才有了以[“Schematic-o-matic”](https://github.com/nickbild/schematic-o-matic)形式出现的，旨在实现试验板文档流程的自动化。诀窍是使用一个试验板，其中每个母线都连接到 Arduino Due 上的一个 IO 引脚。一个程序运行通过试验板上的每个点，运行一个连续性测试，看看是否有跳线连接它们。然后，Python 程序使用连接列表以及一些关于元件插入电路板位置的基本信息来生成 KiCad 原理图。

[Nick]承认原理图在这一点上很粗糙，为了防止错误读数，先从试验板上移除一些元件(如 IC)有点不方便。但是这看起来像是自动完成 80%的工作，然后再担心剩下的工作是一个大胜利。此外，我们还可以看到一条通向自动 ic 探测甚至无源元件测量的道路。但即便如此，它也是一个很好的工具。

 [https://www.youtube.com/embed/L2e3amMnLaA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/L2e3amMnLaA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

