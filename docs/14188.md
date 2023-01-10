# 一个方便的 PS/2 键盘测试工具

> 原文：<https://hackaday.com/2022/07/12/a-handy-tester-for-a-mountain-of-ps-2-keybords/>

黑客生活并非没有挑战，其中最主要的是总是处于获取模式的趋势。当我们遇到大量的散装设备，或者看到有机会从电子垃圾流中拯救一些不起眼的设备时，我们通常会扑向它，而不管是否明智。

我们猜想这就是为什么[内森]最终拥有了一大堆 PS/2 键盘。说真的有成千上万的东西。与其拖着电脑去测试，[Nathan]不如组装了这个基于 Arduino 的便携式测试仪来看看哪些键盘还能使用。下面的视频详细介绍了这一构建，但基本内容非常简单——一个 Arduino，一个 16×2 液晶显示器，以及一些零件来运行它并为它充电。当然，还有一个 PS/2 插孔，可以插入键盘并通电。有趣的是，16×2 显示器是一个旧的视差单元，来自 RadioShack 仍然存在并出售他们的东西的时代。这需要一点努力来让它与 Arduino 一起工作，但最终它像一个魔咒一样工作——插上键盘，你键入的任何内容都会显示在屏幕上。

当然，很难看到这样的东西，以及背景中堆积如山的键盘，而不是设计出真正自动化整个测试过程的方法。也许一台装有触控笔的老式 3D 打印机可以在记录测试仪输出的同时依次按下每个键——类似于 [this *Wordle* -bot](https://hackaday.com/2022/02/26/solving-wordle-by-adding-machine-vision-to-a-3d-printer/) ，但是是在键盘范围内。这有点违背[Nathan]的可移植性目标，但想想还是很有趣。

 [https://www.youtube.com/embed/6i3iC0MTEVE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/6i3iC0MTEVE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

