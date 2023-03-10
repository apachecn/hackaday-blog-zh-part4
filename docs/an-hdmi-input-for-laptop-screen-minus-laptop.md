# 笔记本电脑屏幕的 HDMI 输入，不包括笔记本电脑

> 原文：<https://hackaday.com/2019/03/14/an-hdmi-input-for-laptop-screen-minus-laptop/>

例如，几乎所有笔记本电脑都缺乏 HDMI 输入，这对于那些想在路上轻松玩视频游戏的人来说是一个巨大的缺点。至于为什么没有制造商提供这种便利，当我们都可以轻松使用这种尺寸的工作屏幕时，也许没有人能说得清。另一方面，如果你想抛弃电脑的其他部分，你可以利用笔记本电脑的屏幕做任何你想做的事情。

来自[Avner]的这个项目分几部分交给我们。在第一部分中，开始拆卸笔记本电脑，并找到屏幕的数据手册，这使[Avner]能够准备 FPGA 来驱动屏幕。[第二部分](https://www.element14.com/community/groups/fpga-group/blog/2019/03/04/lcd-panel-fpga-with-an-hdmi-sink-external-display)涉及构建 HDMI 接收器，这是一种将来自 HDMI 源的信号解码为其组成部分的设备，以便将其发送到 FPGA。项目的[最后部分](https://www.element14.com/community/groups/fpga-group/blog/2019/03/04/lcd-panel-fpga-with-an-hdmi-sink-external-display)实际上包括向这个令人印象深刻的硬件集合发送视频，以便让视频出现在旧的笔记本电脑屏幕上。

如果你曾经处理过任何涉及数字视频的东西，这个版本是值得一试的。它深入探讨了许多技术细节，包括 HDMI、视频设备和硬件时序问题。这是一个很棒的构建，即使[我们已经看到了类似的项目](https://hackaday.com/2016/07/27/fpga-drives-old-laptop-screen/)，如果你有一些空闲时间和一个备用的笔记本电脑屏幕，绝对值得一试。