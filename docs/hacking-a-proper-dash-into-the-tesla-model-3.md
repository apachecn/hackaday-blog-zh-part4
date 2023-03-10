# 黑进了特斯拉 Model 3

> 原文：<https://hackaday.com/2022/01/28/hacking-a-proper-dash-into-the-tesla-model-3/>

特斯拉 Model 3 和 Model Y 是很受欢迎的电动汽车，省却了你在典型汽车中可能会想到的一些常见配置。也就是说，司机前面没有仪表盘；相反，所有信息都单独显示在中控台屏幕上。[Nick Nguyen]并不喜欢这个系统，他决定自己组装一个 dash 集群。

CANdash 以一种简单的方式工作，窥探特斯拉的 CAN 总线，获取与车辆运行相关的所有信息。它能够显示从速度到电池剩余里程的一切信息，同时还允许用户关注冷却液温度以及[特斯拉自动驾驶系统](https://hackaday.com/2021/12/29/the-current-state-of-play-in-autonomous-cars/)当前是否可用等信息。

该版本依赖于 CANserver，这是一种基于 ESP32 的设备，专门用于连接特斯拉汽车上的 CAN 总线并对外共享数据。然后，数据可以通过无线管道传输到运行 CANdash 的 Android 手机上，以显示所有想要的信息。在售后仪表板夹或 3D 打印定制支架的帮助下，手机可以放在方向盘后面，在通常的位置显示数据。

这是一个简单、直接的黑客技术，给特斯拉车主提供了一个有用的功能，否则他们就会从工厂中丢失。美国汽车制造商的汽车被证明是黑客和 DIY 者的沃土，一名男子最近用简单的 mod 在电池更换上节省了数千美元。休息后的视频。

 [https://www.youtube.com/embed/FqJygy1jJZ8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/FqJygy1jJZ8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

