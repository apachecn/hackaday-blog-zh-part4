# 激光投影仪依靠步进器而不是检流计

> 原文：<https://hackaday.com/2022/11/02/laser-project-relies-on-steppers-rather-than-galvanometers/>

激光表演总是很受欢迎。一个非常明亮的单点的疯狂运动产生了流畅的动画，真正抓住了想象力。当然，大型激光表演需要很多设备，但这并不意味着你不能使用类似于[这种自制 X-Y 激光投影仪](https://hackaday.io/project/188046-laserprojector-v2)的东西来享受乐趣。

这实际上是[Stanley]在基于步进器的 DIY 投影仪上的第二次通过；我们在 2016 年展示了他之前的[版本](https://hackaday.com/2016/11/23/cheap-dual-mirror-laser-projector/)。这一次，他想超越“模块混搭”的构造风格，所以他没有使用 Arduino 和步进屏蔽，而是滚动自己的控制器 PCB 来容纳一个 ESP32 和一对 STSPIN220 步进驱动器。新版本的商业版也有所改善——鉴于他在第一台投影仪的图像中看到了不必要的边角软化和直线弯曲，他这次选择了较小的步进器和较小的镜子。还有一个新的 3D 打印底盘来容纳一切，简化了构建，并使两个镜子保持更好的对齐。

下面的视频有建造细节和一些投影仪的精彩镜头——激光和烟雾很难出错。性能看起来相当不错，所以改进似乎有了回报。对于那些在下面发表“应该使用 [galvos](https://hackaday.com/2019/06/29/lighting-tech-dives-into-the-guts-of-laser-galvanometers/) ”评论的人，请放松；[Stanley]说他正在考虑如何为下一个版本制作自己的电流计。

 [https://www.youtube.com/embed/w1O48Ysdiiw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/w1O48Ysdiiw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

