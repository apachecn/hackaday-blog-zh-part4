# 抗击家庭空气污染

> 原文：<https://hackaday.com/2019/09/24/fighting-household-air-pollution/>

当肯尼亚工程师[Aloise]发现家庭空气污染的健康风险时，他们知道必须有一个聪明的解决方案来解决这个问题，同时仍然为没有清洁燃料的家庭烹饪提供合理的能源。进入 [OpenHAP](https://hackaday.io/project/166510-openhap) ，这是一个 DIY 家用空气污染监测器，为公民科学家提供并研究测量发展中国家空气微粒的方法。

![](img/a79a697f05306f7dd148274780e11d9a.png)

该装置基于通过 UART 与 ZH03B 颗粒物质传感器通信的 ESP32I2C 上空的 DS3231SN 实时时钟(RTC)、温度和湿度传感器以及 MLX90640 2D 热传感器阵列；以及将接收到的数据无线发送到蓝牙低能量腕带信标和具有互联网功能的电话。该器件还使用 TCA9534 GPIO 扩展器来控制视觉和听觉通知器(蜂鸣器和 led ),并与 SD 卡接口。

该项目使用为网络服务器的 [ESP32](https://github.com/chmorgan?tab=repositories) 修改的 [libesphttpd 项目](https://github.com/chmorgan/libesphttpd)，该项目使用 ESP32 的 WiFi 功能将数据传输到移动手机或计算机。这些数据包括实时传感器信息、系统状态、存储介质状态、热阵列传感器数据的可视化(以确保相机面向热源)，以及测试蓝牙标签在距离方面的限制的标签信息。

电源输入通过微型 USB 连接器提供，由串联的 TVS 二极管和肖特基二极管保护，以防止反向功率流。

该项目在两个真实场景中进行了测试:一个是肯尼亚农村的一个家庭，另一个是城市低收入的四口之家。在第一次测试中，这个家庭使用了一个三石的明火炉子。前视红外热感相机捕捉到了炉子的温度，而标准相机足以捕捉到厨房内的高浓度烟雾。OpenHAP 的读数足够高，超过了颗粒传感器的上限检测阈值，表明在家里做饭的女人每天接受的量相当于 8 支香烟，大约是世卫组织推荐颗粒水平的 8 倍。

 [![openhap stove](img/567a4eb76e83212be49d41d9d0893908.png "openhap stove")](https://hackaday.com/2019/09/24/fighting-household-air-pollution/openhap-stove/)  [![openhap connecting device](img/8e02bed5c1624df675dd6a8954f5cd42.png "openhap connecting device")](https://hackaday.com/2019/09/24/fighting-household-air-pollution/openhap-1/) 

在第二个家庭中，木炭煤球和煤油的典型混合能源通常用于烹饪，白天使用煤油，晚上使用煤球。使用 OpenHAP 测量污染水平的结果表明，该家庭中的母亲和孩子经常受到大约 1.5 倍建议限值的污染物，足以导致慢性窒息。

这个项目已经有巨大的潜力来帮助研究人员测试农村家庭的不同能源，更不用说为公民科学家提供便携式低能耗污染监测器的优势了。

 [https://www.youtube.com/embed/QYEUmKjlSp0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/QYEUmKjlSp0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



The [HackadayPrize2019](https://prize.supplyframe.com) is Sponsored by: [![Supplyframe](img/79a7db035b8a2b6c2b7b0895c45b7de8.png)](https://supplyframe.com/)  [![Digi-Key](img/ba094a14c430ab81591a2abdc54a5363.png)](https://hackaday.io/digikey)  [![Microchip](img/5023ef0b7ff1aee311cba9b54a3ac9fe.png)](https://hackaday.io/microchip)