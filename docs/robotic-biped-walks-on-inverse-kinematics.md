# 机器人双足行走逆运动学

> 原文：<https://hackaday.com/2020/07/03/robotic-biped-walks-on-inverse-kinematics/>

机器人项目总是黑客的最爱。能够几乎真实地将你的项目带入生活，唤起了一种特殊的快乐，这种快乐真的激发了我们最狂野的想象力。我们认为这是近来充斥市场的交互式技术繁荣的灵感之一。嗯，[Technovation]也有同样的想法，并决定制造一个[全关节机器人双足机器人](https://www.instructables.com/id/Arduino-Controlled-Robotic-Biped/)。

每条腿在脚、膝盖和臀部都有轴点，模仿人类腿的关节。为了控制机器人的运动，[Technovation]使用反向运动学，一种计算关节运动而不是显式编程的方法。用户输入每只脚的末端坐标，而不是每个单独的关节角度，一个特殊的函数输出达到每个末端坐标所需的关节角度。软件的这一部分得到了很好的评论，值得你花时间去钻研。

如果您想改变机器人的高度或步幅长度，[Technovation]在固件中提供了一些全局常数，可以自动调整计算以适应新机器人的尺寸。在这个项目的各个方面中，详细的报道给我们留下了最深刻的印象。该机器人是在 Fusion 360 中设计的，零件是 3D 打印的，为下一个黑客提供了最大的设计灵活性。

也许[tech novation]的双足动物将有助于重振社交机器人热潮。在那之前，祝你黑客生涯愉快。

 [https://www.youtube.com/embed/CxociTjzR4Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/CxociTjzR4Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

