# 3D 打印研究机器人平台远程运行

> 原文：<https://hackaday.com/2021/09/27/3d-printed-research-robotics-platform-runs-remotely/>

[开放动态机器人倡议组织](https://open-dynamic-robot-initiative.github.io/)是位于三个国家的五个面向机器人的研究小组之间的合作，旨在建立一个基于扭矩控制方法的开源机器人平台。利用 [3D 打印](https://github.com/open-dynamic-robot-initiative/open_robot_actuator_hardware/tree/master/mechanics)、[几块定制的 PCB](https://github.com/open-dynamic-robot-initiative/open_robot_actuator_hardware/tree/master/electronics)和现成的零件，与同类机器人相比，进入门槛低，成本也低得多。

明眼人会注意到，这只是一个开发平台，所有更高层次的控制都是离机的，由一台单独的 PC 托管。有趣的是，这个机器人实际上是多么低级。运动硬件纯粹是由[磁场定向控制](https://en.wikipedia.org/wiki/Vector_control_(motor)) (FOC)驱动单元驱动的几个 BLDC 电机、一个无线控制器和一些电池。FOC 方法能够实现非常高效的电机换向，提供出色的效率和最大扭矩。对于门外汉来说，深入研究这种方法如何运作的数学原理会让他们大开眼界。附在电机上的光学编码器为控制回路提供位置反馈。

正是这个控制回路有点奇怪，因为它是通过 Wi-Fi 运行的！通常，人们会在腿部单元内利用本地控制回路本地进行所有位置、扭矩和速度感测，以及运行所有肢体运动学和运动规划。这将需要大量的本地处理工作，这会使开发更加困难。

该项目避开了这一点，首先利用了最初针对 ESP8266 和 friends 的 [ESPNOW 协议](https://hackaday.io/project/161896-linux-espnow)。通过[为](https://github.com/thomasfla/Linux-ESPNOW/blob/master/Misc/RT_Preempt_patch_Linux.pdf) Ubuntu Linux 打补丁，并为实时调度启用抢占式多任务处理，以及仔细选择 Wi-Fi 驱动程序，有可能在大约 1 毫秒内将原始数据包发送给机器人，从而实现大约 1 Khz 的控制环路带宽。而且，这个速度足够让[并行运行至少 16 个马达](https://hackaday.io/project/161896-linux-espnow/log/168678-1khz-closed-loop-control-of-up-to-16-motors-over-wifi)。

通过将所有的处理任务推给一台快速的 PC，就有可能在运动学方面变得非常有创造性，并且比嵌入式方法更快地开发新的想法，而不用担心本地 CPU 资源不足。你可以从下面的视频中看到，平台已经非常先进，能够在不平坦和不一致的表面上行走，[垂直跳跃一米](https://www.youtube.com/watch?v=javHeKRKbAc)，以及[从推挤、滑动和其他外部干扰中恢复](https://www.youtube.com/watch?v=6kY0sRYaXyI)。[项目 YouTube](https://www.youtube.com/channel/UCx32JW2oIrax47Gjq8zNI-w/videos) 上有更多测试过程的视频来吊你的胃口。

在[项目 GitHub](https://github.com/open-dynamic-robot-initiative) 上有许多资源库可以探索，这将是你下一个机器人构建的良好开端，所以如果机器人是你的东西，这绝对是一个值得研究的东西。也许从[的研究论文](https://arxiv.org/pdf/1910.00093.pdf)开始，陷进[的话语](https://odri.discourse.group/)？

最新的 12 自由度四足平台，“Solo”去散步:

 [https://www.youtube.com/embed/kGpJpMjCQcA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/kGpJpMjCQcA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



六自由度两足动物，“螺栓”被探头探脑:

 [https://www.youtube.com/embed/x2jYQdjT_es?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/x2jYQdjT_es?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

