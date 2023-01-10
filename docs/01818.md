# 监听电源，第 2 部分

> 原文：<https://hackaday.com/2019/01/14/listening-to-mains-power-part-2/>

无论你住在世界的哪个地方，电网上的电现在将普遍以交流电的形式提供给你。也就是说每秒会在正负极性之间振荡多次。50 或 60Hz 的频率恰好在人类听觉的频率范围内。然而，电力线频谱中的基频远远不止这些，为了更好地听到这些额外的频率，你需要做一些信号处理。

当它还处于原型阶段时，我们第一次展示了这一构建，但从那时起，它已经完成并成功地用于发现当地电网中的一些异常情况。它从线路上获取输入，对其进行隔离，并通过声卡将其输入 MATLAB，在那里可以对其进行频率成分分析。它已经完成，包括一个案例，现在有瀑布图的“神秘”开关谐波与设备发现，加上随时间推移的波形变化图。下面还有一个视频，将这些谐波转换成音频，这样你就可以听到电流。

[由于我们在上一篇](https://hackaday.com/2018/08/23/listening-to-mains-power/)中介绍了它，【David】还从第一篇文章的评论中获得了一些反馈，改进了他的 PCB 上的隔离距离，并在制作最终版本之前进一步增强了 PCB。如果你曾经好奇你会在电线上发现什么，一定要看看项目页面上的更新。

 [https://www.youtube.com/embed/xahvkZKF86c?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/xahvkZKF86c?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

