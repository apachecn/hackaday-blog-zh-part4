# 蓝色药丸作为一个书呆子瑞士军刀

> 原文：<https://hackaday.com/2020/11/22/blue-pill-as-a-nerdy-swiss-army-knife/>

不是每个人都买得起示波器，我们中的一些人一半时间都找不到 USB 逻辑分析仪。但我们通常可以得到一个微控制器套件，如果给它适当的代码，它可以变成一个临时的工具。一个完美的例子是【马克·鲁宾】开发的 *buck50* ，一个[开源固件，将一个 STM32“蓝药丸”变成一个多用途测试测量仪器](https://github.com/thanks4opensource/buck50)。

buck50 内置了大量功能，包括示波器、逻辑分析仪和总线监控器。该器件是一个双向通道，还带有 GPIO 控制和 PWM 输出。这个项目中确实包含了大量的功能。[Mark]提供了一个 Python 应用程序，该应用程序公开了一个基于文本的 UI，用于通过命令和大量命令来配置和使用设备，这使它变得非常乏味。有许多选项可以用来可视化捕获的数据，包括 gnuplot、gtk wave 和 PulseView 等等。

[Mark]不仅在固件方面，而且在文档方面都做得非常出色，我们真的认为这使该项目脱颖而出。命令都有很好的文档记录，一切都可以在[ [GitHub](https://github.com/thanks4opensource/buck50) ]上找到，以满足您的黑客乐趣。如果你打算在网上订购一种蓝色药丸，你可能想了解一下[周围漂浮着的](https://hackaday.com/2020/10/22/stm32-clones-the-good-the-bad-and-the-ugly/)克隆人的本质。

谢谢[JohnU]的提示！