# 3D 印刷光导管将过于明亮的 LED 变成设计和谐

> 原文：<https://hackaday.com/2022/12/22/3d-printed-light-pipe-turns-overly-bright-led-into-design-harmony/>

有许多方法可以有效而优雅地限制 LED 的亮度，但[Tommy]发现使用光导管或扩散器的[可以更好地与设备](https://blog.tommy.sh/posts/early-experiments-with-3d-printed-light-pipes/)集成，特别是当设备本身主要是 3D 打印的时候。

[![](img/2c46c0bb79d0f2c9caacc0a7fcb70bb8.png)](https://hackaday.com/wp-content/uploads/2022/12/infill-test.jpg)

Infill has an effect on appearance. 20% infill on the left, 100% infill on the right.

对于一些问题来说,“金发女孩”方法是正确的选择。[Tommy]设计了一系列不同的 LED 外壳选项，并对每种选项进行了测试，以了解哪种选项最适合他的印刷套件。一些最大的收获包括:

*   100%填充对于均匀的结果是最好的(尽管有趣的阴影在小于 100%填充时出现。)
*   当用 5 毫米高亮度 LED 从下面照明时，7 到 11 毫米的透明 PLA 顶层会发生有趣的事情。随着上层越来越厚，光的均匀扩散开始让位于圆形梯度。
*   发光二极管主要以圆形向上发光。拐角总是更暗，如果导轨不是圆的，情况更是如此。随着光导尺寸的增大，这种效应变得更加明显，对其有效尺寸提出了实际的上限。

[汤米]探索这类问题，因为他设计和制造电子合成器仪器，他们大多是 3D 打印的。他探索效率，并且总是乐于分享他的发现，告诉我们什么可行，什么不可行。

当然，处理过于明亮的 LED 的通常方法是限制其电流或通过用 PWM 信号驱动来控制其亮度。正确的方法取决于应用和设计的规模，实际上有很多方法可以解决这个问题。幸运的是，我们自己的[Inderpreet Singh]在这里告诉你如何最好地控制 LED 亮度。