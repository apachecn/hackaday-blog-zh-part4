# 一种让你用像素编码的编程语言

> 原文：<https://hackaday.com/2020/01/03/a-programming-language-that-lets-you-code-with-pixels/>

这种编程语言给你的程序类似于现代艺术。幸运的是，这是这种语言的一个特点，[以著名的抽象画家皮埃特·蒙德里安的名字命名为皮埃特](https://www.dangermouse.net/esoteric/piet.html)。

这种语言使用 20 种不同的颜色，颜色从红色到黄色到绿色到青色到蓝色到品红色，亮度从亮到正常到暗。这种代码是由可识别的颜色组成的图形形成的，每个像素包含了大量的信息。堆栈用于存储数据值，如果应用了适当的命令，数据值可以作为整数或 Unicode 字符存在。

![](img/53537eb716d98720ddbfeeb529fdc3a4.png)

程序中的数字用颜色表示，黑色块表示边缘，白色块表示自由区。解释器在方向指针(DP)的方向上物理地滑动块，色调的变化表示基于变化步骤的不同命令。

为了执行程序，Piet 语言解释器从程序左上角的 codel(或单独的代码块)开始，维护一个最初指向右边的 DP 和一个最初指向左边的 Codel Chooser (CC)。DP 和 CC 根据执行情况向右、向左、向下或向上转动。

目前有一个小的程序员社区在为该语言开发示例程序、解释器、ide 和编译器。你可以在这里查看一些示例程序。

[![](img/a94259fde838406ffde9757f03387e00.png)](https://hackaday.com/2020/01/03/a-programming-language-that-lets-you-code-with-pixels/screen-shot-2019-12-30-at-7-47-39-pm/)[![](img/a4c12bae3c0920cda0e3700142745919.png)](https://hackaday.com/2020/01/03/a-programming-language-that-lets-you-code-with-pixels/screen-shot-2019-12-30-at-7-47-58-pm/)[![](img/3af23be0054d5dc7408fc07f35a15555.png)](https://hackaday.com/2020/01/03/a-programming-language-that-lets-you-code-with-pixels/screen-shot-2019-12-30-at-7-48-39-pm/)