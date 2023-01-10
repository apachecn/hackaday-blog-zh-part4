# 让你了解世界各地最新动态的地震展览

> 原文：<https://hackaday.com/2021/09/03/an-earthquake-display-to-keep-you-abreast-of-rumblings-worldwide/>

互联网给我们带来了在全球范围内共享数据的能力，而且几乎是瞬间共享。它彻底改变了全世界的科学共享，利用这个全球数据网络的优势，这是来自[AndyGadget]的地震展示。

该建筑依赖于配备了 ILI9486 TFT 显示器的 ESP32。屏幕是彩色的，分辨率为 480×320。这使得它能够使用 [Web 墨卡托投影](https://en.wikipedia.org/wiki/Web_Mercator_projection)来显示一幅相当清晰的世界地图，以适应矩形屏幕。微控制器然后从[地震门户](https://www.seismicportal.eu/)获取信息，该网站汇集了来自地震仪和分布在世界各地的其他传感器的数据。来自该网站的数据被实时传输到设备上，并覆盖在世界地图上，让观众一眼就能看到当前地震的位置。

这是一个伟大的项目，我们认为这将是对任何大学地质系的巨大贡献。如果这激发了你的兴趣，考虑自己深入地震分析和数据的世界吧！