# 超级同步伺服轻轻摇摆

> 原文：<https://hackaday.com/2019/09/18/superbly-synchronized-servos-swaying-softly/>

led 和 blinky 项目是伟大的，可能永远不会从我们的青睐。但是你能看看这美丽的景色吗？这个迷人的展示由 36 个微型伺服系统组成，手臂上贴着部分冰棒棍。在艺术博物馆看到一个有 450 个伺服系统的巨大展示后，[道格·多姆克]受到启发，制作了一个缩小版。

什么[道格]没有按比例缩小是简单的伺服运动可以产生令人愉快的视觉效果。代码产生了一个三分钟的循环节目，越来越精彩，你可以在休息后盯着它看。在挂板后面，一个勤劳的 Arduino Uno 控制着三个 16 通道的 PWM 控制器，扫描伺服系统。我们喜欢想象除了旋转的冰棍之外的东西，像小纸风车，或者可能是为胃强壮的人准备的视错觉轮子。

你不会在视频中看到这些，但有五个超声波传感器面朝上安装在钉板的背面。[Doug]内置了可选代码，允许伺服杆跟随手的移动。我们希望他能尽快上传该功能的演示。

伺服系统既能催眠又有帮助，正如我们在[中看到的这个 114 伺服字钟](https://hackaday.com/2019/04/02/a-word-clock-the-hard-way/)。

 [https://www.youtube.com/embed/lnrVmhRN2gM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/lnrVmhRN2gM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



Via [Arduino 博客](https://blog.arduino.cc/2019/09/06/three-dozen-servos-create-animated-artwork/)