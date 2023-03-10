# ESP32 时钟也需要时间来提供天气信息

> 原文：<https://hackaday.com/2021/10/27/esp32-clock-takes-time-to-give-weather-info-too/>

现在是北半球的秋天，所以[迈克·兰金]的孩子们回到了学校，每天早上都回来向他咨询天气和应该穿什么。因为他不是气象学家， [[Mike]造了一个漂亮的昏暗小巧的时钟](https://github.com/mike-rankin/ESP32_Desktop_Clock)，为他做了所有的工作，还有更多。它发出可爱的深橙色，非常适合床头柜和那些清晨的审问。

在默认模式下，这个时钟会以醒目的橙色显示时间、二氧化碳水平、室温和湿度。但是在飞行时间传感器前挥动你的手，它就会显示当天的低温和高温，以及天气预报。几秒钟后，它会回到默认模式。ESP 从 NTP 服务器获取时间，然后从 OpenWeather API 获取天气。室内天气来自板上的组合传感器。

这个小小的包裹里是一个漂亮的旋转板，它的大脑是一个 ESP32 微微 D4。除了气候传感器，还有一个二氧化碳/TVOC 传感器(总挥发性有机化合物)来嗅出危险。背面还有一对按钮和一个环境光传感器，但[迈克]还没有使用这些。为未来的爸爸们加上 Qwiic 连接器，你就有了这个小玩意。虽然这些图片使它看起来有点大，但休息后你可以在演示视频中看到它到底有多小。

[迈克]似乎喜欢微小的东西，我们非常钦佩这一点。[检查他的积极小人 ESP32 开发板](https://hackaday.com/2019/02/22/a-coin-cell-powers-this-tiny-esp32-dev-board/)。

 [https://www.youtube.com/embed/Y3FI6KhXrEo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Y3FI6KhXrEo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

