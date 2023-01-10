# 您自己的 IBM 大型机(或 Vax，或 Cray…)的简单方法

> 原文：<https://hackaday.com/2022/06/19/your-own-ibm-mainframe-or-vax-or-cray-the-easy-way/>

如果您想要使用 IBM 大型机或其他经典计算机(如 DEC VAX)的经典体验，您有几个选择。你可能会花很多钱去寻找、运输和翻新它。但是，当然，我们大多数人会满足于模拟器。虽然有很好的模拟器，但大多数时候你对运行裸机并不感兴趣——你需要操作系统、编译器和其他让这些机器如此有趣的软件。运行您的三行机器代码没有玩 hunt the wumpus 或编译一些 Fortran IV 代码有趣。不幸的是，找到所有这些旧软件的副本可能会令人望而生畏。但多亏了[Rattydave]的努力，你完全没问题就能做到。秘密？[预建的 docker 映像](https://hub.docker.com/r/rattydave/docker-ubuntu-hercules-mvs)将您需要的一切都放在一个地方。

除了 IBM 的 [MVS](https://hub.docker.com/r/rattydave/docker-ubuntu-hercules-mvs) 、 [VM370](https://hub.docker.com/r/rattydave/docker-ubuntu-hercules-vm370) 和 [TSS](https://hub.docker.com/r/rattydave/docker-ubuntu-hercules-tss) 之外，你还可以在一系列来自 [DEC、HP 和 DG](https://hub.docker.com/r/rattydave/alpine-simh/) 的计算机上运行[Multics](https://hub.docker.com/r/rattydave/alpine-multics)——Unix 的前身——甚至是一台 [Cray 1 超级计算机](https://hub.docker.com/r/rattydave/cray1/)。有很好的说明，虽然有些机器确实需要一点工作。例如，TSS 图像指出:

> 这不是一个随时可以运行的系统。您需要 IPL 250，然后您可以通过 telnet 连接进行控制。(如果你不知道 IPL 280 意味着什么，那么这个容器不适合你。)

我们不确定这两个数字是应该都是 250，还是都是 280，或者这句话本身是否有意义。我们已经很久没有使用 IBM 电脑了。我们认为他们都应该是 250。

收集了许多 SIM-H 机器，包括有和没有 Z80 CPU 的 Altair 8080，IBM 1130 和许多其他可能仍然需要一些关注才能工作的机器。

当然，你仍然需要知道如何操作有问题的计算机，尽管每个图像的注释至少会帮助你获得一个立足点。你可能也应该对 docker 略知一二，尽管只是为了使用它，它并不那么难。另外，如果你开始使用 docker，你会发现[有很多不同的用法。](https://hackaday.com/2016/09/01/how-to-use-docker-to-cross-compile-for-raspberry-pi-and-more/)