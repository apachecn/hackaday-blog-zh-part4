# ESP32 变成了 NRF52 芯片的便携式 SWD 闪光灯

> 原文：<https://hackaday.com/2021/07/01/esp32-turned-handy-swd-flasher-for-nrf52-chips/>

有需要闪存的 nRF52 或 nRF51 设备吗？有一个 ESP32 放在周围收集灰尘？如果是这样，那么固件黑客 extra ordinaire[【Aaron Christophel】有你需要的开源代码](https://github.com/atc1441/ESP32_nRF52_SWD)。他的新项目允许经济实惠的支持 WiFi 的微控制器通过其 SWD 接口读写 Nordic nRF52 系列芯片的内部闪存。只要你有一些跳线和一个网络浏览器，你就可以了。

[![](img/909730119b144b08132a25ff10b8e69f.png)](https://hackaday.com/wp-content/uploads/2021/06/esp32swd_detail.jpg) 在下面的第一个视频中,【Aaron】演示了使用 PineTime 智能手表的技术，但无论你的目标设备是什么，过程都或多或少是相同的。只需将 CLK 和 DIO 线连接到 ESP32 的 GPIO 21 和 GPIO 19 引脚，将您的网络浏览器指向其在本地网络上的地址，您就会看到一个简单的用户界面，用于读写芯片的闪存。

如第二个视频所示，通过增加几根导线和一个 MOSFET，ESP32 固件还能够利用芯片上的电源故障，即使启用了 APPROTECT 功能，也可以读取其闪存的内容。[Aaron]并没有因为这种技术而获得任何荣誉，而是指出[LimitedResults]进行的[研究解释了攻击的具体细节](https://limitedresults.com/2020/06/nrf52-debug-resurrection-approtect-bypass-part-2/)。

当一条来自 Aaron 的消息到达收件箱时，我们总是很兴奋，因为更多时候这并不意味着另一个设备已经收到了开源固件替换。[从他早期的廉价健身追踪器](https://hackaday.com/2019/02/20/custom-firmware-for-cheap-fitness-trackers/)到他的[大获成功的蓝牙环境传感器黑客](https://hackaday.com/2020/12/08/exploring-custom-firmware-on-xiaomi-thermometers/)，我们不认为这家伙见过他不想立即发送给`/dev/null`的股票固件。

 [https://www.youtube.com/embed/Iu6RoXRZxOk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Iu6RoXRZxOk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/tMPD0kBG_So?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/tMPD0kBG_So?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

