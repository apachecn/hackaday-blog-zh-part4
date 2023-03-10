# 交互式 Mandelbrot 集合查看器在 FPGAs 上运行

> 原文：<https://hackaday.com/2018/07/15/interactive-mandelbrot-set-viewer-runs-on-fpgas/>

Mandelbrot 集合是一个数学上的奇怪现象，一个简单的函数创造了一个无限复杂的景观，你可以从字面上放大到永远。像大多数人一样，我已经下载了 Mandelbrot set 查看器，并对无限的螺旋和螺线感到惊叹，然后等待每一帧花费几分钟或几小时来渲染，然后放大。[Michael Henning]、[Max Rademacher]和[Jonathan Plattner]决定通过使用笔记本电脑和两块 FPGA 板构建一个交互式 Mandelbrot 集查看器来解决这个问题。

 [https://www.youtube.com/embed/WxDH-1V-4o0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/WxDH-1V-4o0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



这三个人是康奈尔大学的学生，这是他们在[高级微控制器课程](https://classes.cornell.edu/browse/roster/SP18/class/ECE/5760)的最后一个项目。设计很巧妙:笔记本电脑处理用户界面，并呈现 Mandelbrot 集的最终显示。它还向进行数字处理的 FPGA 板发送请求，将所需的计算划分到各个板上。FPGA 板是围绕 Cyclone V SOC FPGA 芯片构建的 [TerASIC DE-1 SOC](http://www.terasic.com.tw/cgi-bin/page/archive.pl?Language=English&No=836) 板，该芯片配有 1GB DDR 3 内存。他们使用了两块电路板，但他们的模块化设计意味着，通过添加额外的 FPGA 电路板，可以很容易地进一步提高系统速度。

结果非常令人印象深刻:用户可以实时放大或缩小并四处移动，分辨率为 1600 x 1200 像素，每秒 60 帧。当你放大时，它确实会慢下来，但这是一个显著的例子，说明 FPGAs 在这种事情上比标准 CPU 快得多。他们已经测试了 2^260 的最大深度，但是他们的系统应该能够到达 2^1700.更深的地方在这个深度，完整的曼德尔布罗集合几乎和可观测的宇宙一样大。

[更新:从 DDR5 更正为 DDR3 内存]