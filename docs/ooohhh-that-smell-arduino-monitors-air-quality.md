# 哦，那个味道:Arduino 监测空气质量

> 原文：<https://hackaday.com/2021/04/23/ooohhh-that-smell-arduino-monitors-air-quality/>

根据[汤姆·莱勒博士]的歌曲*污染*，“戴上防毒面具和面纱。然后就可以呼吸了，只要不吸气！”虽然世界上大多数地方的空气质量没有那么糟糕，但人们非常担心长期暴露在空气中的颗粒物会导致健康问题。[Ashish Choudhary]与[一台 Arduino 结合，它带有显示器和污染传感器](https://circuitdigest.com/microcontroller-projects/air-quality-analyzer-using-arduino-and-nova-air-quality-sensor-sds011)来给出空气中 PM2.5 和 PM10 水平的读数。

该传感器使用激光二极管和光电二极管来检测和计数颗粒，同时风扇使空气通过系统。如果你不了解污染指标，PM2.5 是指非常细微的颗粒(小于 2.5 微米)，PM10 是指 10 微米的颗粒。你可以在网上找到该设备的数据表。

需要注意的一点是，传感器的寿命是有限的。数据表声称“高达”8000 小时。如果你连续运行传感器，不到一年，所以你可能想明智地决定你点亮设备的频率。

这不是我们第一次看到这种特定的传感器。如果你想找到污染物的确切来源，可以考虑[这座建筑](https://hackaday.com/2020/04/02/particle-sniffer-for-pollution-point-sources/)。

 [https://www.youtube.com/embed/vZLSZCUMZEs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/vZLSZCUMZEs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

