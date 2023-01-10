# 公共交通标志的私人视图

> 原文：<https://hackaday.com/2022/11/12/a-private-view-of-a-public-transport-sign/>

[Stefan Schüller]是他们所在城市苏黎世显示电车和公共汽车到站信息的 LED 标志的粉丝。[Stefan]很难找到购买标牌的来源，因此决定自己做一个。

[Stefan]决定使用 128 x 64 P2 RGB LED 屏幕重新制作 56×208 单色 2 毫米点距显示屏，并保持同样的 2 毫米点距。该显示器由利用 HUB75 RGB LED 矩阵库的 ESP32 DMA RGB LED 矩阵屏蔽驱动，所有这些都由 5 V 4 A 电源供电。

除了驱动 LED 矩阵显示器，ESP32 还会轮询苏黎世的公共交通 API，然后解析 XML 以获取相关信息。由于[Stefan]希望字体尽可能匹配，他从头开始创建了一种新字体，包括公交车和辅助功能图标。新字体被编码成字形位图分布格式(BDF)，然后被转换为与 Adafruit 的 GFX 库一起工作，由[Stefan]创建一个自定义转换工具，称为 [bdf2adafruit](https://github.com/sschueller/bdf2adafruit) ，来完成转换的最后一步。

由于 LED 矩阵具有全彩色功能，[Stefan]决定添加一点额外的装饰，并用官方电车颜色对运输线路进行颜色编码。所有的源代码都可以在他的项目的 [GitHub 仓库中找到，对于那些寻找更多细节的人来说。](https://github.com/sschueller/vbz-fahrgastinformation)

我们之前已经展示过 [DIY 构建公共交通 feeds](https://hackaday.com/2014/03/04/public-transportation-display/) 。随着低成本 RGB LED 显示屏和公共 API 的普及，希望我们能看到更多！