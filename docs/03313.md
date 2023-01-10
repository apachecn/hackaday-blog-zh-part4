# 在你的下一个模型火箭上驾驶私人飞机

> 原文：<https://hackaday.com/2019/07/05/fly-a-pi-on-your-next-model-rocket/>

我们不时会看到模型火箭仪器的电子项目。那些多年来一直从事这项爱好的人可能还记得像 PIC16F84 这样的 8 位微控制器是你可能会在任务中飞行的那种硬件。然而，如今几乎没有理由不发送高性能处理器。这正是[Mohamed Elhariry]在他的 [PiX](https://github.com/moelha/PiX) 项目中所做的，它将树莓 Pi Zero W 变成了一个整洁的小飞行数据记录器。

硬件有你可能期望从飞行记录器，包括加速度计，陀螺仪和压力传感器。此外，它还携带了温度和湿度传感器，当然，还有一个摄像头。一个 64 GB 的 microSD 卡提供存储，而一个 LiPo SHIM board 允许整个系统从 150 mAh 的电池运行。所有组件都是现成的分线点，这使得组装非常简单，只需焊接几个连接并用一点胶带固定模块即可。

[该项目在 GitHub](https://github.com/moelha/PiX) 中，包括 python 代码、硬件原理图和详细说明。如果你曾经想开始安装一个模型火箭，这看起来是一个很好的资源。如果你只是想看一次发射的景色，回购中还有一段从实际飞行【34mb GIF】中捕捉到的[视频。](https://github.com/moelha/PiX/blob/mastimg/video_from_rocket.gif)

使用商业模块似乎很方便，但如果定制硬件更适合你，[看看这些设计用于火箭内部的 22 毫米圆形 PCBs】。](https://hackaday.com/2018/02/24/these-small-pcbs-are-made-for-model-rocketry/)