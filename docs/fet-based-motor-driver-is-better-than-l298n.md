# 基于 FET 的电机驱动器优于 L298N

> 原文：<https://hackaday.com/2019/12/29/fet-based-motor-driver-is-better-than-l298n/>

如果你想制造一个带电机的小型机器人，你可能需要一个 L298N 来连接你的微控制器和电机，可能是 H 桥配置。[Dronebot]已经多次使用这样的 L298N 芯片。在下面的视频中，他使用了 TB6612FNG，利用了该设备对 MOSFETs 的使用。TB6612 可能会贵一点，但显然物有所值。

你可以得到小芯片的分线板。[DroneBot]查看几个现成的分线板。不过，它们与插件不兼容。例如，L298N 可以在 4.5 至 46V 的电压下运行电机，而 TB6612 可以在 2.5 至 13.5V 的电压下运行电机。L298N 还能处理更多的电流。但由于其效率相对较低，所以需要一个散热片。TB6612 拥有高达 95%的效率，并且具有低电流待机模式。当然，TB6612 下降的电压要小得多，如果你使用的是低压电机，这是非常好的。

假设新设备适合你的硬件，软件和 L298N 程序并没有太大的不同。如果您知道如何使用 L298N，您可能只需要抢到一块分线板，下载库，然后开始比赛——没有双关语。

如果你想要更多关于 h 桥的[基础知识，我们已经讨论过很多次了。当然，如果你想要真正的老学校，你总是可以使用](https://hackaday.com/2014/04/25/a-h-bridge-motor-controller-tutorial-makes-it-simple-to-understand/)[继电器](https://hackaday.com/2011/04/14/reversible-relay-based-motor-controller/)。

 [https://www.youtube.com/embed/JPPTRj0KWbg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/JPPTRj0KWbg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

