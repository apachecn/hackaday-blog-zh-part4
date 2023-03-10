# 3D 打印机到 PCB 米勒转换

> 原文：<https://hackaday.com/2019/02/06/a-3d-printer-to-pcb-miller-conversion/>

有 3D 打印机吗？稍加努力，你也可以拥有一台 PCB 铣床。这就是[Gosse Adema]这个巧妙的黑客技术的基础，他[通过为 Dremel 旋转工具建立一个支架并修改 GCode，将 Anet A8 3D 打印机转换成 PCB 铣床](https://www.instructables.com/id/PCB-Milling-Using-a-3D-Printer/)。这种方法意味着对打印机的适应是最小的:唯一的硬件是一个 3D 打印的 Dremel 支架，它代替了打印头。结果是一个令人印象深刻的 PCB 铣床，可以做双面 PCB 和通孔。

[Gosse]在这篇文章中出色地描述了他是如何改装打印机的，以及他是如何将一个 EagleCAD 设计转换成四个 GCode 文件的。PCB 的每一侧都有一个，一个用于通孔，一个用于 PCB 的最终轮廓。这些然后被送入 3D 打印机，并在 Dremel 上用合适的铣刀依次切割。

我们之前已经展示过一些类似的转换，例如 Makerbot 的这种[复古转换](https://hackaday.com/2011/05/21/pcb-milling-with-a-makerbot/)和这种[廉价雕刻师转换](https://hackaday.com/2018/09/12/turning-a-cheap-engraver-into-a-decent-pcb-mill/)，但这一个比那些更详细，涵盖了从 PCB 设计到最终产品的整个过程。