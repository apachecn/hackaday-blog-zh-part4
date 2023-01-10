# KiCad 2022 年终总结和 7.0 预览

> 原文：<https://hackaday.com/2022/12/31/kicad-2022-end-of-year-recap-and-7-0-preview/>

[Chris Gammell]与几位 KiCad 开发人员和图书管理员一起主持了 KiCad 2022 年终总结。他们回顾了每晚 KiCad 6 版本中出现的内容，我们可以从 KiCad 7 中期待什么，甚至回答了用户社区的一些问题。在 2022 年的过程中，KiCad 项目的开发团队和库团队都得到了发展。该项目甚至得到了 CERN 制图办公室的初步支持承诺！

对 KiCad 原理图编辑器的改进包括智能导线拖动，它简化了在原理图中移动组件。切换到 PCB 编辑器时，在原理图中选择的元件现在保持选中状态。schematics 的内部文档支持字体、嵌入式图形，并包含指向数据表和其他参考资料的超文本链接。PDF 生成的新功能提供了交互式文件和工作表之间的链接。

KiCad PCB 编辑器中的新搜索面板支持通过封装、网络或文本搜索来查找元件。属性面板允许编辑多个选定项目的通用属性。虽然成熟的自动布线器不在 KiCad 的范围之内，但是“推推式”布线更快更容易。“尝试完成”功能可为当前选定的走线布线快速连接，而“打包并移动”功能可将所有选定的封装定位在邻近位置，以简化电路板布局内相邻封装的放置。

KiCad PCB 编辑器还增加了对使用字体和倒置“挖空文本”的支持，甚至可以在铜带上使用。位图图形可以作为参考插图导入并缩放到布局工作之下。私有封装外形层可用于在封装外形中放置额外的文档。设计规则检查器(DRC)现在可以捕捉更多的布局问题，尤其是那些可能影响可制造性的问题。

这些只是 KiCad 7.0 令人印象深刻的改进的一部分。此外，还增加了电路仿真和建模功能、用于基于脚本的自动化的新命令行界面、对在 Apple silicon 上运行的 KiCad 的 ARM64 支持，以及对默认库的大量添加，包括符号、封装和 3D 查看器模型。

KiCad 团队提出了几个支持项目的方法。总是需要额外的开发人员和图书管理员。财务捐款可以在[kicad.org](https://www.kicad.org/)进行。作为用户，我们可以运行每夜构建，尝试破坏它们，并以详细的错误报告的形式给出反馈。社区测试将有助于使 KiCad 7.0 尽可能可靠。项目团队也在寻找开放的硬件项目，以 KiCad 7.0 作为演示。例如， [StickHub 项目](https://hackaday.io/project/175165-stickhub-the-space-friendly-7-port-usb-2-hub)作为演示包含在 KiCad 6.0 中。

KiCad 7.0 的正式发布目前定于 2023 年 1 月 31 日。在我们等待的时候，让我们回顾一下 2022 年 1 月我们对 KiCad 6.0 版本的介绍。

 [https://www.youtube.com/embed/iQrdXf7SLkw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/iQrdXf7SLkw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

