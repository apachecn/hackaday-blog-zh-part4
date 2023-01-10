# 所有 CNC 控制器的母(板)

> 原文：<https://hackaday.com/2020/07/17/the-motherboard-of-all-cnc-controllers/>

如果你正在从零开始制造一台数控机床，你需要做出的决定几乎是无限的。金属或木质结构？焊接还是螺栓连接？正时皮带还是丝杠？即使机械零件被分类，你仍然面临着控制电子方面的选择。这就是像[这种模块化数控控制器](http://www.buildlog.net/blog/2020/07/a-new-fully-modular-cnc-controller/)可以真正证明是游戏规则改变者的地方。

[巴顿·德林]最新创作背后的想法始于他对 ESP32 的 GRBL 港。事实上，当前的控制器与他的 1.0 版开发板有很强的家族相似性，并增加了一些引人注目和有趣的内容。首先，一切都是模块化的——主 PCB 基本上是一个主板，只有 5 伏多一点的电源和一些日常电子设备，外加许多接头。它支持多达六个步进器通道，可以直接安装在带有 Pololu 型模块的板上，也可以作为使用可插拔螺丝端子板的外部驱动器。还有空间容纳五个 IO 模块；当前的模块集合包括一个四通道开关输入、一个继电器输出、一个 RS-485 模块和一个用于与变频驱动器(VFD)主轴控制器对话的 0-10V 接口，以及缓冲 5V 输出模块。最好的部分是 IO 模块规范是完全开放的，所以设计定制模块应该是小菜一碟。

下面的视频简要介绍了控制器。我们真的对这种想法印象深刻，我们将大胆猜测，拥有这样的东西将会启动许多停滞不前的数控机床项目。我们可以想到一家商店最终失去了搬迁的最后一个借口。

 [https://www.youtube.com/embed/IMwXUbWLic0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/IMwXUbWLic0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

