# 旋转时间追踪器为生产力注入新的活力

> 原文：<https://hackaday.com/2021/08/13/rotary-time-tracker-puts-a-new-spin-on-productivity/>

像我们许多人一样，[昆西]在已经成为多功能电脑的电脑上感受到了非工作程序的干扰。那么工作生活平衡之谜的答案是什么呢？我们不确定，但是时间管理和跟踪任务可能会让你达到目标。唯一的问题是，记录这些事情既无聊又乏味，而且太容易忘记，即使是有趣的任务。

类似的商业设备也有服务于这种时间跟踪的目的，但[昆西]想要一个更酷的东西，以同样的方式工作:将指示器转向当前任务，状态被记录在计算机上。[【昆西】没有像 Timeflip2 那样在每一面都贴上信息标签的智能多边形，而是建造了一个旋转任务管理器，用于相同的目的](https://hackaday.io/project/180815-3d-printed-rotary-time-tracker-for-task-management)，但它是用磁铁做的。

除了磁铁，我们最喜欢的部分是聪明的二进制编码工作。[昆西]正在使用三个光敏电阻和一个绿色 LED 来创建一个 3D 打印的灰色编码器，它回避了一次翻转两位的需要。Arduino 负责读取 3 位代码并将其转换回十进制。还会有更多的更新，包括主要的`.ino`文件，但是你可以在等待的时候开始打印。

如果你很难坚持工作，也许你需要一个番茄定时器。这些年来，我们已经看到了一些，从最小的[到雕塑般的](https://hackaday.com/2014/02/09/hack-all-the-things-in-the-time-you-save-with-this-led-pomodoro-timer/)的[。](https://hackaday.com/2018/12/23/a-perfectly-orderly-way-to-manage-your-time/)

[hack adayprize 2021](https://prize.supplyframe.com)主办单位:[![Digi-Key](img/e7d13a315fd6226594212ca8f8762832.png)](https://www.digikey.com/)[![Supplyframe](img/fdb8a432506edeeafacfef227b3d3b33.png)](https://supplyframe.com/)