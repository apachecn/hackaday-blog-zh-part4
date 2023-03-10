# Ztachip 加速 Tensorflow 和图像工作负载

> 原文：<https://hackaday.com/2022/09/09/ztachip-accelerates-tensorflow-and-image-workloads/>

[Vuong Nguyen]显然知道他在人工智能加速器硬件方面的方法，创建了 [ztachip:一个用于人工智能和传统图像处理工作负载的加速器平台的开源实现](https://github.com/ztachip/ztachip)。Ztachip(读作“zeta-chip”)包含一系列定制处理器，并不局限于某个特定的架构。Ztachip 实现了[Vuong]创建的新张量编程范式，*可以*加速张量流任务，但不限于此。事实上，它可以与非人工智能任务并行处理 TensorFlow，如下面的视频所示。

基于 VexRiscV 设计的 RISC-V 内核用作处理应用程序分发的主机处理器。VexRiscV 本身就挺有意思的。用 spinal HDL(Scala 的一个变种)编写，它是超级可配置的，产生一个 Verilog 内核，随时可以投入到设计中。

![](img/ba7d34b08cbca1759b44f2a249c1af79.png)

A Digilent Arty-A7, Arducam and a VGA PMOD is all you need

从硬件设计的角度来看，RISC-V 内核连接到一个 AXI 交叉开关，所有 AXI 精简版总线都是混合的，这在 [AMBA AXI 生态系统](https://developer.arm.com/documentation/ihi0022/e/)中很常见。Ztachip 内核以及 DDR3 控制器也与摄像头接口和 VGA 视频连接在一起。

除了提供一个 FPGA 专用的 DDR3 控制器和 AXI 交叉开关 IP，其余的设计都是通用的 RTL。这是好消息。下面的演示部署到基于 Artix-7 的 [Digilent (Arty-A7)](https://digilent.com/shop/arty-a7-artix-7-fpga-development-board/) 上，带有 VGA PMOD 模块，但几乎不需要其他东西。提供预构建 Xilinx IP，但是针对不同的 FPGA 对于有经验的 FPGA 忍者来说应该不是一项巨大的任务。

![](img/c37f9f7f91305ec37671c144fbeecd4d.png)

Ztachip top level architecture

神奇的事情发生在 Ztachip 内核中，它主要是一个 p core 数组。每个 Pcore 都具有矢量和标量处理能力，因此非常灵活。张量引擎(内部称为“数据平面处理器”)负责将指令从 RISC-V 内核与图像数据一起发送到 Pcore 阵列，并输出视频数据。那个摄像头只有 0.3 MP Arducam，视频是 VGA 分辨率，但给它一个更大的 FPGA，这些限制可能会提高。

这种特定于领域的方法使用高度改进的类 C 语言(带有自定义编译器)来描述将跨加速器阵列分布的应用程序。我们找不到这方面的任何文档，但有一些示例算法。

演示视频展示了并行运行的四种算法的实时混合；一个物体分类(谷歌的 Tensorflow [mobilenet-ssd](https://www.tensorflow.org/lite/examples/object_detection/overview) ，一个预训练的人工智能模型) [canny 边缘检测](https://en.wikipedia.org/wiki/Canny_edge_detector)，一个 [Harris 角点检测](https://en.wikipedia.org/wiki/Harris_corner_detector)，以及光流，这给了它类似捕食者的运动视觉。

[Vuong]认为，在效率方面，它的计算效率比 Jetson Nano 高 5.5 倍，比谷歌的 TPU edge 高 37 倍。退一步说，这些都是大胆的主张，但我们有什么资格与一位显然才华横溢的工程师争论呢？

我们涵盖了许多与人工智能相关的话题，比如这个[人工智能辅助打字小工具](https://hackaday.com/2022/05/14/taptype-ai-assisted-hand-motion-tracking-using-only-accelerometers/)。不想忘记最初的人工智能硬件，[好的老式神经元](https://hackaday.com/2022/03/01/researchers-build-neural-networks-with-actual-neurons/)，我们也把它包括在内了！

 [https://www.youtube.com/embed/amubm828YGs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/amubm828YGs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

