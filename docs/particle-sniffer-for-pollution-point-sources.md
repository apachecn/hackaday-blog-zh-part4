# 污染点源的粒子嗅探器

> 原文：<https://hackaday.com/2020/04/02/particle-sniffer-for-pollution-point-sources/>

测量空气质量时，颗粒物是一个重要的观察指标。PM2.5 等级是指直径小于 2.5 微米的颗粒物。虽然当局经常在全市范围内测量，但[[rabbit creek]希望找到一种方法来追踪室内的点源。](https://www.instructables.com/id/Particle-Sniffer/)

这个工具[rabbitcreek]与一个典型的红外车间温度计有着相似的外形。在里面，它装有一个霍尼韦尔 HPMA115S0-TIR 激光粒子传感器，连接到运行该节目的 ESP32。所选的传感器使事情变得简单，该设备已经设置了一个鼓风机和入口和出口，以获取准确的读数..结果显示在 SSD1306 有机发光二极管屏幕上。它被包裹在一个 3D 打印的盒子里，有一个扳机把手，前面有一个狗鼻子，暗示了设备的真实用途。

在测试中，该设备被证明能够检测大气颗粒物的点源，如鲜花和烤面包机。我们确信这对于那些在暖通空调和环境评估行业工作的人来说会很方便。我们以前也见过其他监测微粒的装置。休息后的视频。

 [https://www.youtube.com/embed/fB5FgvBTKpk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/fB5FgvBTKpk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

