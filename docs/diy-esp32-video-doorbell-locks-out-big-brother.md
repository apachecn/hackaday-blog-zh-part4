# DIY ESP32 视频门铃锁出大哥

> 原文：<https://hackaday.com/2020/12/22/diy-esp32-video-doorbell-locks-out-big-brother/>

毫无疑问，从电脑或移动设备上看到谁在你家门口是很方便的，这就是为什么目前市场上充斥着视频门铃。不幸的是，并不总是清楚还有谁可以访问这些设备拍摄的图像。电子前沿基金会(Electronic Frontier Foundation)等组织认为，通过在前门安装这些联网摄像头，消费者在不知不觉中为一个大规模监控系统做出了贡献，该系统很容易被用来对付他们。

幸运的是，有一个解决方案。正如[Sebastian]在他的最新项目中所展示的，你可以[构建自己的视频门铃，复制商业产品的功能](https://smartsolutions4home.com/ss4h-sd-smart-doorbell/)，同时通过利用开源、社区开发的项目，如 ESPHome 和 Home Assistant，确保你是唯一能够访问数据的人。与此同时，像桌面 3D 打印和低成本 PCB 制造这样的现代制造技术意味着你的 DIY 门铃不必像你自己做的一样*。*

[![](img/51554cc4e7f7e83ad7ec8376a677be2a.png)](https://hackaday.com/wp-content/uploads/2020/12/espvidbell_detail.jpg) 该项目从一个定制的 PCB 开始，它结合了 ESP32、摄像头模块、电容式触摸传感器、可选地触发电子门锁的继电器和 DC-DC 转换器，使您可以从广泛的输入电压为设备供电。该板甚至有一个位置，您可以为 ESP32 焊接一个额外的 8 MB 外部 PSRAM，这将使芯片能够捕捉更高分辨率的视频。

电子设备被安置在一个极简的 3D 打印外壳中，可以与 Ring 和 Arlo 等类似设备放在一起；尤其是如果你有一个数控系统，可以把面板从丙烯酸材料上切下来。发光的触摸传感器看起来非常出色，并真正赋予设备专业的感觉。也就是说，如果暴露在恶劣的天气下，这种情况看起来不会持续很长时间，而且这种方法存在一些明显的物理安全问题。但是平心而论，[我们已经在商用硬件](https://hackaday.com/2020/07/01/pop-open-your-neighbors-front-door-with-12-volts/)上看到了同样的问题。

自然，对于这样的项目，硬件只是故事的一半。要让移动设备通知之类的东西正常工作，需要相当多的软件，另外一个特别麻烦的是，根据你的小工具运行的操作系统是哪家 MegaCorp 生产的，这个过程是不同的。[Sebastian]已经在休息后的视频中记录了大部分过程，但细节可能需要一些调整，这取决于您希望如何设置。

这肯定是一个非常令人印象深刻的项目，但如果整个光滑的未来主义外观不是你的风格，你可以选择 DIY 视频门铃，它看起来像来自 1986 年的虚拟现实版本。

 [https://www.youtube.com/embed/P4HT_PlZKZg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/P4HT_PlZKZg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

