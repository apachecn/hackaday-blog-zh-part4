# 激光雷达屋看起来不错，看起来四周都是

> 原文：<https://hackaday.com/2020/12/20/lidar-house-looks-good-looks-all-around/>

灯塔发出光线，使自身和海岸线清晰可见。【丹尼尔的】[灯塔](https://www.instructables.com/Project-Lighthouse-360-Mini-Arduino-LiDAR/)有相反的功能，利用激光绘制出自身周围的区域。使用 Arduino 和 ToF 传感器，这个概念相对简单。然而，连接到 360 度旋转的东西总是一个挑战。

这座灯塔不贵——大约 40 美元——而且很小。事实上，足够小，可以安装在一个机器人的顶部，这将使你在一个足够大的机器人上有很好的情境意识来支持它。你可以在下面的视频中看到这个设备的运行。

这个灯塔用一个普通的方法来解决旋转连接问题:滑环。虽然这些都是机械的，商业单位可以相对可靠。为了发送所有信号，滑环需要六根导线，这意味着有六根导线逻辑上穿过旋转部分。驱动电机以 60 RPM 的速度旋转，但有两个相隔 180 度的传感器，可以将扫描速度提高一倍。3D 打印的外壳用的是 PLA，看起来很棒。

当然，真正的诀窍是在你的机器人或任何正在监听灯塔的东西中有意义地使用所有这些数据。然而，这是一个不同的话题。如果你认为两个 ToF 传感器不错，[为什么不试试三个](https://hackaday.com/2018/06/29/xlidar-is-a-merry-go-round-of-time-of-flight-sensors/)？

 [https://www.youtube.com/embed/uYU534Wn4lA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/uYU534Wn4lA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

