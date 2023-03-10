# Arduino 机器人摇动 PS2 控制器

> 原文：<https://hackaday.com/2019/09/17/arduino-bot-rocks-a-ps2-controller/>

就控制机器人而言，今天的制造商有太多的选择。支持 WiFi 和蓝牙的微控制器随处可见，与智能手机应用程序的集成也不在话下。尽管如此，旧的方法仍然占主导地位，就像伊戈尔·丰塞卡用一个简单的 Arduino 机器人展示的那样。

这是一个经典的建筑，使用履带式底盘，一对马达提供推进和滑动转向。电机由 L298N H 桥板控制，电源由三节 18650 电池提供。Arduino Uno 是这次行动的大脑。控制是通过 Playstation 2 控制器，在这种情况下是 2.4 GHz 的第三方版本。这使得机器人可以被无线控制，解码由[【比尔·波特】有用的 Arduino 库处理。](http://www.billporter.info/2010/06/05/playstation-2-controller-arduino-library-v1-0/)

这是一种构建远程控制机器人的廉价方法，也是一种教感兴趣的孩子如何使用嵌入式系统的好方法。我们以前也推出过类似的版本。休息后的视频。

 [https://www.youtube.com/embed/1oH0zqkGxNc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/1oH0zqkGxNc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

