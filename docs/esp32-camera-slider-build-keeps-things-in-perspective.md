# ESP32 相机滑块构建保持事物的角度

> 原文：<https://hackaday.com/2022/06/30/esp32-camera-slider-build-keeps-things-in-perspective/>

我们已经在 Hackaday 上看到了很多相机滑块，这是有原因的:拥有一个真的可以让你的项目文档，尤其是视频，更上一层楼。这是一种力量倍增器构建——在你完成它之后，它可以帮助你让你未来的项目变得更好。但是，我们也不陌生看到这些项目变得过于复杂，这往往会使其他人难以复制。

但这里的情况并非如此。[【马赛丽·卡拉诺维奇】最近发给我们的电动相机滑块](https://sasakaranovic.com/projects/diy-camera-slider/)完全符合你的预期，除此之外别无其他。这并不意味着挖苦——有时最好的方法是保持简单。除非你是专业摄影师或摄像师，否则你不太可能需要复杂的运动装备。这种设计非常适合那些想美化他们的项目视频，但又不想花几个月时间摆弄设计的黑客或制作者。

[![](img/b3308d9691d3baddb5d1b36d2858c990.png)](https://hackaday.com/wp-content/uploads/2022/06/esp32camrig_detail.jpg)

A wheeled platform moves the camera along the extrusion.

该建筑以一块 2020 铝型材为中心，其长度取决于你要拍摄的照片类型。不管长度如何，它都有几个 3D 打印的组件，允许标准的 NEMA 17 步进电机通过 GT2 同步带沿着挤压的长度来回移动一个小推车。在挤压的一侧甚至有一个终点停止开关，让电子设备在启动时“回家”相机。

在轮式平台上，你会发现第二个 NEMA 17 踏步机，这一次是用来旋转一个商业电话/相机安装的平台。结合沿挤出的横向平移，这允许软件在相机移动时将主体保持在帧的中心。

说到这里，[马赛丽]不仅以开源项目的形式发布了这款相机滑块的硬件，还发布了 ESP32 固件的源代码，让你可以从网络浏览器控制整个事情。如下面的视频所示，该界面为用户提供了一种手动调整相机速度和旋转等变量的简单方法。如果给定相机摇摄操作持续的特定持续时间，它甚至可以自动计算出合适的速度。

那是什么？还是太多你喜欢的部分？[如果你真的在寻找最低限度，但对于我们的钱来说，我们认为【马赛丽】在这种设计上取得了很好的平衡:它有足够的功能来提供专业的效果，而不是复杂到无法在一个周末组装起来。](https://hackaday.com/2019/05/08/an-easy-camera-slider-build/)

 [https://www.youtube.com/embed/-t66ZylGClk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/-t66ZylGClk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

