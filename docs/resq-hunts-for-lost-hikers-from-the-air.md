# RESQ 从空中搜寻失踪的徒步旅行者

> 原文：<https://hackaday.com/2020/08/12/resq-hunts-for-lost-hikers-from-the-air/>

当在偏远地区徒步旅行迷路时，手机似乎不是最有用的工具。没有手机网络的信号，就不可能打电话求救。然而，携带手机可能会让救援人员更容易找到你，[，【埃里克】正在开发一种工具来完成这项工作。](https://hackaday.io/project/172090-resq-search-and-rescue-tools)

![](img/f9136afb482bb309d4b7aecff24182d6.png)

The handheld version of ResQ features a directional Yagi antenna to help pinpoint the location of the signal.

[Eric]的项目名为 ResQ，旨在通过检测手机 WiFi 适配器发出的信号包来寻找迷路的徒步旅行者。该项目有两种形式:一个带有定向八木天线的手持装置，以及一个可以飞越地形扫描信号的无人机安装装置。

ResQ 是围绕 ESP8266 构建的，ESP8266 是一种构建自定义 WiFI 扫描仪的廉价且可行的方法。目前，该系统能够检测 WiFi 设备，并将 MAC 地址以及时间戳和 GPS 位置数据记录到 SD 卡中，以帮助救援人员找到迷路的人。未来的计划包括给无人机增加一个实时下行链路，这样任何 pings 都可以被实时报告给救援人员进行调查。

类似的系统在商业上也存在，主要使用手机信号而不是 WiFi。然而，对于许多组织来说，成本高得令人望而却步，因此我们可以将 ResQ 视为一种有用的工具。我们以前也展示过其他用于搜救的无线电设备。休息后的视频。

 [https://www.youtube.com/embed/FxJkW-vr78s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/FxJkW-vr78s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[hack adayprize 2020](https://prize.supplyframe.com)主办单位:[![Supplyframe](img/193ca31946d20fcfa39296cb816a4c50.png)](https://supplyframe.com/)[![Digi-Key](img/4fc24a8a6b4498aecfe987b00009d192.png)](https://www.digikey.com/)[![Microchip](img/8dd361210bbb0e5592c24f87e4e2267e.png)](https://www.microchip.com/)