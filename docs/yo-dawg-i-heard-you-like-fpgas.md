# 哟伙计，我听说你喜欢 FPGAs

> 原文：<https://hackaday.com/2019/06/28/yo-dawg-i-heard-you-like-fpgas/>

当你唯一的工具是一把锤子时，所有的问题看起来都像钉子。如果你的目标是仿真 FPGA 的行为，但你唯一的工具是 FPGA，那么你的钉子和锤子问题开始变得有点有趣。这至少是康奈尔大学的一群学生最近通过将 Xilinx FPGA 的功能编程到另一个 FPGA 中而了解到的情况。

使用过时的硬件来重现几十年前的技术论文可能是可行的，但更简单的解决方案是在更现代的 FPGA 中模拟 Xilinx，即 Terasic 的 Cyclone V FPGA。这使得 I/O 操作更加容易，也减少了对设备重新编程的麻烦。一旦所有这些都设置好了，执行最初在 90 年代的论文中设置的预期任务就简单多了:使用进化算法来区分不同的输入。

虽然我们将把对这个项目中使用的算法和 I/O 的研究作为一个学术练习留给读者，但这确实是一个很好的提醒，即我们不必总是手头有确切的硬件来完成工作。旧电脑可以在更便宜、更现代的设备上复制，当然，过去的 T2 视频游戏现在在其他硬件上也很容易玩。

感谢[Bruce Land]的提示！