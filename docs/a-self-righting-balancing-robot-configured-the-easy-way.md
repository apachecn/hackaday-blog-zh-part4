# 自动扶正平衡机器人配置简单

> 原文：<https://hackaday.com/2021/12/13/a-self-righting-balancing-robot-configured-the-easy-way/>

YouTube 上的挪威电子黑客[Hans Jr gen]又名[time expander]，对机器人技术有着明显的兴趣，他最近的努力是，决定是时候建立一个定制的控制器平台了。由于[Hans]有一堆 Dynamixel 伺服电机可供测试，该平台的第一个好项目是一个简单的自平衡轮式机器人。(视频，嵌入下方)

我们说“简单”,但事实并非如此，因为要实现这一点需要做很多工作。第一个问题，就是传感，用优秀的 [BMO055 IMU 芯片](https://www.bosch-sensortec.com/products/smart-sensors/bno055/)很快就解决了。接下来，它倒了怎么办？简单地添加一些伺服控制臂，允许机器人翻转自己直立。控制覆盖了 ESP32-WROOM-32D 模块，由我们在 Espressif 的朋友提供，支持远程固件空中上传(OTA 更新)以及参数调整。为了实现后者，[汉斯]选择使用 [bonjour/mDNS](https://en.wikipedia.org/wiki/Bonjour_(software)) ，这是一种零配置网络的实现。这使 ESP32 连接到 WiFi 上，但如果不仔细研究，还不清楚如何连接。为了简化连接，[汉斯]通过联网的有机发光二极管实现了动态二维码。这只是你在我们的互联网角落里看到的那些微小的 0.96 英寸显示器中的一个。

只需用手边的任何兼容设备扫描二维码，就可以打开一个简单的配置网页，允许用户调整 PID 控制器参数，并检查平衡机器人。很棒的东西！

PCB 是在 Eagle 中设计的，ESP32 的固件可用，塑料的 3D 模型是用 fusion 360 设计的，[Hans]甚至目前正在进行一些初步的 Alexa 集成。多么有趣的项目！

以上都是，尽管是早期的剪辑(注意 bug！)可在[项目 GitHub](https://github.com/hansj66/automaton-xl320) 上获得，供您观赏。

我们对自平衡 3D 打印机器人并不陌生，既然你在这里，为什么不检查一下有问题的自平衡刺猬索尼克呢？如果你对轮式机器人不感兴趣，有一款一点也不奇怪的[单腿弹跳机器人](https://hackaday.com/2020/08/02/little-jumping-bot-can-now-stick-the-perfect-landing/)可能会让你感兴趣。

 [https://www.youtube.com/embed/FlivZoxygZM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/FlivZoxygZM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



谢谢你的提示，[哈尔吉尔]！