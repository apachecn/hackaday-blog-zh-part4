# 那到底是不是一只猫？

> 原文：<https://hackaday.com/2021/03/06/is-that-a-cat-or-not/>

疫情引起的厌倦以许多不同的方式带给人们。我们中的一些人去长途散步，另一些人学习说一种新的语言，而更多的人释放他们内心的游戏流光。[Niklas Fauth]已经从他的其他项目中脱离出来，创造了一个非常特别的项目。一个猫探测器！你将不再考虑你面前的物体或生物是不是一只猫，现在这个存在问题可以用一个小工具来回答。

与其说这是一个特殊的新技术，不如说这是一个新奇的项目，他从一个廉价的红外温度计上取下了一个看起来像外壳的东西，并在里面放了一个带摄像头和小屏幕的树莓派 Zero。这进而用 [COCO-SSD](https://github.com/tensorflow/tfjs-models/tree/master/coco-ssd) 对象识别模型运行 Tensorflow。该设备有一个触发器，当它被按下拍摄图像时，它会应用模型来检测对象是否是猫。发布到 Twitter 上的视频低于休息时间，我们不能否认它在猫科动物观察部门的有用性。

[尼克拉斯]过去不止一次出现在这里。这也不是他唯一的疫情项目。

> 里面是一个 Pi 零运行 tensorflow，采用 COCO-SSD 型号。[pic.twitter.com/otlFaZyjir](https://t.co/otlFaZyjir)
> 
> —Niklas Fauth(@ FauthNiklas)[2021 年 3 月 3 日](https://twitter.com/FauthNiklas/status/1367147722776707072?ref_src=twsrc%5Etfw)