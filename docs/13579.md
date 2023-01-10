# 经典电子鸡在现代硬件中重生

> 原文：<https://hackaday.com/2022/05/08/classic-tamagotchi-is-reincarnated-in-modern-hardware/>

如果你认为电子鸡是 90 年代末的时尚，现在已经从大多数人的记忆中消失了，那你就错了:这个系列今天仍然很活跃，定期发布新的型号。但是，即使是 1996 年推出的名为“电子鸡 P1”的原型，也有一小群爱好者在保持活力。几年前，当原始硬件的 ROM 转储开始在互联网上传播时，即使那些没有实物的人也可以在模拟器上运行这些虚拟宠物。

但电子鸡硬件的整体理念是它足够便携，可以随身携带。如果你是那些错过电子鸡体验的人之一，你会很高兴地知道[JC]设计了[OpenTama:一个便携式硬件平台，运行原始电子鸡 P1 软件](http://blog.rona.fr/post/2022/04/21/OpenTama-an-open-source-reference-design-for-MCUGotchi)的模拟版本。它几乎和第一代虚拟宠物一样接近，但是增加了几项功能，让你的生活更轻松。

软件平台是[JC]的 TamaLib，我们去年重点介绍了[；实际上，它是一个开源模拟器，允许电子鸡 ROM 在各种现代硬件平台上运行。它还包含几个额外的选项，如能够保存和恢复您的进展或选择定制的 rom。与此同时，OpenTama 硬件是对原始硬件的适当的 21 世纪重新实现:一个鸡蛋大小的小 PCB，带有驱动 LCD 或有机发光二极管显示器的 STM32 微控制器，由 100 mAh 电池供电，可以通过 USB-C 端口充电。](https://hackaday.com/2021/08/10/tamagotchis-everywhere/)

OpenTama 也不局限于 TamaLib 软件:作为一个开源的通用平台，它也可以用作嵌入式编程的学习工具，所以如果你一直想为自己的虚拟宠物编程，或者只是想建立一个奇特的鸡蛋计时器， [OpenTama 的 GitHub 页面](https://github.com/Sparkr-tech/opentama)是一条路要走。我们最近已经看到了不少整洁的电子鸡样项目:这个 [3D 打印的项目配有一个漂亮的复古液晶屏幕](https://hackaday.com/2022/01/27/reject-modernity-return-to-tamagotchi/)，而[这个项目的巨大尺寸确保你不会忘记给它喂食](https://hackaday.com/2014/04/13/desktop-sized-tamagotchi-is-even-harder-to-ignore/)。

 [https://www.youtube.com/embed/EqYy_0zs9ZY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/EqYy_0zs9ZY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

