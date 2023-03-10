# 把你的门铃放到互联网上的最简单的方法

> 原文：<https://hackaday.com/2020/06/01/the-easiest-way-to-put-your-doorbell-on-the-internet/>

得益于 ESP8266 和 ESP32 等支持 WiFi 的低成本微控制器，现在是部署您自己的智能家居系统的最佳时机。但这并不意味着它不会让新玩家望而生畏。如果你正在寻找一个简单的第一个项目，将你的旧学校门铃放在物联网上是一个很好的开始，但即使在这里也有一些关于如何进行的辩论。

当大多数人不得不将低压微控制器连接到驱动标准门铃的相对较大的变压器时，他们会遇到困难。我们已经看到了许多安全建立这种联系的聪明方法，但是[来自【另一个制造者】的这个提示可能是你可能遇到的最简单和最安全的方法](https://github.com/mudmin/AnotherMaker/tree/master/smart-doorbell)。

他的解决方案只需要一个感应电流传感器，通常从海外供应商那里购买不到 1 美元。门铃电路的一条腿穿过该传感器的中心，传感器本身连接到您选择的微控制器(这里还有 ESP32)。剩下的就是软件，休息之后[AnotherMaker]会在视频中解释。通过添加一点去抖代码，你的微控制器可以可靠地确定什么时候有人在按门铃按钮；之后你如何处理这些信息取决于你自己。

如果你担心这种方法太简单*[你可以用光耦合器](https://hackaday.com/2019/10/21/an-optocoupler-doorbell-notifier/)试试，或者也许[把低压交流电转换成你的微控制器可以处理的东西](https://hackaday.com/2019/08/06/sniffed-transformer-puts-wired-doorbell-online/)。*

 *[https://www.youtube.com/embed/p596PnCCIX0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/p596PnCCIX0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

*