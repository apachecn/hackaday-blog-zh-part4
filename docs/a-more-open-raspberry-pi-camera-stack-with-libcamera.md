# 一个更开放的带有 Libcamera 的 Raspberry Pi 相机堆栈

> 原文：<https://hackaday.com/2020/05/11/a-more-open-raspberry-pi-camera-stack-with-libcamera/>

尽管 Raspberry Pi 基金会对他们心爱的产品一直很开放，但他们会第一个承认总有更多的工作要做:启动和运行一个 Pi 仍然需要许多封闭的专有组件。但是该基金会正在一点一点地工作，最新的一步是发布基于 libcamera 的相机堆栈[。](https://www.raspberrypi.org/blog/an-open-source-camera-stack-for-raspberry-pi-using-libcamera/)

大多数 Linux 应用程序通过 V4L2 或类似的 API 与相机交互。这些已建立的接口是在相机控制受限时设计的，由一些简单的硬件设置组成。今天，我们有更复杂的数字摄影和视频计算技术。算法已经超越了专用硬件，转变为利用 CPU 和/或 GPU 处理的软件模块。实际上，这种趋势意味着越来越多不透明的专有代码。每一个都是“秘方”算法的混合体，混合着普通的开销代码，浪费地为每个新的 blob 复制。

我们预计相机制造商在寻求竞争优势时，将继续设计专有的专业产品。幸运的是，他们中的一些人看到了开源框架的好处，它有助于将这些巨石分解成更易于管理的部分，让他们专注于自己的专业部分。利用类似于 [libcamera](https://libcamera.org/) 的东西可以减少他们的软件开发工作量，导致更快的上市时间，更低的支持成本，以及激励企业采用的相关收益。

但是就像每一个基于宏伟愿景的新界面设计一样，有一个先有鸡还是先有蛋的问题。如果没有硬件，应用程序开发人员不会使用它，如果没有应用程序使用它，硬件制造商也不会实现它。对于消费者而言，libcamera 拥有与 V4L2 和其他流行接口互操作的模块。对于硬件方面，如果有一家业务范围广泛的公司，认为开放他们能开放的东西、隔离他们不能开放的部分是有益的，那将是有益的。这就是树莓派基金会找到契合点的地方。

最初的版本不支持他们新的[高质量相机模块](https://hackaday.com/2020/05/01/new-part-day-raspberry-pi-camera-gets-serious-with-12-megapixels-proper-lenses/)，尽管这是很快承诺的。在短期内，仍然有许多工作要做，但我们对长期的可能性感到兴奋。如果 libcamera 确实可以降低准入门槛，它将鼓励创新，并扩大官方支持列表之外的相机系列。我们这里当然不缺乏与众不同的相机传感器创意，从[的 1 千像素相机传感器](https://hackaday.com/2019/12/30/image-sensor-from-discrete-parts-delivers-glorious-1-kilopixel-images/)到[的去封装 DRAM 芯片](https://hackaday.com/2014/04/05/taking-pictures-with-a-dram-chip/)。

[via [Hackster.io](https://www.hackster.io/news/raspberry-pi-foundation-announces-libcamera-based-open-source-camera-stack-eb41f911c9f7)