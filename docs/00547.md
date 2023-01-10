# 这是您的开源运动跟踪解决方案

> 原文：<https://hackaday.com/2018/09/04/this-is-your-solution-for-open-source-motion-tracking/>

HTC Vive 追踪器将现实世界的物体添加到你的虚拟世界中。虽然虚拟环境中的这些现实世界的物体现在大多局限于任天堂 Zapper for*Duck Hunt*clone 和网球拍，但未来是清晰的:我们将戴着耳机玩 *Duck Hunt* 和 *Wii Sports* 。未来如此光明，它燃烧着。

当然，对于任何一个简洁的计算硬件，都有机会构建一个开源克隆。这就是[Drix]在他的 Hackaday 奖参赛作品中所做的。他发明了一种开源的活体追踪器。它被称为 HiveTracker ，是目前在 3D 空间中追踪物体的最佳解决方案。

在超声波和磁力方法的几次失误后，该团队决定搭载在 HTC Vive 灯塔上。这两个基站首先垂直扫描房间，然后水平扫描。这是一项令人难以置信的技术，[【艾伦·耶茨】在 2016 年黑客日超级大会](https://hackaday.com/2016/12/21/alan-yates-why-valves-lighthouse-cant-work/)上谈到了这项技术。

虽然大多数微控制器的运行速度不够快，无法看到这些激光扫描，但 HiveTracker 背后的团队发现了一个微控制器，带有蓝牙和一个名为“PPI”的功能。这种可编程外设互连*有点，有点*像一个横杆，但设计用于更实时的应用控制。通过正确的软件，HiveTracker 背后的团队能够检测到灯塔，并将位置和方向数据发送回计算机。

这是一个惊人的工作量，结果是显着的。你可以看看下面的视频，看到，是的，这是一个真正的，开源的 Vive 追踪器。

 [https://www.youtube.com/embed/8O7mkd-1-B8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/8O7mkd-1-B8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



The [HackadayPrize2018](https://hackaday.io/prize) is Sponsored by: [![Microchip](img/20eb9d92b47da4c15177567c02a65727.png)](https://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey)  [![Supplyframe](img/2d012d9fc9c7873688699aeadb4742d2.png)](https://supplyframe.com/)