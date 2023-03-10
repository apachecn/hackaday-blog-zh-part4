# 逐圈智能眼镜为您指明方向

> 原文：<https://hackaday.com/2020/11/14/turn-by-turn-smart-glasses-give-you-direction/>

[SamsonMarch]白天设计电子产品，显然也在业余时间从事这项工作。他的最新作品是一副非常酷的太阳镜，当他在镇上散步时，它能给他提供转弯方向。与一些智能眼镜不同，这些眼镜通过使用一个非常简单的界面来解决构建平视显示器的困难问题，该界面基于眼镜腿中你的周边视觉可见的彩色 led。

眼镜本身看起来很棒；采用 Fusion 360 设计，由木头切割而成，没有人会多看一眼。[Sam]说你也可以 3D 打印它们，但我们认为木头看起来最好，即使原料是廉价的竹砧板。他还用丙烯酸树脂切割出镜片。

[![](img/aaa44bf442ac3523f56aca2af18b5ca1.png)](https://hackaday.com/wp-content/uploads/2020/11/temple-gps-navigation-PCB.png)

不过，镜腿中的槽才是最刺激的地方。一个 iPhone 应用程序接受输入，并与苹果服务对话以获取方向。尽管手机一直试图让它进入睡眠状态，但还是花了很多心思让这个应用程序工作。每个 PCB 都有一个 RGB LED，用于指示左转/右转和目的地。它们使用 BLE 与应用程序对话，并包括加速度计，当检测到没有运动时，加速度计会将由硬币电池供电的电路板置于睡眠模式。

总的来说，这是一个有趣又好看的项目。在正常使用时，甚至有盖子来隐藏电路板。你需要复制它的文件在 GitHub 上。通常，当我们看到智能眼镜时，它们有[某种屏幕](https://hackaday.com/2019/10/22/the-futures-so-bright-i-gotta-wear-lcds/)，这更难做到。当然，不可能避免将[与谷歌眼镜](https://hackaday.com/tag/diy-google-glass/)进行比较。

> [查看 imgur.com 的帖子](https://imgur.com/JOpRmbi)