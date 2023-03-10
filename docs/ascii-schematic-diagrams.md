# ASCII 示意图

> 原文：<https://hackaday.com/2021/04/29/ascii-schematic-diagrams/>

我们最近想知道你在一些文档中看到的那些粗糙的 ASCII 示意图——有没有专门的以示意图为中心的工具来绘制它们，或者它们只是使用各种 ASCII 艺术绘制工具手工制作的？让我们惊讶的是，竟然有这样的工具。它叫做 [AACircuit](https://josoansi.de/aacircuit.php) ，由【Andreas Weber】开发。它的历史可以追溯到 2001 年，当时它作为 ASCIIPaint 首次推出。但是，事先警告一下，代码的质量可能是有问题的。根据【安迪】的 [GitHub 库](https://github.com/Andy1978/AACircuit)上的注释:

> **警告:前面有很多复杂的代码**
> 
> 这段代码是我在 2001-2004 年自学 Borland Delphi 3 时创建的。它包含了许多许多的全局变量、非结构化的和未记录的过程代码以及错误的变量名。

[![](img/a38f0898209ccbcdc2bb94041a7f40be.png)](https://hackaday.com/wp-content/uploads/2021/04/aacircuit-duckman-arduino-uno-pinout-1.png)

如果您不想与陈旧粗略的面向对象 Pascal 代码搏斗，那么您很幸运。[混沌有序]制作了一个 python 化的版本，你可以从他的 GitHub 库中获得。我们试用了它，并很快让它在 Ubuntu 上运行起来(在与 pycairo 依赖项角力之后)。这可能不是每个人都喜欢的，但它偶尔会有一些用处。虽然我们不想用 ASCII 示意图来记录计算机主板，但它非常适合快速绘制电路图。

不完全是原理图，但[Duckman]有[一些他用 ASCII-art 制作的 Arduino 引脚排列图](http://busyducks.com/wp_4_1/2015/11/16/ascii-art-arduino-pinouts/)。这些在作为注释粘贴到源代码中时会很有用，记录了您项目的引脚排列。

你推荐什么工具来制作 ASCII 示意图，或者这只是浪费时间？