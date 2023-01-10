# 以低廉的价格制作一套动作捕捉服

> 原文：<https://hackaday.com/2020/07/19/building-a-motion-capture-suit-on-the-cheap/>

动作捕捉是一种在许多电影中使用的技术，尤其是动画电影。这使得给角色逼真的动作变得轻而易举，因为它们都是基于一个真实的人。[跳棋虫]与一个寻求起步的中学小组一起工作，所以他在预算有限的情况下迅速打造了一个功能强大的装备。

该装备基于胸部单元，该胸部单元连接到放置在身体各点的几个卫星单元。每个单元包含一个博世 IMU，用于测量用户身体各部分的加速度和旋转。数据被反馈到 Arduino Mega，然后传递到运行 Blender 的 PC。运动序列可以在 Blender 中实时录制，或者保存到 SD 卡中，以后再导入。Github 上的文件可供那些热衷于重新创作这个项目的人使用。

这是一个整洁的设置，在低预算的情况下做好动作捕捉。这种钻机在过去会非常昂贵，但现在只需几百美元就能组装完成。我们以前也见过其他的动作捕捉系统。休息后的视频。

 [https://www.youtube.com/embed/FGNmMZX0g_M?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/FGNmMZX0g_M?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

