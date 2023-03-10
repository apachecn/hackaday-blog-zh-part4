# TurtleAuth DIY 安全令牌(重新)设计为耐用的日常使用

> 原文：<https://hackaday.com/2022/05/21/turtleauth-diy-security-token-gets-redesigned-for-durable-everyday-use/>

[Samuel]第一次尝试制作 DIY 硬件认证令牌取得了巨大成功，但他很快意识到，与在工作台上生活和工作的 PCB 相比，用于日常携带和使用的设备有几个不同的问题需要解决。这导致了 [TurtleAuth 2.1，为日常使用而重新设计](https://blog.thestaticturtle.fr/turtleauth-2-1-a-design-for-everyday-use/)对我们所有人来说都是幸运的，他详细介绍了他所面临的所有挑战和解决方案。

[![](img/1fca8a1aa0edab6ae9c1fdaab925e15b.png)](https://hackaday.com/wp-content/uploads/2022/05/TurtleAuth-2.1.png) 当我们覆盖了[最初的 TurtleAuth DIY 安全令牌](https://hackaday.com/2020/06/10/stm32-blue-pill-turned-gpg-security-token/)时，一切都变得不可思议。然而，经过一年左右的日常使用后，PCB 布局出现了一些问题。[Samuel]决定尝试一种不同的想法，用 PCB 层本身制作一个外壳，而不是 3D 打印一个外壳就完事大吉。

三层 PCB 夹层使元件密封并受到保护，同时还在顶部提供了一个漂亮的大触摸感应垫，两侧是状态 led。空间是一个真正的限制，需要重新设计 PCB，并采用 0402 尺寸的元件，但最终他成功了。至于能够看到发光二极管，而没有任何组件暴露在外？那里没问题；[Samuel]简单地用一些热胶填充状态 led 上的孔，创建了一个便宜、有效、高度耐用的扩散器，还密封了内部。

用 PCB 材料制作外壳真的很棒，而且没有必要重新发明轮子。我们自己的[Voja Antonic]展示了如何以这种方式建造实用美观的外壳的所有信息。