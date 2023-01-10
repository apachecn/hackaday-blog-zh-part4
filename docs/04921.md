# ESP 环境传感器的印刷外壳

> 原文：<https://hackaday.com/2019/11/28/a-printed-case-for-your-esp-environmental-sensors/>

我们以前说过，但值得重复一遍:如今推出自己的硬件解决方案非常简单。如果您想制作一个网络连接环境传感器，只需将 DHT11 连接到 ESP8266 即可。是时候转向软件了。事实上，为您的硬件项目设计某种合适的机箱比组装它要花更长的时间。

这就是为什么[Pixel Hawk]为 ESP8266 和 ESP32 设计了这款[优雅的 3D 打印外壳。它旨在将微控制器放在底部隔间，而环境传感器(DHT11 或 DHT22)安装在顶部，因此它暴露在外面。外壳卡扣在一起，所以你不必担心粘合，甚至还有一个开口，所以你可以保持 USB 电缆插入。](https://www.thingiverse.com/thing:3947394)

在设计说明中，他提到在测试中确定电潜泵本身的热量会扭曲温度读数。因此，他建议尽可能让微控制器进入睡眠状态，并保持较短的读取时间，这样外壳就没有时间加热。他还创造了一个具有更多开口的替代版本，如果你需要保持芯片清醒，这应该有助于解决这个问题。

如果你正在寻找一个完整的解决方案，[Pixel Hawk]*包括了他个人用来让他的 ESP32 传感器与 Blynk 对话的源代码，但如果你不想，你当然不必走这条路。有很多现有的项目可以帮助你[开始全屋环境监测](https://hackaday.com/2017/11/20/esp8266-home-monitor-is-stylishly-simplistic/)。我们自己的[【埃利奥特·威廉姆斯】碰巧偏爱 MQTT](https://hackaday.com/2019/11/07/found-footage-elliot-williams-talks-nexus-technologies/) 当他想让他所有的小工具都玩得好的时候。*