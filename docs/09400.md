# SVG 到 Gerber，没有痛苦

> 原文：<https://hackaday.com/2021/03/01/svg-to-gerber-without-the-pain/>

我们都惊叹于#BadgeLife 和其他社区中用于制作引人注目的设计的高质量 PCB 艺术品，但那些在 PCB 艺术品中尝试过的人会知道这不是一个简单的过程。[Jaseg]可能会有一个答案，不过他的软件 gerbolyze 可以将 SVG 文件处理成 Gerber 图层或 KiCAD 足迹。

他构建它的动力来自于对其他脚本的失望体验，这些脚本只是简单地尝试光栅化任何给它们的 SVG，或者不完全支持完整的 SVG 规范。它是为最少的预处理而设计的，允许尽可能简化流程。它包含了一个位图矢量器来处理任何可以向它抛出的东西，GitHub 库有完整的说明，包括不同设置的输出示例。

这是 PCB art 工艺长期改进的最新进展，但这绝不是我们第一次冒险走上这条道路。特别是[Brian Benchoff]在多色印刷电路板的生产上[做了很多工作](https://hackaday.com/2018/02/26/successful-experiments-in-multicolor-circuit-boards/)。