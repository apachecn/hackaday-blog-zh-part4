# 通量:一个 40 英尺长的动态艺术作品

> 原文：<https://hackaday.com/2022/10/07/flux-a-forty-foot-long-kinetic-art-piece/>

当你思考你最近的问题时，如果没有一些引人注目的艺术品供你凝视，那么没有一个办公空间是完整的。但如今，基于 LED 的显示器已经普遍到令人厌烦的程度。运动艺术作品很受欢迎，[这件名为 *Flux* 的作品是](https://hackaday.io/project/187446-flux-kinetic-art-installation)的一个完美例子。

C 由【尼古拉斯·斯特德曼】为一个非常受欢迎的电子商务平台的多伦多办事处定制， *Flux* 由天花板上二十块相同的木板组成，排成一条四十英尺长的线。每块木板都有一对旋转棱镜，由一堆泡沫板构成，表面涂有金属漆。棱镜由单独的步进电机旋转，每个步进电机由基于 TMC2160 的模块驱动，使它们安静无声。

一个简单的 3D 打印支架将一个装有 [AMS AS5600 旋转磁编码器](https://ams.com/en/as5600) 的小 PCB 固定在步进电机的后部。这允许对共享的 Arduino 进行闭环反馈，这对这样的雕塑非常重要。每个 Arduino 都连接到一个 Raspberry Pi，运行一个用 node.js 编写的简单应用程序，负责协调运动，并根据需要上传更新的固件映像。我们认为这是一个简单但非常有效的构建！

更有趣的是对某些数据源作出反应的动态艺术装置，如 [*Adad* ，它将雷击数据](https://hackaday.com/2022/01/27/kinetic-art-installation-brings-all-the-worlds-lightning-to-one-place/) 可视化。如果这些构建过于庞大和复杂，我们已经看到了许多较小的桌面玩具的例子，比如这个 [3D 打印翻滚链演示](https://hackaday.com/2022/09/25/3d-printable-sculpture-shows-off-unpredictable-order-of-chains/) 举例来说。

 [https://www.youtube.com/embed/Z2o9WQWpmp4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=16&wmode=transparent](https://www.youtube.com/embed/Z2o9WQWpmp4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=16&wmode=transparent)

