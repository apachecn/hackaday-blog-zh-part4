# 将时序图转换成 ASCII 图片，以便更友好地粘贴

> 原文：<https://hackaday.com/2022/04/04/turn-timing-diagrams-into-ascii-art-for-friendlier-pasting/>

我们都曾使用过基于文本的字段，仅限于 ASCII 最终会成为一种限制。这就是[Luke Wren]创建 [asciiwave](https://github.com/Wren6991/asciiwave#asciiwave-wavedrom-to-ascii-art) 的原因，这是一个将 WaveDrom 时序图转换为 ASCII 艺术的神奇工具。与图像不同，ASCII 时序图适合粘贴到注释字段、更改日志或其他只接受文本的地方。[更新:正如作者在下面的评论中友好地分享的，这个工具最初的位置是粘贴到 HDL(例如 Verilog)源代码评论中，在那里它有一种特殊的用处。]

WaveDrom 本身是一个漂亮的 JavaScript 工具，我们在之前已经介绍过[。它接受以 JSON 数据表示的时序图，并将可读性良好的数字时序图作为图像直接呈现在浏览器中。](https://hackaday.com/2015/05/25/need-timing-diagrams-try-wavedrom/)

尽管这很酷也很有用，但图像不能粘贴到文本字段中。这就是冲击波的作用。它读取 WaveDrom 使用的完全相同的格式，但生成的是 ASCII 艺术时序图。因此，如果您发现 WaveDrom 很有用，但希望能够生成 ASCII 版本，这是您的解决方案。