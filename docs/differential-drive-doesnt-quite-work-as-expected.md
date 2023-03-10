# 差速驱动不像预期的那样工作

> 原文：<https://hackaday.com/2021/06/06/differential-drive-doesnt-quite-work-as-expected/>

将两个电机放在一个共享驱动器中是一件非常简单的任务。通过使用类似链条或皮带的东西来连接它们，甚至将它们放在同一根轴上，扭矩可以有效地增加一倍，而不会有太多的麻烦。但是，找到一种方法来保持扭矩不变，同时增加电机的速度，而不是扭矩，就有点复杂了。[李维·让桑]带我们看了他的原型齿轮箱，试图做到这一点，尽管并不是一切都如他预测的那样。

原型基于与差速器相同的原理，但是动力流方向相反。在像汽车这样的东西中，来自驱动轴的单个输入被发送到两个速度不同的输出轴。在这种差速器中，两个不同速度的输入轴驱动一个输出轴，该输出轴的速度是两个输入速度之和。这不仅允许比两个马达中的任何一个更高的输出速度，而且在理论上，它可以通过在相反的方向上旋转两个马达来允许任意精细的速度控制。

第一种设计使用了两个 BLDC 马达，它们各自配有摆线驱动器。每个电机放置在可旋转的外壳中，并且外壳通过皮带彼此连接。这允许次级马达旋转初级马达的外壳，而不影响初级马达旋转的实际速度。有很多东西需要理解，但看一次(或两次)视频肯定有助于你理解它。

当[Levi]开始测量失速扭矩时，试驾并没有按计划进行。事实证明，扭矩不能以他期望的方式相加，尽管驱动器仍然能够将速度提高到高于两个电机中的任何一个。正如他在视频中指出的那样，它仍然有一些有限的用途，但没有达到他的所有预期。不过，这仍然是一个有趣的构建和很好的概念验证，如果你不清楚他的一些设计选择，还有一些其他的构建[深入摆线齿轮](https://hackaday.com/2018/08/24/a-peek-at-the-mesmerizing-action-of-a-cycloidal-drive/)甚至是标准汽车差速器的[拆卸。](https://hackaday.com/2017/04/25/different-differentials-the-pitfalls-of-the-easy-swap/)

 [https://www.youtube.com/embed/2SUiwQVWe8w?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/2SUiwQVWe8w?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[Kelvin Ly]的提示！