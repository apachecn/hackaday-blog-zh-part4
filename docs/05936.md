# GPU 和 FPGAs 上的 Java

> 原文：<https://hackaday.com/2020/03/11/java-on-gpus-and-fpgas/>

曾经有一段时间，在一系列处理器上运行一个程序意味着你在某个高性能的实验室工作。现在你的电脑可能有大量的处理器隐藏在它的 GPU 中，如果你有一个 FPGA，你就有了定制东西所需的一切。TornadoVM 背后的想法是修改 OpenJDK 和 GraalVM，以支持[在 OpenCL 支持的并行架构](https://github.com/beehive-lab/TornadoVM)上运行一些 Java 代码。该系统可以利用多核 CPU、GPU(NVIDIA 和 AMD)、英特尔集成 GPU 和英特尔 FPGAs。

如果您想尝试加速 Java，有一些 docker 容器可以让您快速入门。还有相当多的例子，比如计算机视觉应用。

还有一些更简单的例子，比如这个使用 FPGA 的例子。您可以看到@Parallel 在 for 循环和一些基本任务管理中的使用。如果你愿意，你可以从简单的 [hello world](https://github.com/beehive-lab/TornadoVM/blob/master/examples/src/main/java/uk/ac/manchester/tornado/examples/HelloWorld.java) 开始。

有几篇关于 TornadoVM 的文章和论文，其中一些在付费墙后面。然而，我们喜欢这篇文章，它很好地融合了理论和实践。

Java 并不总是高性能计算的首选，我们不得不考虑如何与使用 OpenCL 的更传统语言的人进行比较。另一方面，如果你懂 Java，这可能是开始并行处理的好方法。

不久前，我们谈到了竞争技术 CUDA T1，但是许多概念是相同的。 [OpenCL](https://hackaday.com/2019/01/24/running-opencl-on-a-raspberry-pi-gpu/) 甚至会在树莓 PI 上运行。