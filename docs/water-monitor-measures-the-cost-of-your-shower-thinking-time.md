# 水监测器测量你洗澡思考时间的成本

> 原文：<https://hackaday.com/2022/08/26/water-monitor-measures-the-cost-of-your-shower-thinking-time/>

淋浴是我们很多人最想去的地方之一，但是如果你去一个很深的兔子洞，水的浪费和水电费会有点失控。更注意他洗澡时的用水量，[GreatScott！]创造了一个生活在那里的[能量饮水监测器](https://www.youtube.com/watch?v=BNK92ep8DhY)。

该设备是围绕一个连接到他的淋浴软管的廉价 1/2”黄铜水流速传感器构建的，当一个小轮子经过内部霍尔效应传感器时，该传感器输出脉冲。数据手册不包含任何脉冲/体积规格，因此[GreatScott！]不得不通过在一个一升的容器中装满水并计数脉冲来实验性地确定这一点。他发现每升的脉冲数取决于流速，所以他缩小了变量范围，只确定了淋浴压力和流速下的平均计数。

该传感器连接到一个电池供电的 ESP8266，该 esp 8266 位于淋浴器中一个密封的 3D 打印外壳内。为了将功耗降至最低，添加了一个与流量计串联的流量开关，该开关仅在水开始流动时打开 ESP8266。一个[锁存电路](https://hackaday.com/2020/05/18/esp32-trail-camera-goes-the-distance-on-aa-batteries/)在停水后保持电潜泵通电，给它足够的时间在关闭前传输数据。对于任何连接到外部开关或传感器的电池供电项目，这种类型的电路都非常方便。

它用 [ESPHome](https://hackaday.com/2020/04/20/roll-your-own-automation-with-esphome/) 编程，将数据输出到本地[家庭助手](https://www.home-assistant.io/)服务器，所以不会有数据保存在别人的服务器上。

 [https://www.youtube.com/embed/BNK92ep8DhY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/BNK92ep8DhY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

