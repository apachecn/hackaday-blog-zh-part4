# 弯曲你的花瓶模式打印通过黑客攻击 GCode

> 原文：<https://hackaday.com/2022/02/22/bend-your-vase-mode-prints-by-hacking-the-gcode/>

来自 *CNCKitchen* 的[Stefan]想要为一个可安装在窗户上的球运行制作一些弯管，而不是拿出一些弯管模型，似乎有一种不同的方式可以让[达到期望的结果](https://www.cnckitchen.com/blog/non-planar-3d-printing-by-bending-g-code)。从一个简单的管子模型开始，他设计了一个 Python 脚本来读取 g 代码，并修改它，使其可以沿着样条路径弯曲。

花瓶模式的工作原理是，随着挤出机沿着物体轮廓缓慢提升 Z 轴，但切片过程基本上仍然相同，物体在平行于床的平面上切片。虽然这种非平面方法与水平运动同步地移动 Z 轴(尽管目前仅限于一个扭曲平面，这稍微简化了数学计算),但我们猜测它在技术上仍然是平面解决方案，但只是一个倾斜平面。但是我们跑题了，在这个上下文中，非平面仅仅意味着不平行于床，我们会用它来滚动。

[Stefan]解释说这种方法有很多困难。第一个问题是，在弯管内侧，材料流率需要按比例缩小以进行补偿。但主要问题源于挤出机本身的设计。为了平行于床进行操作，通常有一些结构以一定的角度进行操作，如风扇架和床本身。通过选择合适的机器并稍微调整一下，[Stefan]设法让它在偏离水平面 30 度的角度下工作。一个烦恼是，他的 E3D 火山酒店的库存喷嘴形状并不适合在这样的倾角下工作，所以他需要安装一个带有适配器的旧 V6 型喷嘴。经过多次调优和失败，它确实起作用了，最终目标达到了！如果你想亲自尝试一下，可以在 GitHub 的[项目中找到代码。](https://github.com/CNCKitchen/GCodeBending)

如果你想了解更多关于非平面打印的知识，我们已经介绍了[非平面切片的过程，如果你认为你的 *2.5D* 打印机没有真正时髦的打印路径，那么你可能想看看基于](https://hackaday.com/2021/03/08/3d-printing-90-deg-overhangs-with-non-planar-slicing/)[机械臂的打印机，而不是](https://hackaday.com/2021/05/25/robot-arm-adds-freedom-to-3d-printer/)。

 [https://www.youtube.com/embed/0XaaUXOwzTs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/0XaaUXOwzTs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[Keith]的提示！