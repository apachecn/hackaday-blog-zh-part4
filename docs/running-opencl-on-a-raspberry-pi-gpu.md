# 在 Raspberry Pi GPU 上运行 OpenCL

> 原文：<https://hackaday.com/2019/01/24/running-opencl-on-a-raspberry-pi-gpu/>

对于媒体用户和机器学习黑客来说，这是一个有趣的发展:[doe300]已经在名为 VCFCL 的 Raspberry Pi 3 模型 B+上实现了[OpenCL](https://github.com/doe300/VC4CL)这是一个大新闻，因为 Pi 3+有一个内置在处理器中的图形处理单元(GPU)，而这个处理器通常没有得到充分利用。VideoCore IV GPU 内置于 Broadcom BCM2837B0 中，对于低功耗芯片来说，它具有惊人的能力。虽然[这种 GPU 有很好的文档记录](https://www.broadcom.com/blog/android-for-all-broadcom-gives-developers-keys-to-the-videocore)，但它还没有被广泛使用，因为你必须专门为此类 GPU 编写代码。增加对像 OpenCL 这样的高级框架的支持将使运行和修改现有的包变得更加容易。

这个 OpenCL 是 Daniel Steadelmann 在 [Nurenberg Tech](https://www.th-nuernberg.eu/) 主持的 masters these 的最终成果，这个实现支持 OpenCL 1.2 的嵌入式配置文件。这仅包括完整 OpenCL 命令的子集。尽管它支持可安装的客户端解码器(ICD ),这意味着您可以同时运行另一个 OpenCL 实现。如果你想使用像 [POCL](http://portablecl.org/) 这样的 CPU 实现同时在 GPU 和 CPU 上运行 OpenCL 任务，这是一个巧妙的技巧。

VideoCore IV GPU 的性能不会引起轰动:作者估计最高性能约为 24 GFLOPS。相比之下，Nvidia GTX1080 可以管理 8200 GFLOPs，你可以意识到在挖掘 Etherium 时你可能走不远。然而，如果实现的话，这足以使在 Raspberry Pi 上运行 Plex 和 Kodi 等程序更加现实，因为它足以支持视频流的实时代码转换。