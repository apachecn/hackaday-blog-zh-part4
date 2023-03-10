# 坏掉的 3D 打印机变成了扫描显微镜

> 原文：<https://hackaday.com/2020/01/24/broken-3d-printer-turned-scanning-microscope/>

几年前，[Wayne]在试图更换风扇时炸掉了他的 Flashforge Finder 的主板。但是一个工具的死亡最终导致了另一个工具的诞生，因为他最终利用它的机械部件和一个树莓皮[创造了一个令人印象深刻的扫描显微镜](https://hackaday.io/project/169362-motorized-scanning-microscope-using-3d-printer)。

[![](img/484b5d9c02ca70f39584d83b8c477f3a.png)](https://hackaday.com/wp-content/uploads/2020/01/microscan_detail.jpg)

Scan of Ulysses S. Grant from a US $50 bill

正如你可能从名字中猜到的那样，这里的想法是用数字显微镜扫描物体，以创建整个物体的放大图像。这需要对显微镜进行非常精确的控制，而这恰恰是 3D 打印机所擅长的。所有[Wayne]需要做的就是移除热端，并打印一些适配器部件，这样他就可以在它的位置上安装 USB 显微镜。

剩下的就在软件里了。Raspberry Pi 命令步进电机在 X 和 Y 维度上移动相机，收集成千上万张单独的图像。由于显微镜的焦点是固定的，而物体的高度可能会有变化，因此 Z 载物台会上升几微米，然后再次进行扫描。一旦软件以这种方式收集了成千上万张图像，它就会对它们进行分类，找出那些对焦的图像，并将它们拼接在一起。

这个过程很慢，[韦恩]承认这不是解决问题的最有效方法。但是从 Hackaday.io 页面上的示例图片来看，我们可以说它完成了任务。事实上，看着这些 3D 物体的高分辨率扫描，我们想知道我们是否需要在 Hackaday Command Bunker 这里有一个类似的小工具。

这个项目实际上是一个早期尝试的进化，使用[挖空的光驱在](https://hackaday.com/2019/10/30/3d-scanner-for-tiny-objects-uses-blu-ray-parts/)周围移动显微镜。