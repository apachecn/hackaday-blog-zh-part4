# 本周失败:基于激光的视觉暂留装置

> 原文：<https://hackaday.com/2018/11/18/fail-of-the-week-laser-based-persistence-of-vision-gadget/>

[XTronical]关于基于激光的视觉暂留装置的想法失败了，但基本想法似乎是合理的。一排廉价的红色激光照射到一面旋转的镜子上，并被反射到远处的表面上，形成 8 条扫描线。反射物体传感器检测镜子的位置，通过快速打开和关闭单个激光器，可以绘制出图案。

不管怎样，这是我的想法。一个快速原型由一些小而经济的红色激光二极管和一个热粘在一个小 DC 马达轴上的双面镜组成。[XTronical]担心旋转镜可能不稳定或不可靠，但这部分表现得很好。他发现，问题主要出在激光上。

[XTronical]曾希望通过 Arduino 的数字 I/O 引脚直接打开和关闭激光，但这里有许多小问题阻碍了该项目。首先，热胶便于安装，但用手校准激光器很麻烦，而且热胶使得在单元发生故障时进行维修很麻烦。此外，光束的亮度和光斑大小不一致，导致视觉效果不佳。[XTronical]通过施加和切断电源来控制激光的方法也可能是一个麻烦的来源。有可能这些激光器开关速度不够快，但不测量很难说。

小问题的积累会使明智的想法变得不可行，这里的情况似乎就是如此。下面嵌入了视频概述；这种方法是注定要失败的，还是可行的？

 [https://www.youtube.com/embed/MjrRxMAGKe4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/MjrRxMAGKe4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



视觉暂留小工具有各种形状和大小，[甚至跳绳](https://hackaday.com/2014/04/17/the-persistence-of-jumping-rope/)也被用作 PoV 显示器，很遗憾这种显示器的尝试没有成功。