# 将 PS4 变成一台有用的 Linux 机器

> 原文：<https://hackaday.com/2022/02/10/turning-the-ps4-into-a-useful-linux-machine/>

当 PlayStation 3 首次推出时，其最受称赞的功能之一是它能够正式运行完整的 Linux 发行版。这当然是众所周知的，索尼在几年后通过软件更新永久破解了这一问题，大概是因为这款游戏机的定价太低，无法盈利，而且索尼不想间接资助由相对便宜的硬件制成的服务器群。当然，像这样让 Linux 远离计算机系统的决定只会鼓励 Linux 用户把它放在那些相同的系统上，同样的[这个项目在臭名昭著的操作系统](https://zhekunhu.xyz/ps4-kubernetes.html)的帮助下把一个更现代的 Playstation 4 变成了一个 Kubernetes 集群。

根据现代桌面标准，Playstation 4 的硬件有点过时，但作为一台通用电脑，它仍然很有能力，只要你知道在一台电脑上安装 [Psxitarch Linux](https://www.psx-place.com/threads/psxitarch-linux-released-by-psxita-team-adds-support-for-3d-graphics-bluetooth-wi-fi-more.17755/) 的非官方、不受支持的方法。这是一个基于 Arch 的发行版，是专门为 PS4 开发的，但是要让它运行[胡哲坤]想要使用的 docker 镜像，需要对内核做一些修改。在 Gentoo 社区的帮助下，最终编译了一个定制内核，在[Zhekun Hu]描述的“Linux 内核选项地狱”中花了一些时间之后，最终找到了一个工作配置。

当前的集群由两个运行这个定制软件的 ps4 组成，并运行许多服务，包括 Nginx、Calico、Prometheus 和 Grafana。对于那些闲置 PlayStation 4s 的人来说，这可能是让他们重新工作的一个选择，但它也应该是一个关于从头配置 Linux 内核的麻烦的警示故事。尽管如此，它仍然可以在几乎任何机器上完成，正如我们最近看到的使用 386 和软盘。