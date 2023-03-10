# Lisp 运行这个微控制器挂件

> 原文：<https://hackaday.com/2022/12/10/lisp-runs-this-microcontroller-pendant/>

作为一种编程语言，Lisp 比除 Fortran 之外的任何其他活跃的语言都存在得更久。对于任何经常使用它的人来说，很容易明白为什么:这种语言允许新的语法和宏被流畅地创建，这使得它很容易适应新的情况，[就像在现代 Atmel 微控制器上运行它来控制这个星形挂件上的 LEDs】。](http://www.technoblogy.com/show?2AMW)

这个挂件的硬件非常简单——六个发光二极管排列在星星的各个点上，都由一个由纽扣电池供电的小 ATtiny3227 驱动。这本身并不特别引人注目，但这个特定的微控制器正在运行一个名为 uLisp 的定制 Lisp 解释器的整数版本。该项目的创建者这样做只是因为在最小的微控制器之一上运行高级编程语言所涉及的奇思妙想，这实际上支持这个版本的 Lisp 的有限功能。这种实现方式确实对微控制器的内存和处理能力造成了很大的压力，但只要做出一些让步，它就能毫无问题地运行一切。

就这个项目而言，它给人留下了深刻的印象，除了“我爬山是因为它在那里”的态度。我们以同样的方式欣赏各种各样的项目，[像这个 Arduino 竞争对手，它支持一种只有八个命令的编程语言](https://hackaday.com/2021/01/12/make-room-for-a-new-arduino-competitor-with-native-brainfck/)，或者[这个可以载人的无人机](https://hackaday.com/2015/06/24/autonomous-drones-now-carry-people/)。