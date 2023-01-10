# 给奶奶发照片，不需要智能手机

> 原文：<https://hackaday.com/2022/01/21/sending-pics-to-grandma-no-smartphone-needed/>

当谈到与祖父母保持联系时，缺乏对现代技术的熟悉会成为障碍。[palmerabollo]想要与他的祖母分享照片，但发现很难，因为她没有智能手机或互联网连接来接收照片。这样，一个为奶奶定制的房子就准备好了！[(译)](https://threadreaderapp-com.translate.goog/thread/1480599629272129541.html?_x_tr_sl=pt&_x_tr_tl=en&_x_tr_hl=en-US&_x_tr_pto=wapp)

为了最大限度地减少维护需求，该建筑依靠热敏收据打印机。在需要更换之前，每卷热敏纸可以打印大约 150 张图像，因此这是一种低成本、简单的解决方案，不需要更换墨水。

一个树莓派零 2W 运行显示，搭配一顶帽子，提供蜂窝互联网连接。照片是通过电报发送的，带有一些定制的 Python 代码[，【palmerabollo】把它们放在一起。](https://github-com.translate.goog/palmerabollo/ludivina?_x_tr_sl=pt&_x_tr_tl=en&_x_tr_hl=en-GB&_x_tr_pto=wapp)该系统使用 Python“thermal printer”库，内置 Floyd-Steinberg 抖动算法，即使在简单的热敏打印机上也能获得良好的质量。

这是一个有趣的构建，让[palmerabollo]给他的祖母发送有趣的照片和信息，而不需要她做出任何努力。看到照片贴在冰箱上也超级可爱。

热敏打印机有很多乐趣，[所以不要害怕陷入自我](https://hackaday.com/2021/06/26/coding-a-custom-driver-for-the-adafruit-mini-thermal-printer/)！休息后的视频。

> 为了尽量减少维护，我选择了这个散热打印机[【https://t . co/mpkrmtrealist】](https://t.co/MPKRMtiStb)，没有墨水。他吃了长达 10 米的纸卷(约 150 张每 1 欧元的照片)，USB 连接似乎很方便，虽然最终我没有使用。[pic . Twitter . com/2 xbdrtshjo](https://t.co/2xbDRTsHjO)
> 
> —圭多(@ palmera bollo)[2022 年 1 月 10 日](https://twitter.com/palmerabollo/status/1480599689003212805?ref_src=twsrc%5Etfw)