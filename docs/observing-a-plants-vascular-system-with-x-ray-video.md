# 用 X 射线录像观察植物的维管系统

> 原文：<https://hackaday.com/2021/11/23/observing-a-plants-vascular-system-with-x-ray-video/>

[本·克拉斯诺]有一种本领，当东西在移动时，他能向我们展示里面的东西。本周的*应用科学*实验让[制作物体的延时 x 光视频](https://benkrasnow.blogspot.com/2021/11/x-ray-timelapse-of-fluid-movement-in.html)。这种植物的维管系统只是其中的一个例子，其他的例子还有一个表盘时钟和 DSLR 上的变焦镜头。

![X-ray of plant](img/cf42a3e4c4c64af6c6c9dfce76c5bc94.png)这里的诀窍是有一个可以重复使用的 X 射线感应面板。大约需要五秒钟的曝光时间来抓取每一个 40×40 厘米的帧，然后将它们组合成视频。

现在看着机械装置移动很酷——2015 年[Ben]的视频展示了在扫描电子显微镜下黑胶唱片凹槽中的唱针是什么样子仍然是我们见过的最酷的“相机戏法”之一。但是观看植物功能的脉管系统是那些*啊哈*教育时刻之一的秘诀，所以我们希望各地的七年级生物老师都能找到观看这个视频的方法。

该设备描述得非常详细，但普通黑客读者最有可能想关注 X 射线面板的拆卸,[Ben]将其描述为一个巨大的数码相机传感器，用于接收 X 射线。辐射源是一个 50 千伏 1 毫安的电子管，他将其与牙科诊所使用的电子管进行了比较。(显然，这需要预先考虑，以确保他的自动延时装置在 X 射线管的情况下不会出现故障。)Cyclone III FPGA 驱动面板，通过两个以太网接口与传感器阵列通信。

一个朋友把坏了的面板寄给了[Ben],他很容易就修好了一个损坏的 MOSFET。[biluni]出现在该视频的评论中，分享了他 15 年前在该行业工作时的回忆，即像这样的面板价值 15 万美元！但是考虑到恒星的分辨率，和可重复使用，它肯定会击败旧的电影过程。

 [https://www.youtube.com/embed/j-FHbHoiwNk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/j-FHbHoiwNk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

