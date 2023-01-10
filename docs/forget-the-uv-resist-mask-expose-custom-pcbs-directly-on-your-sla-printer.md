# 忘记紫外线抗蚀剂掩模:直接在 SLA 打印机上曝光定制 PCB

> 原文：<https://hackaday.com/2022/08/09/forget-the-uv-resist-mask-expose-custom-pcbs-directly-on-your-sla-printer/>

对于有事业心的爱好者和原型硬件开发人员来说，创建定制 PCB 仍然有些困难。虽然有许多方法可以实现这一点，但它们通常涉及印刷或绘制掩模，用于暴露待蚀刻 PCB 上的光刻胶层。这里[Andrew Dickinson]的[光子蚀刻机](https://github.com/Andrew-Dickinson/photonic-etcher)项目提供了一个有趣的捷径，在将该项目的 Gerber 文件转换成 MSLA 打印机可以处理的格式后，直接使用 MSLA 3D 打印机的 UV 源。

这个概念非常简单:由于 MSLA 打印机基本上是通过创建动态更新的 UV 掩模(通过 LCD 面板或 DLP 系统)来工作的，这意味着 MSLA 打印机可以用来曝光 PCB 的 UV 敏感[光阻](https://en.wikipedia.org/wiki/Photoresist)涂层，有效地使掩模在蚀刻步骤中不溶解。根据使用情况，这可以通过负性和正性光阻涂层来实现。

这种方法的明显优势是，你不需要额外的紫外线源或任何一种单独的面具，只有一个 MSLA 打印机有足够大的工作面积，以配合 PCB 你希望曝光。[Andrew]的项目目前的一个限制是，它只能将 Gerbers 转换为 PWMS (Photon Mono)文件，但这大概可以相当容易地扩展以支持更多的 MSLA 打印机。