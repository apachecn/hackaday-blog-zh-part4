# 蚀刻自拍

> 原文：<https://hackaday.com/2019/07/30/etch-a-selfie/>

在现代智能手机时代之前，自拍是一种真正的努力。翻盖手机没有前置摄像头，如果你想真正回到胶片相机的时代，你需要在相机上设置一个定时器，或者安装一个物理遥控快门。你也可以试着在素描上画一幅自画像，但是这需要很多时间和艺术技巧。幸运的是，在现代世界中，我们可以将一些旧技术带入未来，添加一个机器人来创作有趣的复古自拍——而不需要成为艺术家。

[im-pro]的设备将两个伺服系统连接到蚀刻草图旋钮。这个[本身并不是一个新的想法](https://hackaday.com/2018/09/28/bot-makes-etch-a-sketch-art-in-one-continuous-line/)，但该设备还包括一个前置摄像头，利用了特别便宜的 ESP32 摄像头模块。结合相机功能与[【巴特德林】的 ESP32 Grbl 端口](https://github.com/bdring/Grbl_Esp32)是一个赢家。[查看【im-pro】的 GitHub 中的代码](https://github.com/pknoe3lh/Etch-a-Selfie)。

一旦拍摄了照片，位于建筑中心的 ESP32 就会进行图像处理，然后在蚀刻草图上绘制图像。机器人需要一个黑白图像来绘制，以及一个无需“举起”绘图工具来完成它的算法，这些任务扩展了这样一个小型处理器的能力。这需要一些时间来发挥作用，但最终结果会说明一切。

最终的项目绝对值得期待，如果不是为了有趣的 ESP32 控制的机器人，而是为了图像处理算法的实现。不过，ESP32 是一个真正的[多功能平台](https://hackaday.com/2017/06/16/esp32-mini-robot-packs-sensors-and-4wd/)，对于[建造几乎任何东西](https://hackaday.com/2019/07/08/esp32-gets-advance-windowed-apps-using-this-vga-gui-library/)都很有用。

 [https://www.youtube.com/embed/ciXKd-_mjiM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ciXKd-_mjiM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

