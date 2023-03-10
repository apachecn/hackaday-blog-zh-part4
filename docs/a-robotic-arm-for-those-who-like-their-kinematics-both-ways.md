# 对于那些喜欢双向运动的人来说，这是一个机器人手臂

> 原文：<https://hackaday.com/2018/10/19/a-robotic-arm-for-those-who-like-their-kinematics-both-ways/>

如果你想着手机电项目，机械臂是一个很好的主意。有设计上的联系，有驱动上的马达，但也有控制上的问题。这被称为“运动学”，可以从正反两方面来考虑。 [[aerdronix]建造了一个可以双向工作的机器人手臂。](https://www.instructables.com/id/Arduino-IoT-Robotic-Arm/)

构建的大脑是 Arduino Yun，它通过 USB 接口接收命令。控制是通过 Blynk 应用程序实现的，它允许物联网项目轻松地为智能手机构建应用程序，这些应用程序可以发布到常见的平台上。

手臂的位置以两种方式控制。当配置为使用反向运动学时，用户命令末端效应器位置，手臂计算出连杆的必要位置以实现它。然而，该臂也可以用于正向运动学模式，在这种模式下，各个关节位置被命令，然后决定末端执行器的最终位置。

总的来说，这是一个记录良好的构建，它展示了从基本的机械设计到控制系统所需的软件和源代码的一切。对于新手来说，这是一个很好的学习资源，这样的手臂可以很容易地用在更复杂的项目中。

我们看到许多机器人手臂围绕着这些部件，[就像这个基于宜家灯具的奇妙建筑](https://hackaday.com/2017/01/04/from-ikea-lamp-to-robot-arm/)。如果你有一个，[一定要打电话给小费热线](https://hackaday.com/submit-a-tip/)。休息后的视频。

 [https://www.youtube.com/embed/B4DPD9VfmHA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/B4DPD9VfmHA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

