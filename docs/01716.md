# 具有反馈的远程 RFID

> 原文：<https://hackaday.com/2019/01/17/long-range-rfid-with-feedback/>

不久前，我们发表了一篇关于研究人员将传感器数据添加到无源 RFID 标签的文章，一位读者的评论让我们转向了消费者/制造商版本，任何人都可以立即开始使用。如果你赶上了，无源 RFID 技术是背后的关键 fobs 和贴纸，不需要电源，只是接近阅读器的天线。这是一个更加“黑客”的版本，它处理离散信号而不是模拟信号。然而，这并不需要用户从头开始编写新的库和编程新的标签，所以这是一个权衡。Sparkfun 提供了一个超高频阅读器，可以同时监控本文中显示的 25 个超高频标签。

为了构造这些增强型标签中的一个，天线迹线被断开，然后通过诸如玻璃破碎传感器、温度限制开关、门铃或光传感器之类的开关设备进行布线。每当连续性恢复时，标签将高兴地发回其预编程的数据，并且读取器将确认某处某个标签正在看到一些活动。没有人说这不能应用于廉价的 RFID 阅读器，如果你只是想要一个温度警告给你的壁虎玻璃鱼缸或光传感器给你的 T2 温室的密封控制器。

谢谢你，[迈克·梅森]，感谢你关于 *[RFID 比 ID](https://hackaday.com/2018/12/30/rfid-doing-more-than-id/)* 做得更多的提示。

 [https://www.youtube.com/embed/fpcyilzJE7c?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/fpcyilzJE7c?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

