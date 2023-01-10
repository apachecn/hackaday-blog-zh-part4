# 软件定义的… CPU？

> 原文：<https://hackaday.com/2021/07/19/software-defined-cpu/>

当你能编程时，一切都会变得更好，对吗？我们拥有软件定义的无线电、软件定义的网络和软件定义的存储。现在，一家名为 [Ascenium](https://www.ascenium.com) 的公司想要创造一种软件定义的 CPU。他们已经筹集了数百万美元将产品推向市场。

这些材料有点模糊，但是听起来好像这个想法是让 CPU 资源可用，让编译器管理和调度这些资源，而不使用完整的指令集。一个名为 Aptos 的系统让编译器编排这些资源。

如果你是精明的，你会看到这与 RISC 有一些相似之处，甚至与 VLIW 计算机体系结构更相似。关于更多细节，在 [TheNextPlatform](https://www.nextplatform.com/2021/07/12/gutting-decades-of-architecture-to-build-a-new-kind-of-processor/) 上有一个对该公司首席执行官的采访，对 CPU 将如何工作有一些见解。

除了 RISC 和 VLIW，[传输触发架构](https://hackaday.com/2016/11/30/one-bit-one-instruction-discrete-cpu/)也分享了这一理念，尽管只有少数商业版本。所以将工作推给编译器的想法并不新鲜。时间会证明 Ascenium 的方法是否真的不同和有益，或者至少，他们是否能对三四家大型 CPU 制造商产生更大的影响。

当然，如果你真的想重新配置你的 CPU，你可以用 FPGA 来完成。传输触发的架构有一个优势，因为你只有一条指令和可寻址单元。你甚至可以[微码](https://patents.google.com/patent/US9081582)那些更复杂的指令或仿真。