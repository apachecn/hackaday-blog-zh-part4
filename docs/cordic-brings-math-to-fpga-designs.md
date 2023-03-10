# CORDIC 将数学引入 FPGA 设计

> 原文：<https://hackaday.com/2018/09/07/cordic-brings-math-to-fpga-designs/>

当我们看到[仓鼠]发布一个 FPGA 项目时，我们总是很兴奋，因为它通常是好东西。他的[最新帖子](http://hamsterworks.co.nz/mediawiki/index.php/CORDIC)没有让人失望，展示了他如何使用 CORDIC 算法在 VHDL 中生成非常精确的正弦和余弦波。坐标旋转数字计算机；有时称为 Volder 算法)是计算双曲函数和三角函数的标准方法。更好的是，该算法只需要加法、减法、位移和一个查找表，其中包含您想要的每一位精度的条目。当然，如果你有加法和负数，你就已经有减法了。这非常适合简单的 CPU 和 FPGAs。

[仓鼠]不仅有 VHDL 代码，但也提供了一个 C 版本，如果你觉得更容易阅读。无论哪种情况，角度都经过缩放，因此 360 度是一个完整的 24 位字，以实现最高精度。虽然在循环中计算结果很常见，但利用 FPGA，您可以并行执行所有运算，并在每个时钟周期生成一个新样本。

VHDL 代码之短令人印象深刻。VHDL 也相当冗长，所以我们想象 Verilog 翻译会非常简洁。奇怪的是，虽然 [OpenCores](https://opencores.org/projects?cat=Arithmetic%20core&expanded=Arithmetic%20core) 有一些 CORDIC 项目，但我们没有看到任何用 Verilog 编写的项目。然而，我们确实在 [GitHub](https://github.com/cebarnes/cordic/blob/master/cordic.v) 上找到了一些，包括来自【ZipCPU】的[相当复杂的一个](https://github.com/ZipCPU/cordic/tree/master/rtl)。

CORDIC 的历史也很有趣。[Jack Volder]为一家国防承包商工作，他的任务是用更精确和实时的东西替换 B-58 轰炸机导航计算机上的模拟解析器。1956 年，他基于 CRC 手册中的公式构思了 CORDIC，但在他们制造出使用这些公式的设备之前，他离开了公司。1965 年，[Volder]制造了 Athena，一个使用 CORDIC 的台式计算器，但惠普没有咬它，尽管它确实影响了早期的惠普机器。