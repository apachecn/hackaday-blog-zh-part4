# 垃圾桶自己拿出来

> 原文：<https://hackaday.com/2020/09/10/garbage-can-takes-itself-out/>

家庭自动化是一个美好的目标，但通常局限于灯、百叶窗和其他相对静止和/或电气性质的东西。毫无疑问，这是一个挑战，但要真正提升你的家庭自动化游戏，你需要跳出框框思考。[例如，这个可以自己拿出来的自动化垃圾桶](https://www.raspberrypi.org/blog/self-driving-trash-can-controlled-by-raspberry-pi/)，拥有你所需要的所有家庭自动化街头信誉。

垃圾桶通过内部有轮毂电机的踏板车轮子移动，由锂电池供电，但这个项目的真正天才是控制一切的电子设备。一个 Raspberry Pi Zero W 位于该建筑的中心，它通过驱动板控制电机，并从 Nvidia Jetson 板接收何时将垃圾桶推到路边的指令。那块板是需要的，因为创作者[Ahad Cove]不想麻烦地告诉他的垃圾桶把它自己拿出来或者甚至安排它。相反，他使用机器学习来检测垃圾车何时驶向街道，并指示垃圾桶自动推出。

将这个建筑结合在一起的另一件事是让车库的门自动为垃圾桶打开。幸运的是，[Ahad]的车库开门器已经配备了 WiFi，并有一个可用的应用程序，而他并不知道，这使得这成为构建中令人惊讶的简单部分。如果你有一个更基本的车库门开启器，那么在互联网上有很多选择。

 [https://www.youtube.com/embed/7fdM2hHW8yA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/7fdM2hHW8yA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

