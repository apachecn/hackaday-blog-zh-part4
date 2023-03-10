# Python 中的全部内容

> 原文：<https://hackaday.com/2023/01/02/the-whole-thing-in-python/>

[hsgw]用 Python 构建了一个 macropad，在如今选择这种语言来编写固件并不奇怪。但这只是冰山一角。整个过程——从原理图捕捉，通过布线和生成 PCB，甚至延伸到制作外壳— [,都是用 Python](https://hackaday.io/project/188907-keyboard-as-a-python-code) 编程完成的。

macropad 本身并不太寒酸，有一个有机发光二极管和一些漂亮的丝网印刷图形，但这里的重点是演示工作流程。首先使用 [skidl](https://github.com/devbisme/skidl) 定义原理图，使用 [pcbflow](https://github.com/michaelgale/pcbflow) 对电路板进行布局，这使用了一堆 KiCAD 足迹，然后在 [cadquery](https://github.com/CadQuery/cadquery) 中为一个案例进行 CAD 设计，这有点像 OpenSCAD。

结果是整个物理项目从开始到结束基本上都是代码定义的。我们不确定工作流的所有不同阶段是否能很好地协同工作，但是我们可以想象这使得版本控制变得非常容易。对于这样简单的事情来说，编写 PCB 代码可能有些大材小用——手动布局肯定会更快——但它并不能真正扩展。肯定有某种程度的复杂性，你不想点击一个指针，而是打字。把这想象成代码设计的“hello world”。

工作流程中的一些工具对我们来说是新的，但是如果您想深入了解 cadquery，我们会为您提供帮助。【蒂姆·博斯克】的由 555 个定时器(是的，真的)制成的[疯狂 CPU 用的是 pcbflow。如果你想追溯一下 Python PCB 设计的起源，](https://hackaday.com/2021/12/17/implementing-a-cpu-using-555-timers-and-logic-synthesis/)[这篇文章介绍了 CuFlow](https://hackaday.com/2021/03/30/wires-vs-words-pcb-routing-in-python/) ，它是 pcbflow 的基础。