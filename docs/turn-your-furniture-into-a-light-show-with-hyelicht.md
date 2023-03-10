# 用 Hyelicht 伊莱希特将你的家具变成灯光秀

> 原文：<https://hackaday.com/2022/11/26/turn-your-furniture-into-a-light-show-with-hyelicht/>

IKEA Kallax 货架的方形形状让[Eike Hein]相信它可以从一些 RGB LED 照明中受益，虽然他*可以*简单地使用商业解决方案，但他决定开发[hye licht:一个令人难以置信的记录良好的开源照明系统，具有多个控制界面和 API](https://github.com/eikehein/hyelicht)。我们会说这是矫枉过正，但说实话，我们梦想有一个世界，每个人都把自己的个人项目提高到这个水平。

[![](img/9fca061092be3267c00585a68ed6b2b1.png)](https://hackaday.com/wp-content/uploads/2022/11/hyelicht_detail.png)

Hyelicht’s default touch UI

在样板配置中，[Eike]展示了使用图形用户界面来控制 led，该界面运行在安装在搁板侧面的 Waveshare 7”触摸屏上。这是控制 led 最直接的方式，因为触摸屏被插入到实际运行软件的 Raspberry Pi 4B 中。但是同样的界面也可以被你的智能手机或者台式机远程访问。

您也可以完全跳过 GUI，使用命令行界面来控制 led，或者使用 Hyelicht 的 HTTP REST 界面。该系统甚至可以与飞利浦 Hue 生态系统集成，如果你喜欢走这条路的话。

5×5 Kallax 货架是该项目的官方参考硬件，但当然它也可以与您可能希望用可控 led 覆盖的任何其他东西一起工作。我们在过去已经看到过类似的用于照亮储物箱的设置，但是没有一个能与 Hyelicht 提供的文档和定制可能性相提并论。如果你有给你的世界增添一点色彩的冲动，这绝对是一个需要密切关注的项目。