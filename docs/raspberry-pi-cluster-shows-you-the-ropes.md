# 树莓 Pi 集群向您展示诀窍

> 原文：<https://hackaday.com/2020/04/24/raspberry-pi-cluster-shows-you-the-ropes/>

Raspberry Pi 集群是一个非常常见的项目，但是我们看到的很多构建都集中在集群的硬件方面。一旦它开始运行，接下来会发生什么呢？Raspberry Pis 不是非常强大的设备，但对于学习如何与计算机集群交互或进行实验测试设置来说，它们仍然是一个很好的项目。在来自[Dino]的这个项目中，[四个 pi 联网在一起，然后加载一组用于集群计算的基本软件](https://www.dinofizzotti.com/blog/2020-04-10-raspberry-pi-cluster-part-1-provisioning-with-ansible-and-temperature-monitoring-using-prometheus-and-grafana/)。

在安装硬件和操作系统之后，首先要设置的是网络配置。为了正常通信，每个 Pi 都需要一个静态 IP。在这种情况下，[Dino]大量使用了 SSH。从那里，他开始安装 Prometheus 和 Grafana，用作监控软件，可以跟踪系统资源和工作温度。之后，最后一步是安装 Ansible，这是一个专门针对集群的监控软件，它允许所有计算机作为一个单元而不是作为四个独立的设备进行管理。

这只是[Dino]深入集群计算的第 1 部分，我们希望有更多的内容。计算机集群有很多事情要做，一旦你学会了像这样的 Raspberry Pi 设置的诀窍，那么转移到一个更强大(也更昂贵)的设置会容易得多，它可以完成一些重要的工作。