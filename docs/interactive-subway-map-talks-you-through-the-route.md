# 交互式地铁地图告诉你路线

> 原文：<https://hackaday.com/2020/11/15/interactive-subway-map-talks-you-through-the-route/>

老派的铁路监控系统有着惊人的显示，车站和轨道被闪烁的灯光覆盖着，可以跟踪列车在一条路线上的进展。虽然你不太可能在家里安装这样一个 20 世纪中期的大熨斗，但你可以通过[Kothe 的]交互式地铁信息显示器获得类似的美感。

显示器依靠 Arduino Mega 2560 Pro Mini 作为操作的大脑。它驱动一串 WS2812B LEDs，这些 led 与该地区各条地铁线沿线的车站相对应。此外，微控制器驱动 4.3 英寸 Nextion LCD 显示屏。Nextion 显示器的优势在于可以充当独立的人机界面，在板上运行自己的控制器。这意味着 Arduino 不必花费周期来驱动显示器，Nextion 硬件附带了一个有用的软件包，可以快速轻松地设计 GUI 界面。为了获得进一步的反馈，使用了一个 DFPlayer MP3 模块，使系统能够播放预先录制的声音样本，这些样本提供了有关轨道系统的信息。迷人的前面板由激光切割丙烯酸树脂和彩色印刷醋酸纤维制成。

这是一个与世界各地铁路运行的真实铁路信息系统惊人相似的建筑。我们可以想象这种设备在背包客的宿舍或大学宿舍中特别有用，可以帮助那些初到城镇的人找到他们的路。如果你喜欢更简洁的美学风格，[我们也看到了一个准系统 PCB 构建](https://hackaday.com/2020/07/05/live-map-of-london-tube-created-in-pcb-and-lights/)。休息后的视频。

 [https://www.youtube.com/embed/L22DO0J6EdY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/L22DO0J6EdY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/S57thd1ImP8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/S57thd1ImP8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

