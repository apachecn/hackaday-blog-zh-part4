# 迪士尼打造自主涂鸦无人机

> 原文：<https://hackaday.com/2018/10/13/disney-builds-autonomous-graffiti-drone/>

有没有在一个陌生的地方看到一些涂鸦，并想知道涂鸦艺术家是如何到达那里的？它可能是一架无人驾驶飞机，而不是一个运动少年。迪士尼研究所刚刚发表了一篇有趣的[研究论文，描述了油漆直升机](https://www.disneyresearch.com/publication/paintcopter/):一架在云台臂上装有一罐喷漆的自主无人机。然而，这不仅仅是将颜料罐粘在棍子上:他们建立了一个系统，可以扫描 3D 表面，然后计算如何在其上绘制设计，然后自动完成。这个想法是，他们想用这个来画主题公园难以触及的地方，或者在不派人爬梯子的情况下添加季节性装饰。

 [https://www.youtube.com/embed/YTvr3jCsf0o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/YTvr3jCsf0o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



PaintCopter 是在 DJI M100 的基础上构建的，添加了 Nvidia TX2 和英特尔 UP 处理器板，以提供更多的处理能力。油漆罐安装在云台臂上，云台臂可以通过伺服系统触发油漆罐。使用[英特尔 R200 RGBD(红、绿、蓝深度)相机](https://software.intel.com/en-us/articles/realsense-r200-camera)扫描表面，相机将数据反馈给基站，基站然后构建目标的 3D 模型。基站然后计算无人机在表面上绘制所需设计的路径和方向，然后将其传递给无人机进行实际绘制。该团队制作的例子很简单，但表明该技术在将设计映射到复杂的 3D 表面上时非常有效。目前它只适用于一种颜色，但是作者建议创建颜色渐变和其他更复杂的技术正在进行中。