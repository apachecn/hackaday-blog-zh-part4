# 适用于所有人的动作捕捉系统

> 原文：<https://hackaday.com/2018/09/24/a-motion-capture-system-for-everyone/>

[脊索动物]正在为每个人制作一个动作捕捉系统，到目前为止，结果令人印象深刻，足以进入 T2 黑客日人机界面挑战赛的决赛。几年前，它开始于一个人想要捕捉舞台上一个舞者的数字表演，现在已经发展成为一个贡献者社区。电路板文件和软件已经作为 alpha 版本发布，同时还有一些使用说明，不过更详细的文档还在编写中。

![Chordata motion capture dancer and Blender](img/9013663703b8a7aa3ede154a07eee6a1.png)15 个传感器板被称为 K-Ceptors，附着在身体上的各个点上，每个传感器板都包含一个 LSM9DS1 IMU(惯性测量单元)。K-感受器被连接在一起，同时仍然允许大量的自由活动。通信是通过 I2C 到一个树莓派。然后，Pi 通过 WiFi 将收集到的数据发送到台式机。当你四处走动时，一个人形的 3D 模型会实时跟随，使用 Blender(一种流行的免费 3D 建模软件)显示在桌面的屏幕上。当然，如果你愿意，你可以用这些数据做些别的事情，比如让机器人动起来？在下面的视频中，我们可以看到一位经验丰富的舞者在测试这个系统时的概述和表演。

顺便提一下，[他们 Hackaday.io 页面上的最新日志条目](https://hackaday.io/project/27519-motion-capture-system-that-you-can-build-yourself/log/152452-the-testbed)指出，无论何时对 K-Ceptor 板进行更改，都需要进行 15 次更改才能试用。为了帮助解决这一问题，他们展示了他们为电路板故障诊断所做的测试平台，只要它们一出炉。

 [https://www.youtube.com/embed/npJumH0eol0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/npJumH0eol0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



The [HackadayPrize2018](https://hackaday.io/prize) is Sponsored by: [![Microchip](img/20eb9d92b47da4c15177567c02a65727.png)](https://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey)  [![Supplyframe](img/2d012d9fc9c7873688699aeadb4742d2.png)](https://supplyframe.com/)