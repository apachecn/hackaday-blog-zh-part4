# 从健身追踪器中提取显示数据

> 原文：<https://hackaday.com/2019/10/27/pulling-display-data-off-of-a-fitness-tracker/>

[Aaron Christophel]为他的 D6 健身追踪器写了另一个聪明的黑客。利用 OpenOCD 和 Pygame，他展示了如何从追踪器的屏幕上获取数据并发送给电脑。

这本书因其简洁而吸引了我们。首先[Aaron]启动连接到 D6 的 OpenOCD 服务器。然后，一个简短的 Python 脚本通过 telnet 连接到服务器，读取屏幕数据，并使用查找表将数据变成 PC 屏幕上的重复显示。如果你更喜欢视觉学习，休息后会有一个演示视频。

D6 是一款受欢迎的健身追踪器，通常会重新贴牌，以极低的价格出售。[Aaron]是这些北欧 nRF52 供电设备的忠实粉丝，我们之前报道过他的一些黑客行为。如果你想了解更多关于这些有趣的小装置的信息，这里有一篇关于它们内部工作原理的文章。

 [https://www.youtube.com/embed/5ymh3p8gKiQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/5ymh3p8gKiQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

