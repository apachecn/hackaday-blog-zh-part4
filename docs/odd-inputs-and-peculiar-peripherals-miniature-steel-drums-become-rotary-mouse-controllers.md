# 奇怪的输入和特殊的外围设备:微型钢鼓变成了旋转鼠标控制器

> 原文：<https://hackaday.com/2022/06/29/odd-inputs-and-peculiar-peripherals-miniature-steel-drums-become-rotary-mouse-controllers/>

当[bornach]浏览他办公室的自由循环箱时，他发现了一个古老的新奇玩具，可以让你在微型钢鼓上演奏简单的曲子。这样的事情可能会有趣五分钟左右——如果它有效的话，而这个没有。但是，bornach 没有扔掉它，而是在那些小鼓顶部的电容触摸板上发现了一个机会:它们看起来非常适合被修改成一个不寻常的鼠标光标控制器。

[![A steel drum toy being used to control a mouse cursor](img/f2136631be1c5634d8b9bd3f8bb48396.png)](https://hackaday.com/wp-content/uploads/2022/06/Steel-Drum-Mouse-operation.gif) 行动从【博尔纳奇】撕掉原来的 PCB，换上一个 ESP32 D1 Mini 开始。该板有一堆方便的触敏针，可以直接与鼓的触摸板连接。然后，他对 ESP32 进行编程，将信号解释为鼠标移动和按钮按压，并通过蓝牙连接将结果发送给计算机。

鼠标滚轮的操作非常简单，看起来几乎就是为此而制造的:你用手指在触摸板上画圈滑动，在 X 或 Y 方向移动光标，然后触摸中间的触摸板进行点击。左边的鼓水平移动光标，而右边的鼓垂直移动光标，但是也有一种模式可以将右边的鼓用作滚轮。

旋转 X/Y 控件让人想起蚀刻素描；虽然对于日常使用来说可能过于笨拙，但在一些需要做出单像素精度动作的情况下，它们可能会派上用场，只要在一些在线广告上点击那些微小的“关闭”按钮。

令人惊讶的是，这并不是我们推出的第一款蚀刻素描风格的鼠标:[这个可爱的小木制设备](https://hackaday.com/2016/12/07/usb-etch-a-sketch-style-mouse-is-more-analog-than-youd-think/)以类似的方式工作。

 [https://www.youtube.com/embed/5nYREtXK6io?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/5nYREtXK6io?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[![Odd Inputs and Peculiar Peripherals Contest](img/4c1d0cbefc0219866bf706dbbac40818.png)](https://hackaday.io/contest/185414-odd-inputs-and-peculiar-peripherals)