# DIY 个人助理机器人听到和看到所有

> 原文：<https://hackaday.com/2019/08/11/diy-personal-assistant-robot-hears-and-sees-all/>

谁不想要一个能给他们拿杯水的机器人呢？[Saral Tayal]不仅仅是这么想的，他直接投入进来，建造了他自己的个人助理机器人。然而这不仅仅是一辆遥控漫游车。机器人实际上会听他的声音并识别他的脸。

机器人的身体是常见的“漫游者 5”平台，其中[Saral]添加了许多 3D 打印部件。像雪橇这样的铲车赋予了机器人拿起东西的能力。一些部件更多的是关于形式而不是功能——[ Saral]喜欢美国宇航局的精神号和机遇号火星探测器，所以他增加了一些模拟太阳能电池和其他东西。

前面的罗技网络摄像头功能非常强大——图像被输入到机器学习模型，而音频则被处理以监听命令。这个机器人可以找到并捡起 90 个独特的物体。

机器人的大脑是一个树莓派。它使用 TensorFlow 进行物体识别。[Saral]使用的一些模型非常大——大到 Pi 在 100%的 CPU 利用率下每秒只能处理几帧。Google Coral 协处理器大大加快了速度，而只使用了大约 30%的 Pi 处理器。

它需要几个电机来控制机器人的轨道和雪橇。这是由两个 Roboclaw 电机控制器处理的，它们本身由 Pi 控制。

这些年来，我们已经看到了相当多的移动机器人漫游车，但是萨拉尔的机器人是最实用的设计之一。更好的是，它是完全开源的。你可以在[的 GitHub](https://github.com/SaralTayal123/Object-Finding-Rover) repo 上找到代码和 3D 模型。

休息之后，请观看个人助理 rover 的视频。

 [https://www.youtube.com/embed/aso3N4YiCAQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/aso3N4YiCAQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

