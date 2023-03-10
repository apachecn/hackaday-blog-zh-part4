# 智能喷头的太阳能史蒂文森屏

> 原文：<https://hackaday.com/2021/04/11/solar-stevenson-screen-for-smart-sprinkler/>

我们经常看到湿度传感器和水泵的结合来实现工厂维护的自动化。不过，每一个都有自己独特的想法，解决问题的方式对其他应用程序也是有用的。[Emiliano Valencia]带着一些值得收集的著名技术着手这个项目，并对他的“[自主太阳能灌溉监测站](https://www.instructables.com/Autonomous-Solar-powered-Irrigation-Monitoring-Sta/)”做了一个很好的描述。

特别令人感兴趣的是[Emiliano]3D 打印螺纹杆的解决方案；把它放平，刮掉顶部和底部。无论如何，你并不需要整个线程，不是吗？尽管 ESP8266 上的 GPIO 引脚数量相对有限，但该站有三个模拟传感器，通过 ADS1115 ADC 连接到 I2C，一个 BME280 用于温度、压力和湿度(也在 I2C 总线上)，两个 MOSFETs 用于控制阀。至于电力，外壳顶部的太阳能电池为 18650 电池充电。无线通信进入 Thingspeak，一个漂亮的仪表板显示你想要的一切。 [Stevenson 屏幕](https://en.wikipedia.org/wiki/Stevenson_screen)的整个想法也很聪明，虽然这个是 3D 打印的，但似乎任何类型的堆叠容器都可以被修改以达到相同的目的，并通过堆叠更多的单元来实现任何大小。不过，我们对虫子进入电子设备持怀疑态度。

我们最近看到一个基于 [ESP32 的电容式湿度传感器](https://hackaday.com/2021/03/07/give-your-smart-home-a-green-thumb-with-mqtt/)在单个 PCB 上通过 MQTT 发送，我们还看到【Emiliano】生产其他高质量内容[用乙烯切割器](https://hackaday.com/2020/04/01/making-pcbs-with-a-vinyl-cutter/)蚀刻 PCB。

 [https://www.youtube.com/embed/oxOlJC9eMm4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/oxOlJC9eMm4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

