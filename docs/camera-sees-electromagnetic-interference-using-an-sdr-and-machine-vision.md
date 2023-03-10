# 摄像机使用 SDR 和机器视觉发现电磁干扰

> 原文：<https://hackaday.com/2019/04/30/camera-sees-electromagnetic-interference-using-an-sdr-and-machine-vision/>

知道你的设备正在泄漏电磁干扰(EMI)是一回事，但如果你真的想解决这个问题，知道*辐射来自哪里*可能会有所帮助。[这款热图电磁干扰探测器](http://charleslabs.fr/en/project-Electromagnetic+interference+mapping)将会很有型地回答这个问题。它使用网络摄像头来记录 EMI 探针，并在图像上叠加干扰热图。

老读者会注意到，[Charles Grassin]的 EMI 映射器的硬件端与我们最近介绍的由半刚性同轴电缆制成的 EMC 探头非常相似。作为昂贵的现成电磁测试探针组的廉价 DIY 替代品，该探针超级简单:只是一个半刚性同轴跳线，一个 SMA 插头被砍掉，原始端回环并焊接。连接到 SDR 加密狗，探针被证明有助于追踪噪声电路。

[Charles]的项目更进了一步，增加了一个可以俯视被测设备的摄像头。OpenCV 用于跟踪探头，探头在增强现实显示器的帮助下在 DUT 上空手动移动，增强现实显示器有助于跟踪覆盖范围，Python 脚本记录了探头的位置和射频功率测量值。下面的视频显示了捕获过程，以及在设备顶部重新组合成覆盖图时数据的样子。

即使 EMC 测试不是你的菜，但对好奇的人来说，这一项似乎很有趣。[Charles]友好地[在 GitHub](https://github.com/CGrassin/EMI_mapper)上提供了源代码，所以这是一个很好的项目，只需快速完成并开始绘制即可。

 [https://www.youtube.com/embed/O3-pH8tdrgA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/O3-pH8tdrgA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[via[RTL-SDR.com](https://www.rtl-sdr.com/using-an-rtl-sdr-and-opencv-to-create-an-emi-heatmap-of-circuit-boards/)