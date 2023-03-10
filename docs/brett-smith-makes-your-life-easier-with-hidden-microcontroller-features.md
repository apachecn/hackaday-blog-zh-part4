# Brett Smith 通过隐藏的微控制器功能让您的生活更加轻松

> 原文：<https://hackaday.com/2019/06/27/brett-smith-makes-your-life-easier-with-hidden-microcontroller-features/>

曾经有一段时间，微处理器是缓慢而昂贵的设备，需要大量的支持芯片才能运行，因此工程师们想出了巧妙的技巧，使用额外的硬件预处理输入来避免必须创建更多的代码。通常会发现一些逻辑门、一个比较器，甚至无处不在的 555 定时器做一些工作来减轻计算机的负载，工程师们学会了理所当然地使用这些组件。

好的一面是，这些年来，这些伟大的硬件技术已经被嵌入到现代微控制器中。问题是你要了解他们。布雷特·史密斯最新发表的黑客日超级会议演讲“为什么要这么做？”，旨在[揭开隐藏在微控制器](https://www.youtube.com/watch?v=O7ZtaPOkDyc)中的有用硬件的神秘面纱。

加入我们下面的深入探讨和这次演讲的嵌入式视频。超级电脑是终极硬件大会——不要错过参加今年 11 月 15 日至 17 日在加州帕萨迪纳举行的的机会。

## 在快速计算的世界中走向成熟

今天的硬件黑客通常不是在 8 位微处理器的裸机世界中学徒后进入微控制器世界的，相反，他们更有可能是在 PC 或 Mac 上学习编码的一代人，他们通过 Arduino 等电路板进入硬件世界。他们擅长编码，对他们来说，计算机确实总是非常快。对于那些头发花白的老工程师来说，硬件解决方案是必要的，但对于今天的工程师来说，这个问题可以用软件来解决。

这很好，直到你发现自己在使用一个资源有限的平台，比如低成本的微控制器。突然之间，时钟周期就像几年前一样重要，几行代码或一个函数调用就能产生足以毁掉一个项目的差异。

## 微控制器的特点是什么

在这一点上，这些额外的硬件可能会非常有用，但你不会在一个典型的 ATtiny 或 PIC 周围看到 74 逻辑或其他芯片。这是因为许多微控制器带有比较器、定时器或内置基本组合逻辑等组件，需要通过软件来实现。对于那些只通过软件接触微控制器的人来说，这些并不是显而易见的，因此也是 Brett 演讲的重点。当您经常可以选择一个已经包含硬件的微控制器来预处理您的输入而无需额外的代码时，为什么要这么做呢？

[![If you didn't know this was already built-in, you could spend a lot of time doing the same job. From the ATtiny48 data sheet(PDF).](img/88d47b43ed4e696643ca2c7a0c4de869.png)](https://hackaday.com/wp-content/uploads/2019/06/brett-smith-comparator-attiny48-themed.jpg)

If you didn’t know this was already built-in, you could spend a lot of time doing the same job in code. From [the ATtiny48 data sheet](http://ww1.microchip.com/downloads/en/DeviceDoc/doc8008.pdf)(PDF).

他以设置音调为例，音调是一个简单的模拟输入，一旦达到某一水平就会触发。使用模拟读取功能，然后进行比较，可以完成这项工作，但代价是占用宝贵的时钟周期。诀窍在于发现微控制器的内置比较器可以免费完成这项工作。

Brett 鼓励我们研究流行芯片的数据手册，甚至带我们看了几个例子。引脚变化中断或内置正交解码器等功能令人惊叹，如果你不知道它们在板上的话。在这个过程中，他谈到了一些有趣的问题，比如不同供应商的名称，让你在这些数据表上有一个好的开始。

除了下面的演讲，你还可以看看 [Brett 自己关于主题](https://www.brettklinesmith.com/blog/2018/9/22/had-talk)的博客文章。如果你感兴趣的话，他还[把他的幻灯片制作成. pptx 文件](https://www.brettklinesmith.com/s/Why-Do-It-the-Hard-Way.pptx)。

 [https://www.youtube.com/embed/O7ZtaPOkDyc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/O7ZtaPOkDyc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

