# 小丑监视器保持对危险气体水平的关注

> 原文：<https://hackaday.com/2021/07/23/joker-monitor-keeps-an-eye-on-hazardous-gas-levels/>

小丑是蝙蝠侠系列中的一个受欢迎的角色，有时会使用有毒气体作为他犯罪技能的一部分。这启发了[的【kutluhan_aktar】这个有趣的项目，旨在监测空气中有害气体的水平。](https://hackaday.io/project/180859-joker-remote-hazardous-gas-station-and-monitor)

该项目不仅仅使用一个气体传感器，而是几个！它包括 MQ-2、MQ-3、MQ-4、MQ-6 和 MQ-9。这使得它对多种可燃气体敏感，也能检测一氧化碳。Arduino Nano 读取传感器，并在 RGB LED 和附加的 IPS 屏幕上显示结果。

每个传感器的读数可以通过使用红外遥控器来选择。然而，为了更好地作为安全设备工作，让 Arduino 自动循环通过每个传感器可能更有用，定期检查它们，并在读数高的情况下发出警报。

整个项目是建立在一个定制的 PCB 上，它巧妙地构建了一个小丑自己的图像。这有助于使这个项目更像是一个展示品，也体现了创作者的美学技巧。

这是一个有趣的构建，并且通过一些软件调整就可以非常强大。也就是说，如果你在一个有可燃气体危险的空间工作，投资一些适当的安全设备可能比依赖 Arduino 项目更有价值。

顺便说一句，如果你想改善使用这种气体传感器的结果，[我们已经在过去研究过了](https://hackaday.com/2017/07/13/improving-the-accuracy-of-gas-sensors/)。休息后的视频。

 [https://www.youtube.com/embed/BJi-VIKMpJE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/BJi-VIKMpJE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

