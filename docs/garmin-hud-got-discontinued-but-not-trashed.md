# Garmin HUD 停产了，但还没报废

> 原文：<https://hackaday.com/2022/10/30/garmin-hud-got-discontinued-but-not-trashed/>

Garmin HUD+是一款用于汽车仪表板的小型蓝牙设备，旨在用作 Garmin 智能手机应用程序数据的 GPS 平视显示器。它使用一个明亮的 VFD(真空荧光显示器),通过一个清晰的反射器观察，并显示 GPS 信息和方向。它于 2015 年停产，但[Doz]喜欢他的，并愉快地使用它，直到手机升级意味着它不再工作。它是注定要被填埋的吗？如果他有什么要说的就不会了！

[Doz]尝试的第一件事是使用另一个 Android 应用程序，但由于它也不起作用，是时候坐下来反思这个问题的范围了。在[Doz]的例子中，他真的只想显示一些基本的有意义的数据，并决定如果他有合适的硬件，他可以完全放弃手机。

[![](img/c6cbe5362ce94cb0b693471e369a4447.png)](https://hackaday.com/wp-content/uploads/2022/10/IMG_20220304_114459-e1667028373649.jpg)

A GPS receiver and ESP32 board take the place of a mobile phone app that no longer works. The HUD display itself is unchanged.

u-blox GPS 模块和 ESP32 板是通过蓝牙在 Garmin HUD+上显示有意义数据的独立设备的关键，这要归功于所使用的协议经过了[逆向工程](https://github.com/gabonator/Work-in-progress/tree/master/GarminHud)。经过大量的故障排除后，[Doz]获得了一些基本功能:速度，时间，卫星计数，和一个工作的指南针箭头。GPS 接收器和 ESP32 位于一个小型 3D 打印外壳中，HUD 呢？在 2015 年，它一如既往地留在仪表板上，幸福地意识到智能手机技术的进步已经将它抛在身后。

[他的代码在 GitHub](https://github.com/andydoswell/ESP32-Garmin-Hud) 上，下面有一个视频演示这个单元，就在分页符下面。总是很高兴看到 [VFD 显示器被赋予新的生命](https://hackaday.com/2021/09/23/upcycling-a-vfd/)。

 [https://www.youtube.com/embed/vptdm6o0_lE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/vptdm6o0_lE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

