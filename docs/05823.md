# Arduino 驱动天文圆顶

> 原文：<https://hackaday.com/2020/03/02/arduino-drives-astronomy-dome/>

南佛罗里达科学中心最近增加了一个新的 10 英寸望远镜，并转向[安德烈斯·帕里斯]和他的兄弟，以取代手摇圆顶门系统。他们转向一辆 Arduino 和一些强壮的马达司机。你可以在下面看到一些运行中的野兽的视频。

根据 Reddit 帖子，兄弟俩选择了 5A 12V 电机，但决定过度设计，选择了能够处理 20A 峰值电流的 H 桥。红外遥控器允许操作员打开和关闭门，簧片开关感应门运动的极限。

第二个视频显示了电机和 3D 打印的耦合到现有的门齿轮系。由于盒子上的显示器相当亮，操作员可以使用遥控器关闭它们。

看起来好像没有任何代码或图表可用，但我们猜测这种类型的系统将为每个单独的案例定制。事实证明，现有齿轮系的移动并不是最大的问题，相反，它提供了动力。

由于穹顶在旋转，不可能给盒子通电。该系统使用一些电池，现在必须手动充电。然而，兄弟俩计划利用圆顶总是放回同一位置的事实，这样他们就可以使用 Qi 发射器无线充电，当在原位时，该发射器与相关的接收器对齐。

如果你想拥有自己的穹顶，我们和 Wayback Machine 可以提供帮助。我们真的很羡慕那些没有 T2 契约限制的人。

 [https://www.youtube.com/embed/AJAlnIDWrJQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/AJAlnIDWrJQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/z6C4XVKdFAI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/z6C4XVKdFAI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

