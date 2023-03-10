# 使用激光雷达传感器监控您的邮箱

> 原文：<https://hackaday.com/2022/06/06/using-a-lidar-sensor-to-monitor-your-mailbox/>

不得不走到你的邮箱前查看邮件的不便激发了许多黑客安装自动系统，让他们知道邮件何时被投递。邮箱监视器是基于几种不同的机制制成的:一些测量里面物品的重量，一些使用相机和机器视觉，而另一些只是在邮箱的门或挡板被移动时触发。当[Gary Watts]想要为他 20 世纪 40 年代的砖砌信箱安装通知系统时，他的选择很有限:没有要监控的挡板或门，安装机械装置的空间有限，[他决定使用激光雷达传感器来代替](https://www.inspectmygadgets.com/a-lidar-based-letterbox-notifier/)。

激光雷达系统可能因其在自动驾驶汽车中的新兴应用而闻名，它发出激光脉冲，并测量它从表面反射回来所需的时间。就[Gary]的邮箱而言，表面要么是砖墙，要么是靠在墙上的一封信。由于信件是通过一个垂直的槽插入的，它们通常会垂直靠在墙上，为激光提供了一个清晰的目标。

激光雷达模块是由 ST 公司制造的 VL53L0X，连接到 Wemos D1 迷你 Pro 上。D1 通过外部天线与[Gary]的家庭 WiFi 通信，由通过太阳能电池板充电的 18650 锂电池供电。整个系统安装在一个防水的塑料盒内，激光雷达传感器通过 3D 打印的安装支架连接到邮箱内部。在软件方面，邮箱通知程序由 Home Assistant 和 MQTT 提供支持。D1 大部分时间都处于深度睡眠模式，仅每 25 秒醒来一次，以读取传感器数据，并在需要时发送通知。

这些年来，我们已经看到了不少花哨的邮箱显示器:有些是[极其节能的](https://hackaday.com/2020/01/22/a-battery-sipping-cellular-mailbox-notifier/)，有些使用[多个传感器以适应不同的使用情况](https://hackaday.com/2014/11/07/triple-sensor-mailbox-alert-really-delivers/)，还有一些[其他的只是设计精美的](https://hackaday.com/2016/05/14/building-a-sturdy-remote-control-mailbox/)。