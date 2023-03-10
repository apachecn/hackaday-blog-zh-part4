# 用网络浏览器替换您的红外遥控器

> 原文：<https://hackaday.com/2020/10/28/replace-your-ir-remote-with-a-web-browser/>

虽然越来越多的消费产品争相加入 WiFi 和蓝牙连接，但红外线的简单性和可靠性使其在游戏中的存在时间远远超过了许多人的想象。尽管更薄、更时尚，但您的全新智能电视附带的红外遥控器与我们在 20 世纪 80 年代使用的遥控器并无本质区别。

但这并不意味着红外设备不能享受一些现代的便利。厌倦了把遥控器放错地方，[[马赛丽·卡拉诺维奇]决定想出一个方法来模仿它](https://github.com/SasaKaranovic/esp32_wifi_remote)通过网络控制他的电视。现在，除了在手机或电脑上安装一个网络浏览器之外，他再也没有什么新奇的东西了，他可以在家里的任何地方点击遥控器的可视图标来控制电视。正如你所料，这个项目可以很容易地适应控制任何红外小工具，你可能有想法。

[![](img/069f0947a06bb88981ef6e4dc11ca7a9.png)](https://hackaday.com/wp-content/uploads/2020/10/espremote_detail.jpg)

Assembling a simple IR transmitter dongle.

诚然，这并不完全是一个新的突破。过去，我们已经看到许多人提出了类似的 IR 网关，只是复杂程度不同。但我们真正喜欢这个项目的是，[马赛丽]不仅分享了将 ESP32 变成网络控制的红外发射器的源代码，而且他还制作了一个简洁的视频，演示了如何轻松地旋转自己的版本。看起来像传统红外遥控器的 3D 打印外壳也是一个不错的触摸。

这个项目的硬件只不过是一个 ESP32 开发板和一个 LED，但如果你正在寻找一些更有针对性的东西，我们最近看到了一个非常光滑的开放式硬件 IR 网关，可能会满足你的需求。

 [https://www.youtube.com/embed/XKWTu5t2lUA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/XKWTu5t2lUA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

