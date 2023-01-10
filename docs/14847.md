# 机械拾色器为您输入十六进制代码

> 原文：<https://hackaday.com/2022/09/21/mechanical-color-picker-types-hex-codes-for-you/>

十六进制代码是在数字媒体中指定颜色的一种简单、明确的方式。然而，对于没有实践经验的人来说，从你头脑中的一种颜色到一个十六进制代码可能是困难的。[【盖伊·杜邦】造了一个小玩意，名叫表盘调色剂，替他做](https://twitter.com/gvy_dvpont/status/1569807637637922819) ( [尼特](https://nitter.net/gvy_dvpont/status/1569807637637922819))。

刻度盘碳粉每个颜色通道有两个刻度盘-红色、绿色和蓝色。通过旋转转盘，人们可以在 8 位 RGB 颜色空间中选择给定的颜色，然后该颜色会显示在设备自带的 RGB LED 上。选择后，可按下按钮将所选颜色的十六进制代码输入文本框。拨号碳粉运行在小啊 RP2040 微控制器板上，并用 CircuitPython 编码。

[Guy]希望将来能在 Etsy 上销售表盘墨粉，甚至正在为打印爱好者开发 CMYK 版本。我们以前也在这里介绍过【盖伊】的作品，以[他的扩展播放 HitClips 弹夹的形式。](https://hackaday.com/2022/01/10/hitclips-custom-cartridge-hack-will-never-give-up-let-down-or-turn-around/)休息后的视频。

> 特点:
> –非常容易点击的旋钮/按钮
> –内置从十六进制到 RGB、CMYK、HSV
> 的对话–就是这样，但是没有 pic.twitter.com/swR7sKlFzY
> 
> —盖伊·杜邦(@ gvy _ dv pont)[2022 年 9 月 13 日](https://twitter.com/gvy_dvpont/status/1569808042476158978?ref_src=twsrc%5Etfw)