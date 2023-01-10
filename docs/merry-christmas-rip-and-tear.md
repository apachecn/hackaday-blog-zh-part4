# 圣诞快乐！撕扯！

> 原文：<https://hackaday.com/2022/12/07/merry-christmas-rip-and-tear/>

如果你想在你的圣诞树上搞点破坏，你可以看看[Sprite_tm]的[微型电脑圣诞装饰品](https://spritesmods.com/?art=doom-bauble&f=tw)。对于 3D 打印来说，这并不是一个很高的要求，但是[Sprite]有一个独特的能力:它可以播放*末日*，正如你在下面的视频中看到的。

该设备使用 ESP32，虽然[Sprite]之前已经将标志性的 shooter 移植到微控制器上，但他决定使用更轻量级的 Game Boy 端口。这一选择有几个原因，包括蓝牙功能，这样你就可以连接控制器，这样你就可以玩游戏了。唯一的问题是他必须拔掉闪存，换上一个更大的(见下面的第二个视频)。

诚然，屏幕很小，所以这是一种新奇。但是如果你想试一试的话，[文件都在那里](https://github.com/Spritetm/esp32c3-doom-bauble)。正如你所料，还有一个微型电池和充电电路。我们可能会制作一个适配器，让它从圣诞灯充电，但这可以等到版本 2。

输入设备处理有点奇怪。蓝牙 BLE 设备将自动抓取处于配对模式的输入设备。没有使用“正常”蓝牙机制进行连接的规定。这是一个有趣的项目，你也可以用它来做一些其他的小项目。ESP32 上更大的闪光灯也有很多可能性。

如果你需要一本关于 [ESP32](https://hackaday.com/2016/10/04/how-to-get-started-with-the-esp32/) 的入门书，我们有。如果你想在真正奇怪的东西上玩*末日*，[试试七段显示器](https://hackaday.com/2022/10/29/play-doom-on-seven-segment-displays/)。

 [https://www.youtube.com/embed/u9ODhV40aEI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/u9ODhV40aEI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/11tu9p26eIA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/11tu9p26eIA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

