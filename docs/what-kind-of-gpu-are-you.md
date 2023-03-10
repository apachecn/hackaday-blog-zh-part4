# 你是什么 GPU？

> 原文：<https://hackaday.com/2021/07/22/what-kind-of-gpu-are-you/>

在过去，大型计算机通常有某种形式的外部阵列处理器。这个想法是，你可以将一堆数字加载到处理器中，然后并行地对所有的数字进行一些数学运算。这些天来，你更有可能转向你的图形卡的数字处理支持。您通常会使用一些库来帮助您做到这一点，但是当您理解了幕后发生的事情时，事情总是会变得更好。这就是为什么我们喜欢[RasterGrid 的] [关于 GPU 架构类型](https://rastergrid.com/blog/gpu-tech/2021/07/gpu-architecture-types-explained/)的帖子。

如果你能区分 IMR(即时模式)和 TBR(基于图块)渲染，这可能不适合你。虽然我们知道这些术语，但我们发现了许多有趣的细节，包括一些阐明关键区别的图形和伪代码。

哪种架构比较好？正如帖子指出的，这取决于你如何定义更好。每个人都可以夸耀自己在某方面更好，但另一方面，每个人在其他方面也更差。一般来说，IMR GPUs 会出现在台式电脑上，而移动设备则倾向于 TBR。这也取决于你要求 GPU 完成的具体任务。

当然，你通常不需要知道这些。对于图形，你可能不会直接控制设备，对于计算，你可能会使用 [CUDA](https://hackaday.com/2018/03/19/cuda-is-like-owning-a-supercomputer/) 或 [OpenCL](https://hackaday.com/2019/01/24/running-opencl-on-a-raspberry-pi-gpu/) 。但是你不需要理解引擎来驾驶汽车，但是表现最好的司机确实知道引擎是如何工作的。