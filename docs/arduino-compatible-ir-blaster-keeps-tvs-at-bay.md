# 兼容 Arduino 的红外线增强器让电视远离你

> 原文：<https://hackaday.com/2021/06/08/arduino-compatible-ir-blaster-keeps-tvs-at-bay/>

TV-B-Gone 是黑客圈子里一个众所周知的工具:只需在公共场所将它对准一台嘈杂的电视，按下按钮，它快速连续闪烁的数百个红外遥控代码中的一个就很有可能得到预期的响应。不幸的是，虽然这是一个简洁的谈话开场白，但它的实际用途仅限于一个功能。但这款可编程红外开发板却并非如此，它的创造者【乔尔杰·曼迪克】将其描述为“服用了类固醇的电视”。

当然，你可以将它对准一台随机的电视，只需按一下按钮就可以关闭它，但你也可以将该板插入你的计算机，并通过其 CP2104 芯片提供的串行连接直接控制它。使用简单的纯文本控制协议，用户可以修改器件的行为并监控其状态。[Djordje]设想这一功能与智能手机应用程序结合使用，用于秘密应用。为此，该设备对板载电池的支持应该可以防止它在长时间操作期间耗尽手机。

当然，你也可以通过启动 Arduino IDE，并为该设备的 ATmega328P 微控制器编写一些新代码，完全用它来做其他事情。[正如我们几个月前看到的支持红外的 ESP8266 开发板一样](https://hackaday.com/2021/04/23/this-esp8266-dev-board-has-a-surprising-story-behind-it/)，一体式开发板有很多应用，可以让您与各种红外设备进行通信。

 [https://www.youtube.com/embed/KtAopdu8X34?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/KtAopdu8X34?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

