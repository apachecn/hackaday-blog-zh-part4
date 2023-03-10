# 让 KiCad 和 Python 制作您的线圈

> 原文：<https://hackaday.com/2020/10/19/let-kicad-and-python-make-your-coils/>

我们喜欢假装我们的电路和图表一样完美。但事实上，PCB 走线具有不必要的电阻、电容和电感。另一方面，这意味着您可以使用这些跟踪来构建组件。例如，一个非常小的电流检测电阻只不过是一条很长的 PCB 走线，这种情况并不少见。使用 PC 层来去耦电容和创建精确的传输线路也是例子。[IndoorGeek]带我们了解他使用 KiCad 在 PCB 上制作线圈的过程。为了帮助解决这个问题，他使用了一个 Python 脚本来处理这些圆圈，这是 KiCAD 遇到的问题。

这个想法很简单。即使是 PCB 上的扁平铜线，线圈也有电感。在这种情况下，线圈更多的是为了电磁特性，但如果你想建立调谐电路，同样的想法也适用。该项目从开源柔性 PCB 磁铁 FlexAR 获得灵感。

KiCAD 不喜欢弯曲的轨迹，但是由于文件格式是开放的和基于文本的，所以很容易编写可以为您创建形状的脚本。【Joan Spark】提供[剧本](https://gist.github.com/JoanTheSpark/e3fab5a8af44f7f8779c)。顺便说一下，这些磁铁的目标是改善我们之前看到的[机械 7 段显示器](https://hackaday.com/2020/07/27/mechanical-seven-segment-display-really-sticks-out-from-the-pack/)。

能够处理文本文件和修改你的 PCB 布局真是太棒了；这导致了[非常方便的工具](https://hackaday.com/2020/04/25/kicad-panelization-made-easy/)。当然，你可以用 gcode、做[一样的把戏，但是到那时，你已经丢失了很多信息。](https://hackaday.com/2020/01/20/gradient-infill-puts-more-plastic-where-you-want-it/)

 [https://www.youtube.com/embed/Ttqm1z24Ihc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Ttqm1z24Ihc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

