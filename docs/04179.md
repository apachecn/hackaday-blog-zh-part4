# Arduino、加速度计和 TensorFlow 让你成为现实世界的街头战士

> 原文：<https://hackaday.com/2019/09/18/arduino-accelerometer-and-tensorflow-make-you-a-real-world-street-fighter/>

一个问题:如果你在用手势控制经典视频游戏《街头霸王》，你不就是在玩街头格斗吗？

如果她的人工智能手势识别控制器实验成功，这将是[查理杰拉德]必须解决的问题。[Charlie]将游戏控制器组装在一起，以有趣和有趣的方式了解更多关于机器学习的黑暗艺术。

控制器由一个带 WiFi 的电池供电 Arduino MKR1000 和一个 MPU6050 加速度计组成。控制器握在手中，将加速度计数据传输到外部 PC，捕捉运动特征。[查理]训练了三种不同的动作——一拳、一记上钩拳和可怕的哈都肯——并捕捉了每种动作的数百个例子。原始数据经过处理，转换成张量，并用于训练三个动作的模型。最初的测试似乎效果不错。[查理]还制作了一个在线版本，可以从你的智能手机上捕捉动作。演示在下面的视频中解释；不幸的是，在撞毁它之前，我们只能让三个以上的人进去。

随着大多数机器学习项目似乎专注于区分猫和狗，这是一个令人耳目一新的变化。这些天，我们看到了许多与众不同的机器学习项目，从[加密货币钱包攻击](https://hackaday.com/2019/09/13/side-channel-attack-shows-vulnerabilities-of-cryptocurrency-wallets/)到[一个半令人毛骨悚然的健身监控摄像头](https://hackaday.com/2019/09/15/gymcam-knows-exactly-what-youve-been-doing-in-the-gym/)。

 [https://www.youtube.com/embed/oTZXZyW_yno?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/oTZXZyW_yno?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[baldpower]的提示！