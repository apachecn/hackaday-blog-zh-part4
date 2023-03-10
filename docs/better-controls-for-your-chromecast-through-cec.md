# 通过 CEC 更好地控制您的 Chromecast

> 原文：<https://hackaday.com/2020/01/14/better-controls-for-your-chromecast-through-cec/>

现代家庭影院设备配备了互操作性和便利性的功能，但在实践中，相互竞争的标准和奥秘可能会使其失败。有时候，你必须自己做一点工作来把它们粘在一起，这就是为什么[Victor]开发了自己的小工具。

ChromecastControls 是一款工具，通过改进 Chromecast 与 HDMI 的 CEC 功能的集成，使控制家庭影院变得更容易。CEC 或消费电子控制是一种双向串行总线，集成为 HDMI 标准的一部分。它旨在帮助电视、音频系统和其他 AV 硬件进行通信，并允许用户用一个遥控器控制整个家庭影院系统。常见的使用案例是电视在关闭时向连接的条形音箱发送关闭命令，或者蓝光播放器在按下播放按钮时将电视切换到正确的输出。

[Victor]的工具允许 Chromecast 向环绕声处理器传递音量命令，这通常需要用户用单独的遥控器手动调整设置。当 Chromecast 进入空闲状态时，它还会向连接的电视发送关机命令，从而节省能源。它依靠 PyChromecast 库来拦截网络上的流量，从而向其他硬件发送适当的命令。只需在连接到相关设备的任何 HDMI 端口的 Raspberry Pi 上运行代码，就可以让 CEC 命令通过。

这是一个你可能会觉得很方便的项目，特别是如果你厌倦了一天 24 小时开着电视，因为 Chromecast 从来不会在空闲超时时执行简单的 CEC 命令。CEC 黑客也有很长的历史——[我们早在 2010 年就开始报道了！](https://hackaday.com/2010/08/24/adventures-in-consumer-electronics-control-cec/)