# 滑移转向自动割草

> 原文：<https://hackaday.com/2019/08/28/skid-steer-mows-airport-grass-autonomously/>

当然，修剪草坪是件麻烦事。没有人真的愿意花时间和金钱去种植一种不生产粮食的作物，但我们还是这样做了。如果你在郊区照看四分之一英亩的土地，这不会耗费太多的时间，但是如果你照看的草和罗比一样多，你可能也会造出类似于 T2 的自主滑移式割草机。

这个东西也不是普通的装有随机电子设备的推式割草机。这是一台真正的割草机，本质上是一台装有刀片的拖拉机。由于这是一个滑移转向，它依靠两个手柄来控制左右驱动轮的速度。制造一些伺服连杆将它们连接到专门的伺服系统上，负责转向部分，大脑是 [ArduPilot](http://ardupilot.org/) 连接到一系列无线电、GPS 和指南针上，允许它在机场跑道上行驶，而不干扰任何飞机。

这是一个严重的建设，并进入了很多细节，伺服和联动应该如何表现，所有的软件如何工作，以及实际安装一切割草机的问题。整个项目也是开源的，所以即使你没有整个机场跑道要修剪，你也可以在那里找到一些东西来帮助你的小块草地。

感谢[文森特]的提示！

 [https://www.youtube.com/embed/nCaJzeuDVOQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/nCaJzeuDVOQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

