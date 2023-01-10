# LittlevGL 为 Micropython 带来 GUI 工具

> 原文：<https://hackaday.com/2019/02/28/littlevgl-brings-gui-tools-to-micropython/>

微控制器是非常有用的东西，但是如果你习惯了为普通电脑编译的简单性，对它们进行编程可能会有点令人生畏。随着时间的推移，这变得越来越容易。社区已经偏离了汇编代码，并创建了更高级的语言，如 Micropython，以允许这些设备以更容易理解的方式进行编程。不幸的是，Micropython 历史上一直缺少一个像样的高级 GUI 库。幸运的是，随着[amirgon]将 LittlevGL 移植到这个平台上，情况不再是这样了。

在一个有屏幕的项目中放一个 GUI 看起来很简单，直到你真正触及实质。一个简单的按钮可以由背景颜色、文本和符号组成——这还没有考虑阴影或其他视觉效果的使用。有一个库来处理繁重的工作可以大大减少开发时间。

LittlevGL 是[kisvegabor]的作品，用 C 语言编程，但这一努力使其与 Micropython 代码集成成为可能。它都是面向对象的，因此在更广泛的 Python 框架中工作得很好。[amirgon]指出，由于 Python 能够运行代码而无需缓慢的编译步骤，因此它对快速开发特别有用。

解决这个问题还有其他方法——[MyOpenLab 就是一个非常通用的例子。](https://hackaday.com/2018/09/21/myopenlab-talks-to-arduino-pi-and-more/)