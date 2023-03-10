# 深入了解 Sterzo 转向盘

> 原文：<https://hackaday.com/2020/09/11/a-deep-dive-into-the-sterzo-steering-plate/>

原地踩踏板不是最令人兴奋的消遣，所以毫不奇怪，现代技术正被用来使室内骑自行车的体验更具互动性。后轮上有一个支架提供阻力，前轮下有一个可移动的转向板来读取车把角度，现在你可以在 Zwift 等软件提供的虚拟环境中使用你的标准自行车作为“控制器”。

[![](img/0e577aa33518ac596b6c3d0d37ca8009.png)](https://hackaday.com/wp-content/uploads/2020/09/zwiftble_detail.jpg)

Paving the way towards a DIY Sterzo clone

[Keith Wakeham]想要进一步了解 Zwift 如何与他的 Sterzo 转向设备通信，这变成了一场相当史诗般的探索和逆向工程。正如休息后的视频所示，他没有*只是*从嗅探设备的专有蓝牙低能耗(BLE)通信协议，到弄清楚如何在软件中模拟它，这样你就可以推出自己的 Zwift 外设。他还拆开了设备，从其微控制器中取出固件，并假设你可以构建自己的低成本克隆设备，与现有的软件一起工作。

即使你对虚拟自行车毫无兴趣，Keith 为这个项目制作的视频也是必看的。你有没有想过嗅嗅和逆向工程 BLE 通信？寻找一个从消费类设备中获取固件的真实例子？也许在市场上寻找一些如何识别电路板上未知 IC 的技巧？所有这些，甚至更多，都包含在这个近一个小时的黑客之旅中。

另一方面，如果你*对给 Zwift 添加你自己的硬件感兴趣，那么看看[让一辆无支撑的固定自行车与它一起工作](https://hackaday.com/2020/08/04/unbricking-a-2000-exercise-bike-with-a-raspberry-pi-zero-and-bluetooth-hacks/)应该是有用的。*

 [https://www.youtube.com/embed/BPVFjz5zD4g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/BPVFjz5zD4g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

