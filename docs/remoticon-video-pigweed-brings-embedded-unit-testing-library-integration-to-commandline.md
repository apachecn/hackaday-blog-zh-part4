# Remoticon 视频:Pigweed 将嵌入式单元测试、库集成引入命令行

> 原文：<https://hackaday.com/2021/01/13/remoticon-video-pigweed-brings-embedded-unit-testing-library-integration-to-commandline/>

说到嵌入式工程，工具链是最糟糕的。建立并正确运行新的工具链通常很困难，并且在升级 IDE 或其他软件时往往容易中断。对于不同的硬件，过多的不同工具链使得事情变得更加模糊，如果你想进入像自动化测试这样节省时间的技巧，你就在一个疯狂的旅程中。

这些痛点导致了 Pigweed 项目的创建。正如 Keir Mierle 在 2020 Hackaday Remoticon 的研讨会上所展示的那样， [Pigweed 是一组使嵌入式开发对黑客更加友好的库](https://www.youtube.com/watch?v=EyLXoWTB_c4)。该集合通过命令行访问，并与现有库协调工作，以提供单元测试、林挺、静态分析、日志记录和处理键值存储，以及更常见的任务，如编译和刷新。

在一个 Teensy 微控制器和一个 STM32 发现板上演示，该演示充分说明了 [Pigweed](https://pigweed.dev/) 的实用性，这是一个谷歌项目，早在 2020 年 3 月就以开源形式发布。用于这些平台的图形化 ide 还遥遥无期，但是测试固件可以相对容易地构建并闪存到这些设备上。单元测试，传统上是片上应用的一个棘手的主题，在计算机端仿真和在电路板上运行都得到了演示。随着微控制器的能力在最近几年迅速增长，为现有功能编写测试并在新的开发过程中对其进行确认已经成为你的必备技能。

这里展示了更多内容，因此[请访问研讨会知识库](https://pigweed.googlesource.com/pigweed/sample_project/+/refs/heads/master/workshop/)继续学习。它仍然被认为是实验性的，具有讽刺意味的是，我们不得不学习 Pigweed 工具链的复杂性来减轻其他工具链的痛苦。然而，大多数阅读的人会对使用统一工具和命令行自动化的能力有自己的亲和力；这是一种向低级硬件项目交付大量强大软件开发技术的迷人方式。

 [https://www.youtube.com/embed/EyLXoWTB_c4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/EyLXoWTB_c4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

