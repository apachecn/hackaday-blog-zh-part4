# 用于 PCB 电机的脚本线圈

> 原文：<https://hackaday.com/2022/10/25/scripting-coils-for-pcb-motors/>

PCB 电感是 Hackaday 上多次出现的一个主题，最著名的可能是[Carl Bugeja]的电磁开发。但是在感应器本身的创造方面还有很多需要学习的地方，[atomic14]最近一直在研究通过脚本自动创造感应器。

一个简单的螺旋轨迹很容易创建，但当创建一个电机线圈的圆形阵列时，需要更复杂的形状。对于一个脚本来说，绘制一个梯形螺旋是一项非常困难的任务，在实现一个可用的设计的过程中，我们遇到了各种各样的算法。

完善了算法，如何带入 KiCAD？PCB CAD 包内置了自己的 Python 环境，但它不是最灵活的开发环境。解决方案是用 KiCAD 编写一个简单的 JSON 解释器，将螺旋生成留给传递 JSON 的外部脚本。这也留下了在其它 PCB 封装中使用相同代码的可能性。

休息下面可以看完整视频。同时更多 PCB 电磁学，[观看【Carl Bugeja】的 2019 Supercon 访谈](https://hackaday.com/2019/11/05/superconference-interview-carl-bugeja/)。

 [https://www.youtube.com/embed/CDhlx_VMpCc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/CDhlx_VMpCc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

