# 最小的 ESP8266 数码相框

> 原文：<https://hackaday.com/2020/03/01/a-minimal-esp8266-digital-picture-frame/>

在过去的几年里，一个好的数码相框的价格已经下降到我们不再经常看到 DIY 版本了。尽管我们可能不愿意承认这一点，但当规模经济已经让你可以以低于零件本身的成本购买最终产品时，很难证明自己制造东西是合理的。但是当然，总有一些边缘情况下[建造它可能是得到你需要的东西的唯一途径](https://www.instructables.com/id/Cheap-Cute-PhotoFrame-Without-SD-Card-on-ESP8266-1/)。

[![](img/4ff7f5489654c5158eae1a1c744138a6.png)](https://hackaday.com/wp-content/uploads/2020/02/espframe_detail.jpg) 诚然，我们不确定【托尼·刘】*是否真的需要*一个 1.8 英寸的数码相框，但我们肯定有人需要。这个项目用的 ST7735R 显示器是真的 TFT，所以色彩和刷新率还算不错；但由于分辨率仅为 128×160，我们建议您降低对视觉保真度的期望。

这个项目真正有趣的地方在于零件数量有多低。您所需要的只是 ST7735R 显示器和 ESP8266 本身(当然也可以是您选择的开发板)。甚至 3D 打印框架在技术上也是可选的。显示器由 SPI 驱动，因此增加电源后，两个器件之间只需焊接八根导线。如果你正在寻找一种简单的方法来将照片幻灯片添加到一个小设备上，比如一个会议徽章，这是非常简单的。

但是图像是从哪里来的呢？你可能会想到 SPIFFS，但是在这个例子中[Tony]已经将图像转换为位图，并使用 PROGMEM 将它们作为头文件加载到 Arduino 草图中。有帮助的是，他提供了他用来将图像转换成图形库可以理解的数组的工具的链接。这使得添加新的图像有点耗时，但是我们认为如果你需要这样的东西，它可能只会显示一组非常特定的图像。

如果你正在寻找更大的东西，或者仅仅是一个让那个满是灰尘的树莓派派派上用场的借口，你可能会对[感兴趣，这是我们这些年来看到的更有实质性的构建之一](https://hackaday.com/2018/03/05/shoot-and-forget-digital-photo-frame/)。

 [https://www.youtube.com/embed/2yeeBgClBrs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/2yeeBgClBrs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

