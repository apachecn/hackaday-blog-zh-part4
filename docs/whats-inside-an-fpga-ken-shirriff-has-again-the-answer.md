# FPGA 内部有什么？肯·希尔瑞夫(再次)找到了答案

> 原文：<https://hackaday.com/2020/09/21/whats-inside-an-fpga-ken-shirriff-has-again-the-answer/>

FPGAs 在某种程度上是集成电路的 IPv6 它们出现的时间比你想象的要长，它们让你可以做人们最初感兴趣的令人敬畏的事情，但直到最近它们才真正突破自己的领域。围绕它们仍然有一些神话和神秘，就像这些年来复杂性大大增加的任何技术一样，有时最好回到它的最开始以便理解它。嗯，谁会比[肯·希尔里夫]更擅长近距离观察芯片呢，所以[在他最近的努力中，逆向工程了世界上第一个 FPGA:Xilinx xc 2064](http://www.righto.com/2020/09/reverse-engineering-first-fpga-chip.html)。

如果你曾经希望有一个试验板友好的 FPGA，XC2064 可以满足你的需求，尽管它只有 64 个可配置的逻辑模块，但它没有太多其他功能——当然不能与它的现代继任者中最小和最便宜的相比。这就是这个芯片作为逆向工程目标的美妙之处，除了 FPGA 的核心本质之外，别无其他。在介绍了 FPGAs 的一般概念之后，【Ken】(他[并不知道](https://hackaday.com/2016/12/31/8008-exposed/)是[太害羞了](https://hackaday.com/2020/05/20/looking-for-pi-in-the-8087-math-coprocessor-chip/)不敢[打开芯片](https://hackaday.com/2018/06/27/ken-shirriff-found-butterflies-in-his-op-amp/)以便[看到芯片内部](https://hackaday.com/2017/01/07/yes-you-can-reverse-engineer-this-74181/))继续以已知的方式展示芯片图片，以便将内部元件的原理图映射到实际的芯片上，并理解所有的内容。他的最终目标是:完全理解和剖析 XC2064 的比特流。

当然，[逆向工程 FPGA 比特流并不是新的](https://hackaday.com/2015/03/29/reverse-engineering-lattices-ice40-fpga-bitstream/)，毫无疑问，[基于其结果构建工具链](https://hackaday.com/2015/05/29/an-open-source-toolchain-for-ice40-fpgas/)有助于将 Lattice 放在创客社区的地图上([他们起初似乎并不重视](https://hackaday.com/2020/06/05/lattice-semiconductor-targets-bitstream-reverse-engineering-in-latest-propel-sdk-license/)，但[仍然很快](https://hackaday.com/2020/06/06/lattice-drops-eula-clause-forbidding-fpga-bitstream-reverse-engineering/))。我们可能不会看到 Xilinx 发生同样的事情，但谁知道[Ken]下一步会做什么，以及其他人会对此做什么。