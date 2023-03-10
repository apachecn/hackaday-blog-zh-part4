# NVIDIA 宣布 59 美元的 Jetson Nano 2GB，这是一款针对制造商的单板计算机

> 原文：<https://hackaday.com/2020/10/05/nvidia-announces-59-jetson-nano-2gb-a-single-board-computer-with-makers-in-mind/>

NVIDIA 在 2014 年推出了 GPU 加速的单板计算机系列，这是一款售价 200 美元的开发系统，面向那些希望参与所谓“边缘计算”新兴世界的人。它旨在将高性能计算放在一个小而节能的包装中，可以直接集成到产品中，而不是连接到世界另一端的数据中心。

TK1 是一个令人印象深刻的硬件，但不是黑客和制造商社区必然感兴趣的东西。首先，它相当昂贵。但或许更重要的是，它显然更面向行业类型，而非消费者。我们确实看到了使用 TK1 和随后的 TX1 和 TX2 板的偶然项目，但它们很少。

然后是杰特森纳米。它的 128 核 Maxwell CPU 仍然拥有强大的功能，并完全兼容 NVIDIA 的 CUDA 架构，但其较小的尺寸和 99 美元的价格标签使其对爱好者更具吸引力。根据该公司自己的数据，自 2019 年 3 月 Nano 推出以来，活跃的 Jetson 开发者数量增加了两倍多。随着平台对更大和更多样化的用户群开放，新的和创新的机器学习应用程序开始涌入。

将入门级 Jetson 硬件的价格减半显然是朝着正确方向迈出的一步，但 NVIDIA 希望让更多的开发者加入竞争。那么为什么不看看闪电能不能打两次呢？今天，他们正式宣布新的 Jetson Nano 2GB 将于本月晚些时候上市，售价仅为 59 美元。让我们仔细看看 Nano 的新版本，看看与去年的型号相比有什么变化(和没有变化)。

## 修剪脂肪

 [![jetson2gb_top](img/c51ddd8883c3e1ac5653b1e559f9e3ec.png "jetson2gb_top")](https://hackaday.com/2020/10/05/nvidia-announces-59-jetson-nano-2gb-a-single-board-computer-with-makers-in-mind/jetson2gb_top/)  [![jetson2gb_bottom](img/917cd1222279a811cc548c753d5f9645.png "jetson2gb_bottom")](https://hackaday.com/2020/10/05/nvidia-announces-59-jetson-nano-2gb-a-single-board-computer-with-makers-in-mind/jetson2gb_bottom/) 

需要明确的是，新的 Jetson Nano 2GB 不是一款新设备，它本质上只是 2019 年发布的硬件的成本优化版本。它仍然是相同的大小，消耗相同的功率，拥有完全相同的 Maxwell GPU。从广义上讲，它是更昂贵的 Nano 的替代产品。事实上，它是如此的相似，以至于你可能一开始都分不清这两种型号的区别。尤其是因为最大的变化并不明显:顾名思义，新型号只有 2g 内存，而原来的 Nano 有 4g 内存。

[![](img/333a5be5b511fbafb2c24dc65b2b2c75.png)](https://hackaday.com/wp-content/uploads/2020/10/jetson2gb_ports.jpg)

然而，为了将价格降到原价的一半，该委员会已经失去了几个端口。Nano 2GB 取消了 HDMI 的显示端口(之前的版本有两个)，删除了第二个 CSI 摄像头连接器，取消了 M.2 插槽，并将 USB 端口的数量从四个减少到三个。对于大多数应用程序来说，失去一个 USB 端口可能不是一个大问题，但如果你需要高速数据，值得注意的是，其中只有一个是 3.0。总的来说，很明显，NVIDIA 仔细研究了人们连接到 Nano 的设备类型，并相应地调整了端口的类型和数量。

当然，侧面的 40 引脚接头保持不变，因此新板应该与您已经构建的任何器件保持引脚兼容。千兆以太网端口仍然存在，但不幸的是，这次无线仍然没有成功。因此，如果您的项目需要 WiFi，可以指望其中一个 USB 端口被一个加密狗永久占用。

它不仅变瘦了，还更新了。2GB 移除了老式的 DC 桶形插孔，代之以 USB-C 端口。在最初的 Nano 上，你可以通过 micro USB 端口运行它来完成大多数任务，但如果你打算推动硬件，建议使用笔记本电脑类型的电源。现在，您只需使用一个 15 瓦的 USB-C 电源，就可以在任何情况下使用。

## 紧紧的挤压

由于两个版本的 Nano 的硬件几乎相同，因此在其上运行任何新的基准测试都没有意义。如果你的软件能在 99 美元的 Nano 上运行，那么它在 59 美元的 Nano 上也能运行。或者至少，这是我的想法。实际上，只有一半的可用 RAM 对某些应用程序来说可能是个问题。

[![](img/69d5621f50eb70a757903f9f1989465d.png)](https://hackaday.com/wp-content/uploads/2020/10/jetson2gb_detectnet.jpg)

NVIDIA 发给我一个审查单元，因此作为一个简单的测试，我在罗技 C270 摄像机的直播视频上运行了构成 NVIDIA 人工智能培训课程一部分的`detectnet.py`脚本。虽然 Nano 保持了每秒 22 到 24 帧的速度，但系统几乎立即耗尽了 RAM，不得不使用交换空间来跟上速度。[自然，这在 SD 卡](https://hackaday.com/2019/04/08/give-your-raspberry-pi-sd-card-a-break-log-to-ram/)上很成问题，当然，除非你碰巧持有 SanDisk 股票，否则你不会想长期这么做。

[![](img/5209b8c12b53f9d148a7163d9a012128.png)](https://hackaday.com/wp-content/uploads/2020/10/jetson2gb_memory.png)

为了帮助解决这个问题，NVIDIA 建议禁用 Nano 2GB 上的 GUI，如果您计划执行任何计算密集型任务，请运行 headless。这应该可以为你节省 200 到 300 MB 的内存，但显然不是在所有情况下都有效。考虑到默认的 Ubuntu 18.04 系统映像直接启动到图形环境，这也有点违背直觉。看看将来是否会提供一些轻量级的操作系统来帮助解决这个问题，这将会很有趣。

## 机器的崛起

将 Jetson Nano 2GB 称为 Raspberry Pi 的直接竞争对手可能不太公平，但显然 NVIDIA 希望缩小差距。虽然缺乏内置 WiFi 和蓝牙可能会让许多制造商犹豫不决，但毫无疑问，如果你想尝试计算机视觉等东西，Nano 将会绕 Pi 4 跑一圈。99 美元对于精打细算的硬件黑客来说可能无关紧要，但现在 Nano 基本上与中端 Pi 4 的价格相同，这将是一个更难做出的决定。

[![](img/d46af8bc27ebfcde237994f23119f454.png)](https://hackaday.com/wp-content/uploads/2020/10/jetson2gb_robot.jpg) 特别是自从 NVIDIA 利用新主板的发布来帮助[启动 Jetson AI 认证计划](https://www.nvidia.com/jetson-ai-certification/)以来。这个免费的自定进度来源由教程和视频演练组成，涵盖了从基础训练到实际应用(如防撞和物体跟踪)的所有内容。为了完成 Jetson AI 专家课程并获得认证，申请人必须[向 NVIDIA 的社区项目论坛](https://developer.nvidia.com/embedded/community/jetson-projects)提交一个开源项目，以供审查和批准。

如果你想尝试一下人工智能和机器学习，花 99 美元买一台 Jetson Nano 是个不错的选择。现在有了一个 59 美元的版本，包括进入培训和认证程序，几乎没有选择余地了。最终，这正是 NVIDIA 想要的。