# 本周失败:如何不做 3D 扫描仪

> 原文：<https://hackaday.com/2018/07/23/fail-of-the-week-how-not-to-make-a-3d-scanner/>

有时候，你对一个项目能说的最好的话就是，“不错的开始。”这就是迄今为止糟糕的 DIY 3D 扫描仪的情况，它既可以作为进一步开发的起点，也可以作为不要做什么的教训。

不要误解我们，我们对[比特鲁尼]非常尊重，因为他会发布他的失败和成功，比如来自 ESP32 的[合成视频](https://hackaday.com/2018/02/22/software-defined-television-on-an-esp32/)和 [AM 无线电信号](https://hackaday.com/2018/01/28/esp32-makes-for-worlds-worst-radio-station/)。他在这个项目中使用了一个 ESP8266，它实际上使用了两种不同的传感器:一个超声波换能器和一个小型飞行时间激光芯片。每个都被安装到一个由业余爱好伺服系统和 3D 打印部件构建的双轴扫描仪上。俯仰和偏航轴通过半球移动传感器收集数据，但不幸的是，Wemos D1 Mini 缺乏 RAM 来渲染原始点的完整点云。这被外包给一个 WebGL 页面。超声波传感器的初步结果不太好，TOF 传感器也留下了所有需要的东西。但是[比特鲁尼]坚持了下来，并得到了一些结果，至少看起来他正朝着正确的方向前进。

我们希望他能解决这个问题，并带来更好的结果，但同时，我们也为他愿意把这个贴出来而鼓掌，这样我们都能从他的痛苦中受益。他可能想从这台精致昂贵的激光雷达扫描仪的结果中寻找灵感。

 [https://www.youtube.com/embed/vwUGPjQ_5t4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/vwUGPjQ_5t4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

