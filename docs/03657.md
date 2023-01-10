# 气象站能像飓风一样震撼你

> 原文：<https://hackaday.com/2019/07/22/weather-station-can-rock-you-like-a-hurricane/>

人们喜欢谈论天气。这是一次完美的闲聊，无论你是想开始一段对话还是通过避免尴尬的沉默来保持对话。同样，气象站也是任何传感器相关项目创意的理想起点。你开始熟悉通信总线、ADC、通用数据采集，并了解如何将它们可视化。

如果你的气象站没有可视化任何东西呢？【OttoNL】正在用一个产生 MIDI 的气象站来回答这个问题，这个气象站利用音乐的情绪来传达外面的元素状况。

使用通过 Arduino IDE 编程的 ESP8266，[OttoNL]连接了光敏电阻、雨水传感器和用于温度、气压和湿度的全能工作狂 BME280。通过读取传感器，ESP 将生成 MIDI 音符，这些音符被发送到连接的合成器，每个传感器影响生成的 MIDI 信号的不同方面。下雨时会放一首悲伤的慢歌，而晴天时会放一首欢快的快歌。虽然目前它还没有使用 ESP 的 WiFi 功能，但未来的版本可以很容易地从互联网上检索一些天气预报数据，并将其添加到组合中。

将这个连接到你的闹钟上，你就能以合适的心情开始你的一天。你甚至可以[定制你的早餐吐司](https://hackaday.com/2018/12/12/toast-printer-prints-tasty-images-and-weather-forecasts/),让你的早晨生活沉浸在抽象的天气暗示中。

 [https://www.youtube.com/embed/W3yqpwlSAmI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/W3yqpwlSAmI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

