# Raspberry Pi 硬件文档的折衷

> 原文：<https://hackaday.com/2021/06/23/the-compromises-of-raspberry-pi-hardware-documentation/>

[Rowan Patterson]告诉我们他最近在 Raspberry Pi 文档 GitHub 存储库中打开了一张票。他询问了关于树莓 Pi 4 的 USB-C 电源原理图缺乏更新的问题。你可能记得 USB-C 电源问题在 2019 年 7 月由美国覆盖[，然而近两年后，当前官方](https://hackaday.com/2019/07/16/exploring-the-raspberry-pi-4-usb-c-issue-in-depth/) [Raspberry Pi 4 原理图](https://www.raspberrypi.org/documentation/hardware/raspberrypi/schematics/rpi_SCH_4b_4p0_reduced.pdf)仍然显示有缺陷的实现，CC 引脚短路。

负责 Raspberry Pi 文档的[Alasdair Allan]提到他们正在将文档从[Markdown 迁移到 AsciiDoc](https://github.com/raspberrypi/documentation/issues/1911)中，并表示在此之前他们没有时间进行新的更改。但之后，Raspberry Pi 的首席软件工程师[James Hughes]提到，由于缺乏人力，即使在这次更改后，原理图也可能不会更新。

正如[James]所强调的，由于与 Broadcom 签署了保密协议，他们的硬件可能永远不会开放。折衷的解决方案一直是发布有限的外设原理图。然而现在，即使是这些有限的原理图也可能跟不上董事会的修订。

对于 Raspberry Pi 4 的原理图，一个简单的修复方法是让社区中的某个人对 Raspberry Pi 4 电路板布局进行逆向工程，并在修改后的原理图中进行标记。这应该只不过是增加第二个 5.1kω电阻，这样 CC1 和 CC2 各自通过自己的电阻接地，而不是短接在一起。

尽管如此，你可能希望 Raspberry Pi 会为你更新原理图，特别是因为他们已经在内部更新了版本。但是 NDA 迫使他们重复他们的努力，至少现在这意味着他们的公开图表不能反映他们硬件的现实。