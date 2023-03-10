# 拆除新加坡新冠肺炎 TraceTogether 令牌

> 原文：<https://hackaday.com/2020/06/25/teardown-of-the-singaporean-covid-19-tracetogether-token/>

抗击新型冠状病毒疫情的很大一部分是追踪接触者的做法，即可以追踪感染者的下落，并对过去几天与此人接触过的任何人进行新冠肺炎病毒检测。虽然智能手机应用程序一直是这种跟踪的流行选择，但它们有一系列限制，这就是 TraceTogether 硬件令牌试图规避的问题。现在[Sean "Xobs" Cross] [已经看到了一旦令牌启动，令牌内的硬件](https://xobs.io/trace-together-token-teardown/)。

[![](img/cc46000c37fa81ec3e31a5d1a74e1aea.png)](https://hackaday.com/wp-content/uploads/2020/06/simmel-concept.png)

The Simmel COVID-19 contact tracer.

最近，【Sean】和[【Andrew " bunnie " Huang】](https://www.bunniestudios.com/blog/?p=5820)以及其他几个人被新加坡政府技术中心要求审查他们的 TraceTogether 硬件令牌提案。其核心类似于 [Simmel](https://simmel.betrusted.io/) 联系人追踪解决方案——两者都在研究——联系人存储在设备中，蓝牙通信，不可充电电池的运行时间为几个月或更长。

使用的寻人协议是 [BlueTrace](https://en.wikipedia.org/wiki/BlueTrace) ，这是一个针对数字触点寻人的开放应用协议。它由新加坡政府开发，最初用于他们的 [TraceTogether 移动应用](https://en.wikipedia.org/wiki/TraceTogether)。

这款智能手机应用程序显示出许多问题。首先，苹果不允许 iOS 应用程序在后台使用蓝牙，要求应用程序在前台活跃才能使用。苹果有自己的追踪协议，但它没有涵盖建立完整联系图的要求，正如[Andrew] [更详细地涵盖了](https://www.bunniestudios.com/blog/?p=5820)。最后，对于那些最近没有(兼容的)智能手机的人，或者根本没有智能手机的人来说，这个应用程序通常没有什么用处。

开发这些设备的许多挑战在于使它们低功耗，同时仍然使蓝牙收发器足够活跃以供使用，以及有足够的空间来存储交互和跟踪协议中使用的临时令牌。随着 Simmel 和 TraceTogether 标记在未来几个月的推出，看看这些预测的效果如何将是一件有趣的事情。