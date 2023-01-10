# WiFi 遥控那些廉价的 LED 灯带用一个 ESP8266 直通

> 原文：<https://hackaday.com/2019/01/09/wifi-remote-control-those-cheap-led-strips/>

廉价 LED 照明产品的激增为足智多谋的黑客提供了永无止境的机会。几美元就可以获得一串彩色的照明，但如果不花更多的钱，它们就缺乏电子控制的额外效用。这是[艾伯特·大卫用他简单的[基于 ESP8266 的 WiFi 切换器](http://albert-david.blogspot.com/2019/01/wifi-based-diy-5v-switcher-for-led.html)解决的问题，他将它添加到一串 USB 供电的 led 上，并巧妙地将它使用的 ESP-12 模块安装在 USB 插头上。

电路非常简单，只使用了几条 I/O 线。晶体管负责重物的提升，软件由 Sonoff(和类似)设备的 Tasmota 固件提供。我们怀疑这种连接的经济性，即使使用较小的 ESP-01 模块提供的有限资源，也可以实现相同的任务。

不久以前，执行诸如通过无线网络控制灯之类的任务需要大量的成本、电力和复杂性。自从我们报道了 ESP8266 的问世以来，近五年来[我们已经发展到了这样一个地步，即这项任务是一个使用商品组件的简单项目，这代表着某种奇迹。](https://hackaday.com/2014/08/26/new-chip-alert-the-esp8266-wifi-module-its-5/)