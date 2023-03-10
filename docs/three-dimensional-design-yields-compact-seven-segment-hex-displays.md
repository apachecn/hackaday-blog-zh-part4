# 三维设计产生紧凑的七段六边形显示器

> 原文：<https://hackaday.com/2021/11/11/three-dimensional-design-yields-compact-seven-segment-hex-displays/>

从最简单到最复杂的计算机，如果不能向用户提供反馈，就没有多大用处。无论这个接口是监视器、扬声器还是简单的 LED，几乎总会有某种输出。其中最普遍的是一直存在的七段显示器。它们很小，很容易使用，也许最重要的是，它们很便宜。

虽然显示器本身相对紧凑，但它们通常需要某种驱动电路——在正确的引脚上将数字转换为电压。这些驱动器会占用宝贵的空间，尤其是在试验板上，有时会使使用七段显示器变得很麻烦。谢天谢地，[约翰·朗尼根]有一个很好的解决方案:[完全位于显示器下方的驱动板](https://hackaday.io/project/178227-dual-7-segment-hex-display-module)。他的双七段十六进制显示器项目是出于需要——他需要它用于[试验板 CPU SPAM-1](https://hackaday.com/2021/11/06/spam-1-is-a-well-documented-discrete-cpu-with-an-impressive-software-library/) ，它变得有点太笨重了。每个模块是两个位于小型 PCB 上的七段显示器。在显示器下面是一个 8 位 PIC 微控制器，它充当两个显示器的驱动器。

在进行电子设计时，我们很容易局限于二维思维——即使是设计多层 PCB，也常常感觉像是在几个不同的二维区域而不是一个三维区域工作。堆叠组件以节省空间的概念虽然实现起来相当简单，但却是我们在 Hackaday 上喜欢看到的解决问题的一个很好的例子。当然，如果你喜欢 3D 电路设计的想法，你必须看看[一些我们在过去](https://hackaday.com/2020/11/20/no-wonder-these-projects-won-the-circuit-sculpture-contest/)展示过的不可思议的电路雕塑。

 [https://www.youtube.com/embed/8fGcgFgZOEk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/8fGcgFgZOEk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

