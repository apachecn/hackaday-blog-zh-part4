# 像 1999 年一样拨号上网

> 原文：<https://hackaday.com/2022/02/18/dial-into-the-internet-like-its-1999/>

修复任何种类的经典硬件都是一个很好的爱好，无论是修复老爷车、工具，甚至是古董苹果或 Commodore 电脑。了解旧设备有助于提高人们对更复杂的现代设备的理解，而且让旧设备重新运转起来也是一件非常有趣的事情。当然，我们在这里看到更多的复古计算修复，但有一点我们通常不会看到，那就是将那些旧计算机接入早期互联网的网络设备。[Retrocet]对那个领域很感兴趣，[他最新的拨号服务器真的让我们感觉回到了 90 年代](https://www.reddit.com/r/homelab/comments/stpbyn/the_dialup_home_lab_56k_edition/)。

这个家庭网络实验室是围绕钴 Qube 2 建立的，这是作为结婚礼物送给他后修复的。Qube 拥有一个尖端的 250 MHz 64 位处理器，内存高达 256 MB，并附带一个定制的 Linux 发行版作为操作系统。对这一建筑的最新升级加速了调制解调器以其全部 56k 速率工作，包括增加一个 DIVA T/A ISDN 终端和一些额外的硬件，以确保进入调制解调器的呼叫是数字的。保持数字连接而不是模拟连接可以防止调制解调器将速度降低到 33k 来处理转换。

[直到最近](https://www.reddit.com/r/homelab/comments/rn4px2/the_dialup_home_lab_featuring_the_cobalt_qube_2/)，【Retrocet】一直在一个定制的虚拟机上运行一些安装所需的软件，但是由于 Qube 的完全恢复和 Red Hat Linux 安装的一些调整，以提高旧系统的点对点协议能力，现在一切都在古董硬件上运行。如果你像[Retrocet]一样，有一堆这种旧硬件，那么[仍然有一些 ISP 可以为你提供一些服务](https://hackaday.com/2020/05/30/build-your-own-dial-up-isp-now-with-modem-pool/)。