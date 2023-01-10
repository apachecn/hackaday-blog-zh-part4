# 用光作画:自制的像素棒

> 原文：<https://hackaday.com/2019/10/16/painting-with-light-the-homemade-pixelstick/>

光线绘画长期以来一直是长曝光摄影师的作品，但当你用人类主题进行光线绘画时，高分辨率通常是不可能的。

来自[Timmo]的这个周末项目使用一个基于 ESP8266 的微控制器和一个基于 WS2812 的可寻址 LED 条来在稀薄的空气中描绘文字或自定义图像。它实际上是基于 Pixelstick 的，pixel stick 是专业摄影师用来设置动画和照片真实感镜头的工具。设置光绘棒所需的设备多达数百台，更不用说所需的专业相机和镜头了。然而，比起和你的朋友挥舞手电筒，这是一个巨大的进步。

对于业余摄影师和业余爱好者来说，LED Lightpainter 将 Pixelstick 降低了几个等级。它直接支持 24 位 BMP，无需转换。图像存储在闪存内部，并通过网络界面上传。led 的数量、图像行的时间和无线连接的 STA/AP 模式的设置也由 web 界面设置。该项目使用 [Adafruit NeoPixel](https://github.com/adafruit/Adafruit_NeoPixel) 、 [ArduinoJson](https://github.com/bblanchon/ArduinoJson) 和[博德莫尔的 TFT_HX8357](https://github.com/Bodmer/TFT_HX8357/tree/master/examples/Draw_SDCard_Bitmap) 库来实现 BMP 绘图代码，这也允许在将代码上传到微控制器之前进行图像预览。图像是从底行到顶行绘制的，因此图像必须在更新到 LED painter 之前进行转换。

该项目计划的一些未来改进包括 TFT/有机发光二极管支持、LED 中的彩虹或颜色渐变图案，以及用于支持动画的加速度计或陀螺仪支持。

目前没有太多的 DIY LED 光画画廊，但我们希望在未来看到一些定制的光画方法。

如果你对这种东西感兴趣，这不是我们见过的第一个 LED 荧光棒。