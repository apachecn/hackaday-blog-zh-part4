# 立体 3D 电视来了！

> 原文：<https://hackaday.com/2021/02/21/volumetric-3d-television-is-here/>

无需特殊眼镜即可观看完整 3D 图像的立体 3D 显示器在我们的社区中并不少见，通常采用 3D LED 矩阵或旋转转子的形式，其上投影有图像或固定有 LED 阵列。它们是令人印象深刻的项目，但是它们能够展示的内容通常是有限的。漂亮的图案和简单的 3D 模型都很好，但它们几乎不是 3D 电视。因此，我们对[Evlmnkey]的学士学位项目[印象深刻，该项目将动作捕捉和立体显示结合起来，用于真正的立体 3D 闭路电视系统](https://www.reddit.com/r/arduino/comments/lmtdf9/this_is_my_take_at_a_hologram_for_my_bachelors/)。

寻找细节需要通过 Reddit 线程进行一些挖掘，但显示器是由 ESP32 驱动的现成 Adafruit 单面 LED 矩阵，所有这些都安装在一个带有一对滑环的电机上。数据通过 WiFi 传输到 ESP，由负责抓取图像的 PC 以未压缩帧的形式发送。关于 3D 捕捉的细节很少，但因为他提到了 Kinect 库，我们怀疑这可能是来源。

这可能不是你见过的分辨率最高的电视，事实上我们会把它比作 20 世纪 30 年代闪烁的 30 行机械电视，但它仍然是一个功能齐全的 3D 直播闭路电视系统。如果你对 3D 显示器感兴趣，你可能想看看我们对主题的研究[。](https://hackaday.com/2019/01/09/three-dimensions-what-does-that-really-mean/)

感谢[nandkeypull]的提示。