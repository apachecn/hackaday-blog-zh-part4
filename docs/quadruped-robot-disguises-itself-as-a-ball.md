# 四足机器人将自己伪装成一个球

> 原文：<https://hackaday.com/2019/12/23/quadruped-robot-disguises-itself-as-a-ball/>

当天网棒球机器人蜂拥攻击时，我们会给他们点颜色看看。他一直在研究 4B T1，这是一个小型四足机器人，可以几乎完美地将自己变成一个球体。![](img/7713b6ea2305b7b0eb7fe0dccef4fc13.png)

一年多以前，在[卡尔]被[PCB 致动器](https://hackaday.com/2018/07/29/flexible-pcb-becomes-the-actuator/)的奇迹分散注意力之前，他就开始研究这个小家伙了。他终于找到时间让它自己运转起来，至少初步结果看起来很有希望。在这个 6 厘米的球体中，共有 12 个伺服系统，每条腿 3 个。所有的机械部件都是在 SLS 机器上用尼龙 3D 打印的，定制的 PCB 板上有一个 BLE 微控制器模块，一个 IMU 和红外接近传感器。一切都是开源的，所有文件都可以在 Hackaday.io 项目页面上找到。

微控制器运行完全逆运动学模型，因此只需输入每条腿所需的尖端和底部坐标，伺服角度就会自动计算出来。最终[卡尔]的目标是让机器人能够可控地行走和滚动。到目前为止，他在这两方面都取得了一定程度的成功，但仍需要一些努力(见下面的视频。我们渴望看到这个令人愉快的令人毛骨悚然的机器人的未来。

步行机器人总是一个有趣的挑战。对于更多我们未来的霸主，来看看这只可爱的小猫和这只真正可怕的渡渡鸟。

 [https://www.youtube.com/embed/aXzuMHtgagU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/aXzuMHtgagU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/WIOOD2jTAN4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/WIOOD2jTAN4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

