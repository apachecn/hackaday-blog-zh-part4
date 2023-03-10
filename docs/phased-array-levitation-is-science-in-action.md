# 相控阵悬浮是科学在行动

> 原文：<https://hackaday.com/2021/08/18/phased-array-levitation-is-science-in-action/>

悬浮可能看起来像魔术。然而，对于某些对象，在某些条件下，它实际上是一种已解决的技术。如果你想移动小颗粒或者用超声波触觉反馈做实验，你可能会发现 SonicSurface 是一个有用的实验平台。

这座建筑从[UpnaLab]来到我们这里，这是一个不小的工程壮举。它在一个 16×16 的网格中集成了 256 个超声波发射器，在整个面板上有单独的相位控制。这允许在声表面板上产生复杂的超声波场。两块板也可以以垂直相对的配置配对在一起。这允许微小粒子在 3D 空间中悬浮。

正如您所料，FPGA 被用于处理繁重的工作——在本例中，是 Altera CoreEP4CE6。命令通过 USB 转串行连接从连接的 PC 发送到 SonicSurface。

该板很大程度上仅限于悬浮小球形泡沫片，用超声波场将它们悬浮在半空中。然而，该项目视频显示了这些微小的泡沫片如何附着在线、胶带和其他物体上，以便用超声波阵列操纵它们。

这可能不是一个简单的项目，但它为你自己的悬浮实验提供了一个很好的基础。当然，如果你想从小做起，[那也可以](https://hackaday.com/2021/02/02/building-an-ultrasonic-levitation-rig/)。如果你自己想出任何伟大的悬浮突破，[一定要让我们知道](http://hackaday.com/submit-a-tip)。

 [https://www.youtube.com/embed/vAEZvYlUnEM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/vAEZvYlUnEM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

