# 蜂鸟、3D 打印和深度学习

> 原文：<https://hackaday.com/2018/08/31/hummingbirds-3d-printing-and-deep-learning/>

在你的花园里设置照相机陷阱来观察附近的野生动物是很受欢迎的。但(克里斯·拉姆)心中只有一个主题:蜂鸟。他[设计了一个定制设置](https://medium.com/@kakittwo/what-do-you-get-when-you-mix-sugar-water-3d-printing-and-deep-learning-39de7b3f5f0e)来使用一些简洁的技术捕捉他想要的镜头。

为了吸引蜂鸟，[克里斯]使用了现成的喂食器——没有必要重新发明轮子。为了获得所需的特写镜头，使用了 4K 动作摄像机。这是用[克里斯]设计的 3D 打印支架固定在喂食器上的。

当谈到检测视频中蜂鸟的存在时，有各种方法可以考虑。在硬件方面，PIR 和超声波距离传感器在这类项目中很受欢迎，但[Chris]想要一个纯软件解决方案。这类项目常用的运动检测库可能已经倒在这里了，因为整个馈线在空中摆动，所以[Chris]选择了机器学习。

RESNET 架构用于对每一帧进行分类，以确定图像中是否包含蜂鸟。最初的尝试不太成功，但在将图像裁剪到喂食器周围的较小区域后，分类准确度大大提高了。经过一点 FFmpeg 的魔法，被选中的片段被连接成一个包含所有有趣部分的视频；休息后，您可以在剪辑中看到结果。

机器学习和野生动物摄像头似乎是天作之合。我们已经写了一个概念验证项目，当检测到运动时[识别镜头中的不同动物。](https://hackaday.com/2017/06/14/hackaday-prize-entry-automated-wildlife-recognition/)

 [https://www.youtube.com/embed/pUyAH3iF_zU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/pUyAH3iF_zU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

