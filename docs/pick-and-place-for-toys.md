# 玩具的挑选和放置

> 原文：<https://hackaday.com/2019/04/13/pick-and-place-for-toys/>

玩具是让孩子们在玩耍时开心的好东西，但通常很难让他们明白自己收拾东西的重要性。在这方面，拥有某种形式的机器人来帮助自然是理想的，[和【Paco Garcia】可能会在这一领域领先。](https://medium.com/@pacogarcia3/computer-vision-pick-and-place-for-toys-using-raspberry-pi-and-arduino-68a04874c039)

[Paco]的项目包括将机器人手臂与计算机视觉工具相结合，以便允许它拾取和放置小物体——在本例中是玩具。[机器人手臂为龙门式](https://www.instructables.com/id/Horizontal-Travel-Robot-Arm/)，由 3D 打印组件构建在铝制框架上。计算机视觉方面的事情由 Raspberry Pi 处理，配备标准摄像头，运行 OpenCV 软件进行对象识别。然后，这将命令传递给 Arduino，Arduino 运行步进电机来控制手臂。

[Paco]指出，构建过程中最困难的部分是学习如何在 OpenCV 中从单个摄像头生成真实世界的坐标。掌握了这一点，其余的多米诺骨牌开始倒下。有了三角学和运动学知识，机器人已经能够在其运动范围内可靠地拾取和放置小物体。未来的工作旨在提高机器人的旋转能力和操纵其末端执行器的能力，以实现更多功能。

自然，我们通常会看到用于 PCB 生产的拾取和放置机器—[,这种构建也不例外。](https://hackaday.com/2017/08/29/hackaday-prize-entry-a-manual-cnc-pick-and-place-machine/)休息后的视频。

 [https://www.youtube.com/embed/f3s_uub4P6Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/f3s_uub4P6Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

