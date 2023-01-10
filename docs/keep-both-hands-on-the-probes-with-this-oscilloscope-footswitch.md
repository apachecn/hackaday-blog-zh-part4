# 用示波器脚踏开关将双手放在探头上

> 原文：<https://hackaday.com/2018/12/02/keep-both-hands-on-the-probes-with-this-oscilloscope-footswitch/>

我们有两只手，所以在用示波器诊断电路时，很自然地想用两只手。问题是，双手都放在探头上会让操作瞄准镜有点困难。要是有办法让你闲置的下半身活动起来就好了。

[这种多用途示波器脚踏开关接口](https://twitter.com/roukemap/status/1066811243237904384)非常有意义，我们想知道为什么这种东西不是更多示波器的标准设备。[Paul Roukema]的接口依赖于 USB 测试和测量类(USBTMC)协议，该协议允许远程控制大多数现代示波器，有点像旧的通用接口总线(GPIB)协议。[Paul]的界面使用 STM32 微控制器与 USBTMC 对话，与是德科技的 Infinium 示波器或泰克 DPO 线对话，因为这些是他必须测试的对象。轻按脚踏开关可打开和关闭采集模式，或触发单次采集。他深思熟虑地将 USBTMC 规范包含在[他的 GitHub 项目](https://github.com/MegabytePhreak/scope-footswitch)中，因此将其应用于其他领域应该很简单。我们甚至打赌，配有 GPIB 接口的老式示波器也能享受同样的免提控制。

拥有低端市场范围，但仍想使用免提功能？ [[Jenny List]关于用 Python 运行 Rigol 的入门文章](https://hackaday.com/2016/11/16/how-to-control-your-instruments-from-a-computer-its-easier-than-you-think/#more-228539)可能会提供一些关于从哪里开始的提示。