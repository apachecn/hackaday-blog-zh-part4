# 观看 Blender 插件制作动画 PCB 轨迹(以及更多)

> 原文：<https://hackaday.com/2021/11/30/watch-blender-plugin-make-animated-pcb-traces-and-more/>

[Staacks]的 [Blender 插件动画增长](https://there.oughta.be/a/blender-plugin-to-animate-growth)是后面的甜蜜动画上面看到的。这是一个附加软件，当使用[搅拌机](https://www.blender.org/)时，它巧妙地使创建光滑的生长动画变得更加容易。它也不局限于 PCB 图像，尽管它们恰好是这个过程的一个很好的例子。

![](img/182df67fca691e2bd9e5aed3e879af8d.png)

The add-on isn’t limited to animating PCB traces.

这个想法是从一个图像纹理开始，它有一个显示一串路径的结构(像一个迷宫，或者 PCB 上的轨迹)，并被用作输入。然后，该插件使用路径查找算法来确定这些路径如何从原点开始增长，并将相关数据存储在输出图像的颜色通道中。该输出在 Blender 中进一步用作生成实际动画的参数，从而生成如上所示的整洁的自创建 PCB。顺便说一句，那块 PCB 不只是用来展示的。是【Staacks】的[智能门铃项目](https://there.oughta.be/a/smart-doorbell)的 PCB。

Blender 是一个非常全面的建模和动画工具，虽然我们已经介绍过使用它来创建高质量的 KiCad 渲染，但这种动画确实是另一回事。

如果你有兴趣尝试一下，这里是 Blender 增长工具的 GitHub 库。如果您想先了解更多，请观看下面嵌入的视频，了解它的功能和工作原理。

 [https://www.youtube.com/embed/2a2vZFN38zk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/2a2vZFN38zk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

