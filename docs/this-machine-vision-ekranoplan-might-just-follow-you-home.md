# 这台机器视觉里海怪物可能会跟着你回家

> 原文：<https://hackaday.com/2022/04/29/this-machine-vision-ekranoplan-might-just-follow-you-home/>

什么东西既不是飞机也不是船，但兼有两者的特征？可能有很多东西符合这种描述，但[尼克·雷姆]正在研究的一种被称为 ekranoplan。具体来说，他希望让[这种贴地滑行的地效飞行器能够自主运行](https://www.youtube.com/watch?v=uaY2G5Kbj_g)。

如果你认为你以前在这里听说过 ekranoplan，那你就对了——我们已经报道了一个很酷的激光雷达控制的 ekranoplan 模型，它是[rctestflight]大约一年前开发的，最近，[ThinkFlight]试图让[成为一个可以跟在船后面的自主 ekranoplan](https://hackaday.com/2021/10/10/autonomous-ground-effect-vehicle-demonstrator-aims-to-speed-up-maritime-shipping/)。后者是[Nick]参与合作的地方，下面视频中显示的轻量级泡沫地效飞行器是他的测试平台。

在整理了基本的机身设计并集成了激光雷达后，他将注意力转向了自主位，它依赖于一台运行 ROS 的 Raspberry Pi 4 和一台带有广角镜头的相机。Pi 使用机器视觉算法来寻找场景中的“AprilTag”基准标记，这给飞行控制器提供了关于 ekranoplan 与标记的相对方位的信息。[Nick]使用电子长板测试了标签跟踪，ekranoplan 模型做了令人钦佩的工作，不仅管理了地面效应，还保持了他身后的目标。向尼克致敬，他让所有的球都保持在空中，并且没有在这个过程中折断他的脖子。

我们期待着看到[尼克]在这里建造的东西最终成为[ThinkFlight]的大型 ekranoplan 版本。不可否认，像这样的地效飞行器很酷，看起来它们有潜力解决一些有趣的交通问题。

 [https://www.youtube.com/embed/uaY2G5Kbj_g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/uaY2G5Kbj_g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

