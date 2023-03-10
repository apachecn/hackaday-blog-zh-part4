# 灯有助于改善空气质量

> 原文：<https://hackaday.com/2021/06/03/lamp-sheds-light-on-air-quality/>

很难理解空气质量是好是坏，除非情况糟糕到你真的可以看到空气中悬浮的烟雾。[guillaume_slizewicz]没有试图消化一堆空气质量数据，而是建造了 Canari — [一盏可爱的灯，通过获取当地空气质量数据并将其转化为光模式](https://www.instructables.com/Canari-a-Lamp-That-Transform-Air-Quality-Measureme/)来揭示空气污染问题。

Canari 当然是以勇敢的鸟命名的，这些鸟曾经在矿工被迫改用一氧化碳传感器之前警告他们危险的空气条件。这只鸟有一个 Raspberry Pi Zero W，它从公共 API 获取空气质量数据，并根据空气中的颗粒浓度用 PWM 发动机罩控制灯光。微粒越多，发光二极管就越暗，它们越快消失。

Canari 抓取的主要数据是颗粒物的数量，显示器可以在表示空气中 PM2.5(直径小于 2.5 微米的颗粒物)和 PM10 的水平之间切换。休息之后，请观看演示和设置视频。

更喜欢数字？你真正需要的只是一个微控制器、一个空气质量传感器和一个显示器。

[https://player.vimeo.com/video/548770805](https://player.vimeo.com/video/548770805)