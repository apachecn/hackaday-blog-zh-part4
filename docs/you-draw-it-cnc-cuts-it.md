# 你画它，数控切割它

> 原文：<https://hackaday.com/2022/03/24/you-draw-it-cnc-cuts-it/>

[Jamie]又名[vector76]给我们带来了 OctoPrint 的线条跟踪插件，它可以剪切出你在一块木头上画的任何 2D 形状。该插件让你完全跳过建模步骤，直接从 CNC 安装的网络摄像头开始，[读取你的涂鸦，并给你一个 Gcode 刀具路径](https://forum.v1engineering.com/t/another-octoprint-plugin-line-tracer/31997?u=jeffeb3)作为回报。[代码在 GitHub](https://github.com/vector76/CameraTracer) 上，下面嵌入了演示视频。

[![](img/ce7ade829ad497daffe3ffc3a31dd11f.png)](https://hackaday.com/wp-content/uploads/2022/03/eb355f2bc7f9f4d5992c51836ab19e5237d4be94_2_281x500.jpeg) 在引擎盖下，OpenCV 正在做大量的图像处理，包括直线检测，以及迭代的“找到直线”和“移动工具架”步骤真正展示了计算机视觉可以做什么。它以一个基准箭头开始缩放和定向，然后它增加了场景周围的摄像头。用户可以输入常用的铣削参数:速度、进给量、切削深度、刀具偏置、铣削方向等。然后它开始工作。

目前，它仅限于没有交叉线的路径，并且可能具有良好的对比度和漂亮的暗线——所有常见的 CV 限制。但是，将网络摄像头安装到 CNC 工具头上，并使用它来解决各种路径问题，确实开辟了大量的可能性:视觉寻的、工件寻边、复制零件、定制奇怪的形状等等。这个项目显然是邀请继续黑客，开胃菜。一旦你看到[杰米]的女儿制作的女孩海盗机器人，你就会明白了。

我们已经看到类似的 OpenCV 方法用于[中心查找钻孔](https://hackaday.com/2016/12/15/zeroing-cnc-mills-with-opencv/)，但是尽管我们已经看到一些网络摄像头与激光切割机一起使用，数控铣床应用似乎在很大程度上尚未开发。如果你有其他好的例子，请在评论中告诉我们。

 [https://www.youtube.com/embed/u80e94eu4s0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/u80e94eu4s0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



谢谢[杰夫]的提示！