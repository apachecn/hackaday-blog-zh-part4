# 调制指示灯锚定现实世界

> 原文：<https://hackaday.com/2019/12/17/modulated-pilot-lights-anchor-ar-to-real-world/>

我们在这里大胆地说，无论你现在在哪里，快速扫视一下周围，可能会发现至少有一个 LED。它们无处不在——我们可以从办公桌上快速找到六个，主要用作指示灯和房间照明。在这种情况下，led 非常普通。但是，如果世界上的发光二极管可以增加一点闪光——真的吗？

这就是 [LightAnchors](https://www.lightanchors.org/) 背后的想法，它自称是一个“空间锚定的增强现实界面”LightAnchors 来自卡内基梅隆大学(Carnegie Mellon University)克里斯哈里森(Chris Harrison)实验室的工作，该实验室寻求与计算机交互的新方法，并利用当今智能手机上无处不在的 LED 点光源和高速摄像头。灯塔基本上是智能手机可以感知和解码的数字编码数据的信标。使用幅移键控来调制目标 LED，并且每个分组包含数据有效载荷和奇偶校验位以及前同步码和后同步码序列。手机上的软件使用相机来隔离点源，跟踪它，并从中提取数据，用于在场景上创建覆盖图。下面的视频展示了许多应用，从通过路由器上的指示灯显示客人登录凭证，到调制拼车车辆的前灯，以便下一位乘客可以找到合适的汽车。

[一篇学术论文](https://karan-ahuja.com/assets/docs/paper/lightanchors.pdf) (PDF 链接)对该协议进行了更深入的研究，并提供了用于创建 LightAnchors 的演示 Arduino 代码。在我们看来，采用 LightAnchors 的两个主要障碍是说服设备制造商支持它们，以及宣传这样一个事实，即看起来像是指示灯的东西实际上可能是更多的东西，但这个想法肯定胜过用于 AR 跟踪的固定标记。

 [https://www.youtube.com/embed/435OSV8Hudw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/435OSV8Hudw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

