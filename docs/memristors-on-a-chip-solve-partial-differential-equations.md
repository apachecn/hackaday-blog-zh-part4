# 芯片上的忆阻器解偏微分方程

> 原文：<https://hackaday.com/2018/08/04/memristors-on-a-chip-solve-partial-differential-equations/>

我们总是被告知基本的无源元件是电阻、电容和电感。但是在 1971 年，[Leon Chua]引入了忆阻器的概念——一种具有记忆的电阻器。惠普在 2008 年创造了一个，从那以后我们就没有迫切需要使用它了。在最近的一篇自然杂志文章中，[Mohammed Zidan]和其他人讨论了一个芯片上的 32 乘 32 忆阻器阵列，他们称之为记忆处理单元。这种芯片上的模拟计算机对于 CPU 在历史上效率不高的某些操作非常有用，包括求解微分方程。其他应用包括用于机器学习和天气预测的矩阵运算。这篇论文在付费墙后面，尽管通常能找到学术论文的地方可能很快就会有了。

使用这些模拟元件进行高精度计算有几个关键点。首先，阵列以无源交叉排列的方式设置。此外，忆阻器被量化，使得不同的电阻值代表不同的数字。例如，可以具有 16 个不同电阻值的忆阻器元件将允许它作为基数为 16 的数字来操作。

流过忆阻器的电流自然会产生与电流乘以电阻的乘积成比例的电压，这就是欧姆定律。交叉开关执行求和功能。因此，输入出现在交叉杆的行上，而列得到的输出对应于输入乘以作为系数的忆阻器值，然后在列上求和。如果您喜欢使用电压，也可以通过调整系数来实现(例如，2 乘以 X 等于 X 除以 1/2)。您可以用几种方法测量由此产生的输出电流，包括将其转换为电压。从论文来看，这最后一种方法似乎就是他们正在做的事情，将输出电流转换为标准转换器可以读取的电压。

那么，以一种过于简化的方式，你可以把阵列想象成一排电位计，在刻度盘周围有数字标记。输入电压或电流进入行和列，对该列上的所有输出求和以产生结果。唯一的区别是这些电位计是电子设置(和复位)的。

这可能有点过于简化，但它确实表达了基本的思想。如果你试图处理论文，要小心。用微分方程模拟氩等离子体反应器是一项艰巨的任务，不管你用什么样的计算机。

微分方程有着悠久的历史[模拟解](https://hackaday.com/2016/08/08/differential-analyzer-cranks-out-math-like-a-champ-at-vcf-2016/)。我们已经写过关于[忆阻器](https://hackaday.com/2015/07/02/new-part-day-memristors/)及其在神经网络中的用途。