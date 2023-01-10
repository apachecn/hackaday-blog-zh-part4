# Tardygrade Walker 是 3D 打印设计的一课

> 原文：<https://hackaday.com/2021/07/23/tardygrade-walker-is-a-lesson-in-3d-printed-design/>

用 3D 打印机快速制造复杂零件的能力创造了一个展示机械设计技能的平台。在[Dejan Ristic]的能干的小[缓慢行走机器人](https://hackaday.io/project/180210-tardygrade)的情况下，这是真实的，它只使用了两个伺服系统和一堆聪明的 3D 打印部件。

机器人的底盘被分成两个组件，每个组件的对角都有一对脚。当一双脚抬起机器人时，机器人的另一部分可以在返回之前旋转，从而允许机器人转向。一个伺服控制脚的动作，另一个根据需要旋转身体。基于 ESP32 的控制器创建了一个 web 服务器用户界面，电源来自 lipo 电池。

这个机器人有趣的地方在于[Dejan]是如何设计它来进行打印和组装的。所有部件都可以在没有支撑的情况下打印，并在正确的方向上优化强度。在装配中只有六个螺钉固定伺服和伺服喇叭，而其他所有部件都使用搭扣配合或短灯丝。休息过后，看看视频，了解一下这个机器人的设计和细节。即使是脚的接触面也经过精心设计，以实现在平坦表面和小障碍物上的最佳行走。

这让我们想起了[gzumwalt]的 3D 打印小发明，比如[冰箱爬虫](https://hackaday.com/2020/12/10/a-walking-rover-destined-explore-your-fridge-door/)和[机械避边机器人](https://hackaday.com/2020/12/27/mechanical-edge-avoiding-robot/)。