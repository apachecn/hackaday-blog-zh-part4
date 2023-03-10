# 用 Hm-panelizer 图形化面板 PCB

> 原文：<https://hackaday.com/2022/05/31/panelize-pcbs-graphically-with-hm-panelizer/>

当你在中国的晶圆厂处理 PCB 和生产单件产品时，无论你喜欢什么样的 PCB 布局工具，从布局到可制造的 Gerber 文件只需按几下按钮。但是，一旦你开始生产构成一个更大系统的多组 PCB，或者为了高效制造而制作多份副本，那么不深入研究 PCB 面板艺术，你就不会走得太远。这些年来，我们已经看到了一些选项，这里还有一个看起来很有前景的选项——[hm-panel izer by[half marble]](https://github.com/halfmarble/hm-panelizer)是一个跨平台的 Python GUI 应用程序，它利用了 [Kivy](https://kivy.org/#home) ，所以它应该可以在大多数主要平台上运行得很好，没有太多麻烦。该工具还处于早期开发阶段，因此目前仅限于处理 PCB 的直边，带有水平鼠标咬痕，但我们确信，只要有时间和支持，它将很快发展出更通用的功能。

在一个理想的世界中，像 KiCAD 这样的开源工具应该有一个内置的 panelizer，但是现在我们可以梦想，hm-panelizer 可能对某些人来说已经足够好了。想要更多关于面板的选择，请查看我们的指南，让它变得简单，这里有另一种方法，T2。