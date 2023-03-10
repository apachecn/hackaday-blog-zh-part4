# 1969 年模拟计算机的秘密

> 原文：<https://hackaday.com/2019/09/23/secrets-from-a-1969-analog-computer/>

今天，大多数我们认为是计算机的东西都使用了数字技术。但情况并非总是如此。从计算尺到机械火力解算计算机，再到电子模拟计算机，已经有大量的计算机不是对 1 和 0 进行运算，而是对角度或电压等模拟量进行运算。[Ken Shirriff]正在修复一台由[CuriousMarc]提供的大约 1969 年的模拟计算机。他可能会写几篇文章，但这个月的一篇[主要关注运算放大器](https://www.righto.com/2019/09/reverse-engineering-precision-op-amps.html)。

对于电子模拟计算机，运算放大器是主要的处理元件。你可以输入多个电压来做加法，增益则用于乘法。如果加上一个电容，就可以做积分。但是有一个问题。

典型的运算放大器很适合做我们通常要求它们做的事情。例如，放大音频是运算放大器的一大用途。如果 DC 或几赫兹的性能不是很好，没有人会真的介意。但在模拟计算机中，低频甚至 DC 信号都很重要，任何失调、漂移或增益不规则都会影响计算。

一个解决方案——这台计算机中使用的方案——是加入斩波器。斩波器本质上充当由输入信号调制的载波频率。运算放大器现在可以作为交流放大器执行任务，而不是 DC 放大器，使其更加稳定。最后，另一个斩波器重建信号。虽然问题中的模拟计算机确实使用 IC 作为核心运算放大器，但斩波器和其他电路使它们工作良好，占用了整个电路板。

编程都是用跳线完成的。如果你想更多地了解这些是如何工作的，我们在今年早些时候讨论过它们。我们不禁要问，如果数字计算机没有成功，模拟计算技术会发展到今天的水平。毕竟，我们在 1959 年就有了模拟笔记本电脑。算是吧。