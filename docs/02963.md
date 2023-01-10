# 帮助解决单晶体管闩锁之谜

> 原文：<https://hackaday.com/2019/05/08/help-solve-the-single-transistor-latch-mystery/>

如果你在 hackaday.io 上呆过一段时间，你可能会注意到，该网站的很多人都是“另类”电子逻辑的粉丝。他们的目标是从继电器、真空管、分立晶体管、偶尔还有二极管等东西中创造数字电路，他们提出的设计要么以过时的方式，要么偶尔以新的和意想不到的方式使用这些元件。这正是[马克·谢尔曼]在他的最新项目[中所做的，一个单晶体管锁存器](https://hackaday.io/project/165447-the-real-single-transistor-latch)。

如果你认为每个设计都必须与尖端的集成电路竞争，或者甚至必须有立即的实际应用，你现在不妨停止阅读——如果你要问为什么有人会做这样的事情，你永远不会知道。

鉴于你已经走了这么远，你会感激[马克]提出的东西。众所周知，当反向偏置为雪崩击穿时，双极结型晶体管(BJT)的集电极-发射极结会表现出负电阻特性。正是这个原理使得单个 BJT 可以用作[一个超简单的 LED 闪光灯](https://hackaday.com/2016/10/17/a-vintage-single-transistor-led-blinker/)。[Mark]采用了这一概念，创造了一种可以存储一位信息的单晶体管锁存器。作为奖励——还是一项要求？—晶体管还驱动一个 LED，这样您就可以直观地看到状态。我们以前见过一个[单晶体管触发器](https://hackaday.com/2018/04/18/the-one-transistor-flip-flop/)，但是那个也需要二极管和交流偏置电源。在这款新设备中，所有这些都是不必要的，因此它是根据不成文、不成文和普遍认可的游戏规则向前迈进的一步。

在真正的黑客时尚中，[马克]在没有完全理解它是如何工作的情况下就想出了一个可以工作的设备。乍一看，我们也有点迷惑。因此，[Mark]请求您帮助复制和/或分析电路。休息之后，他解释了他在视频中迄今为止的发现，但主要问题似乎围绕着为什么需要基极电阻，以及为什么它与 2N4401s 一起工作，而不是 2N2222s。

所以，黑客日，这是怎么回事？请在下面的评论中发表意见。

 [https://www.youtube.com/embed/SgRR6Q9CPNY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/SgRR6Q9CPNY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

