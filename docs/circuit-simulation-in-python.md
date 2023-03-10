# Python 中的电路仿真

> 原文：<https://hackaday.com/2019/11/30/circuit-simulation-in-python/>

使用 SPICE 来模拟电路在工程中是一种足够常见的做法，以至于“给电路加 SPICE”在词典中是一个完全有效的短语。SPICE 作为一个软件工具从 70 年代就已经存在了，它的开源特性意味着现在有更多的 SPICE 工具可以计算。这也意味着它足够简单，可以与其他软件一起使用，如[将 LTspice 与 Python 集成，用于一些有趣的信号处理电路模拟](https://acidbourbon.wordpress.com/2019/11/26/seamless-integration-of-ltspice-in-python-numpy-signal-processing/)。

[Michael]的最新项目包括在 lt SPICE(SPICE 的衍生产品)中模拟滤波器，然后使用 Python/NumPy 为滤波器提供输入信号并处理输出数据。基本上，它允许您将任何设计的图形模拟电路“插入”到 Python 脚本中，并以任何需要的方式轻松操作它。SPICE 程序并不是没有笨拙之处，能够编写自己的工具来操纵电路是一个强大的工具。

如果您对信号处理(数字或模拟)感兴趣，或者即使您在之前[从未听说过 SPICE，并且想要一种更简单的方法在试验板上制作电路原型之前模拟电路，这个项目绝对值得一看。](https://hackaday.com/2016/02/26/adding-spice-to-your-workbench/)