# 自动浇水机有植物渴望的东西:肥料

> 原文：<https://hackaday.com/2021/05/14/automated-watering-machine-has-what-plants-crave-fertilizer/>

多年来，我们已经看到了无数的自动化植物护理系统，但出于某种原因，它们几乎从未涉及到园艺的秘方——肥料。但是[xythobuz]知道发生了什么。当他们自己搬进新公寓时，是时候展开并开始在阳台上种植一些植物了。不久，花园就大到足以保证有一个自动浇水和施肥系统。

这个聪明的 DIY 系统是基于一个 5L 的重力供水水箱，带有螺线管控制和三个[壶]液体肥料，通过蠕动泵添加到水中。别担心，水箱有浮动开关，每次都有[xythobuz]手动关闭，这样就不会淹没公寓。

在 UI 方面，Arduino Nano 克隆正在运行，提供 LCD 输出并处理键盘输入。机器本身由一个 ESP32 和一对四通道继电器板控制，继电器板控制入口阀、四个出口阀和三个喷出肥料的蠕动泵。ESP 还提供了一个模拟控制面板的 web 界面，并添加了调试日志。这两块板使用 I C over DB-9 进行通信，因为这可能就是[xythobuz]所拥有的。休息后看看演示视频，然后去看看你自己的植物。他们想念你！

不想买任何旧的蠕动泵？或许你可以打印自己的照片。

 [https://www.youtube.com/embed/q-sjvPYs-EQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/q-sjvPYs-EQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

