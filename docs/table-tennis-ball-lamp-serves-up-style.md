# 乒乓球灯发球风格

> 原文：<https://hackaday.com/2020/04/11/table-tennis-ball-lamp-serves-up-style/>

虽然乒乓球漫射的 RGB LEDs 大概永远不会停止炫酷，【thomasj152】感觉球的平板已经有点成为一个很累的概念了。经过大量的努力和两次完整的制作，他已经完成了一个 80 个球的球形灯。结果非常好！

[![](img/16fa85ee8d44535a403d0eda2caea4ef.png)](https://hackaday.com/wp-content/uploads/2020/04/ping-pong-lamp-guts.png) 所有的球都用一些巧妙的 3D 打印件连接在一起，这些打印件的灵感来自经典的六边形和五边形足球布局。[thomasj152]选择这个形状是因为为它编写动画序列相当容易。

该设计还可以很好地分成两半，这使得布线更容易。所有 80 个球都由单个 NodeMCU ESP8266 开发板控制。

这个搁浅的版本是第二个灯[thomasj152]建成。第一个使用了相同的足球风格，但用 RGB LED 条代替，球用激光切割的支撑件固定。条带比绳股平得多，使内部整洁而宽敞。不幸的是，LED 灯带意外烧毁，这是额外的悲哀，因为灯带版本看起来像更多的工作。

这里的亮点是[thomasj152]现在可以为两个版本提供指令。他甚至编写了循环遍历每个五边形和六边形部分的代码，一次点亮一个部分进行测试和健全性检查。将鼠标滑过休息时间，观看演示两个版本并解释差异的视频。

有一堆墙壁空间乞求闪光灯？显然，在不到 24 小时的时间里，我们有可能将 300 个球组成的电视墙组装起来。谁知道呢？

 [https://www.youtube.com/embed/BTB4zlGwbHs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/BTB4zlGwbHs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



通过 [r/arduino](https://www.reddit.com/r/arduino/comments/fudxyl/lamp_made_of_80_table_tennis_balls_80_ws2812b_and/)