# 智能手机应用程序使用 AR 来可视化射频频谱

> 原文：<https://hackaday.com/2019/01/09/smartphone-app-uses-ar-to-visualize-the-rf-spectrum/>

你是否曾希望能看到无线电频谱的射频部分？虽然这种技能可能会让你晚上很难睡个好觉，但它至少可以让你立即看到 WiFi 覆盖范围内的盲点。不错的交易。

![](img/9ad880b257690935edca0470489390a6.png)不愿全力以赴的【Geordi La Forge】为了能够可视化射频，【Ken Kawamoto】为他的智能手机打造了一款次佳产品——[增强现实射频信号强度应用](https://kenkawakenkenke-en.hatenablog.com/entry/2019/01/06/231619)。该应用程序旨在帮助他在节后清理中重新定位路由器，它使用 Android ARCore 框架来计算手机在房子中的位置，并在当前相机图像上覆盖一个代表传感器数据的彩色编码球体。这些球体在 3D 空间中持续存在，留下一串虚拟的面包屑，当你在房子里走动时，这些面包屑会绘制出传感器数据。该应用程序还可以让你绘制蓝牙和 LTE 覆盖范围，但射频不是它的唯一输入:如果你的手机配备正确，磁场和气压也可以被 AR 绘制。我们发现下面视频中的蓝牙演示特别有趣；双层铝箔对信号的衰减程度令人惊叹。[Ken]甚至设计出了一款带有气体传感器的 Arduino，它可以与手机对话，并绘制厨房炉灶周围的气氛。

这款应用名为 [AR Sensor](https://play.google.com/store/apps/details?id=com.ken.arsensor) ，在 Play Store 上有售，但你至少需要 Android 8.0 才能玩。如果你的手机像我们的一样落后于时代，你可能不得不满足于[艰难地绘制你的射频世界](https://hackaday.com/2018/06/20/desktop-radio-telescope-images-the-wifi-universe/)。

> 亚伦·布鲁图特(arlan blue tooth)~嘿~嘿~嘿~嘿~嘿~嘿~嘿~嘿~嘿~嘿~嘿~嘿~嘿~嘿~嘿~嘿~嘿~嘿~嘿~嘿~嘿~嘿~嘿~嘿~嘿~嘿~嘿~嘿~嘿~嘿~嘿~嘿~嘿~嘿~嘿
> 
> — Ken Kawamotoï¼ˆã‚¬ãƒªã®ã»ã†ï¼‰ (@kenkawakenkenke) [December 30, 2018](https://twitter.com/kenkawakenkenke/status/1079385558751690753?ref_src=twsrc%5Etfw)