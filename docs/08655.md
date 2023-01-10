# 坐直了！:开源蓝牙姿势感知

> 原文：<https://hackaday.com/2020/12/16/sit-up-straight-open-source-bluetooth-posture-sensing/>

随着越来越多的人把工作时间花在电脑后面，不良姿势以及随之而来的背痛和背部问题变得越来越普遍。为了在自己的日常生活中解决这个问题，[ ImageryEel]制作了 [PosturePack](https://hackaday.io/project/175099-posturepack) ，这是一款可穿戴的蓝牙姿势传感器。 ![](img/cd818da14859aeee7471ab6fd24d9c22.png)

PosturePack 的设计是为了放入一个缝在内衣口袋里的小口袋，在肩胛骨之间。它由一个带有 ATmega32U4 的定制 PCB、BNO055 IMU、蓝牙模块、小型 LiPo 和电源电路组成。根据来自 IMU 的方位数据，每当用户向前弯腰时，就会通过蓝牙向智能手机发送通知。

他说，尽管手机通知起了作用，但将触觉反馈集成到手机中会是一个更好的选择。这也可以用来提醒用户时不时地站起来休息一下，并为智能手表提供一种活动监控的替代方案，而不必将每个动作发送到其他人的服务器上。软件永远是这类项目中最难的部分，尤其是当设备变得“更智能”的时候。学习识别活动和姿势实际上是[微型机器学习模型](https://hackaday.com/2020/12/04/remoticon-video-how-to-use-machine-learning-with-microcontrollers/)的一个好地方。

相比之下，我们之前讨论过的姿态传感器必须在特定的工作站上安装和设置，比如安装在椅子上的基于[超声波的版本](https://hackaday.com/2016/03/11/posture-sensor-reminds-you-to-sit-up-straight/)，以及基于[网络摄像头的版本](https://hackaday.com/2014/05/06/a-webcam-based-posture-sensor/)。