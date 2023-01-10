# 呼吸 LED 使用从 Verilog 设计合成的原始逻辑完成

> 原文：<https://hackaday.com/2019/07/20/breathing-led-done-with-raw-logic-synthesized-from-a-verilog-design/>

会呼吸的发光二极管是许多电子设备上有吸引力的装饰品。如今，它们通常由软件控制，但当然在模拟时代也有褪色效果。[Pepijn de Vos]通过从 Verilog 设计构建一个基于硬件的推子来混合一点新与旧，甚至还有时间[深入解释这个过程](http://pepijndevos.nl/2019/07/18/vhdl-to-pcb.html)。

Pepijn 没有使用微控制器和软件，而是用硬件描述语言 Verilog 编写了让 LED“呼吸”所需的逻辑。对于 FPGAs，您可能很熟悉这一点，但用它来规划逻辑芯片的构建也同样合适。Verilog 被合成为一个使用 74 系列逻辑芯片的电路，[在【Dan ravens loft】](https://twitter.com/ZirconiumX/status/1140003607078744064)的工作帮助下，他已经为 Yosys 开放合成套件制作了[库。通过添加一个基本的时钟电路，LED 可以呼吸，并且可以通过改变时钟速度来控制呼吸速度。](https://gist.github.com/ZirconiumX/00ac38534e251ba69dbfc29800e1eced)

这是一种尝试 Verilog 和老派逻辑的有趣方式，尽管这种方式可能无法很好地扩展。Twitter 帖子中有一个有趣的附带说明，[Dan]估计，按照目前的设置，PicoRV32 CPU 将需要 2000 多个芯片来构建。无论如何，这是一个有趣的工具，并且可能有进一步实验的空间。

早在 2002 年，苹果就申请了第一个专利，呼吸 LED 已经成为学习电子产品的人的热门项目。[我们甚至在摩托车上见过它。休息后的视频。](https://hackaday.com/2014/05/08/the-p-u-l-s-e-parking-light/#more-121796)

 [https://www.youtube.com/embed/-1G_gXUzLPg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/-1G_gXUzLPg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



【感谢莫里斯的提示！]