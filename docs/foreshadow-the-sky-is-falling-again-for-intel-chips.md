# 伏笔:英特尔芯片的天又要塌了

> 原文：<https://hackaday.com/2018/08/14/foreshadow-the-sky-is-falling-again-for-intel-chips/>

距离上次英特尔 CPU 的漏洞发布至少有一两个月了，但这次很严重。[伏笔](https://foreshadowattack.eu/)是最新的投机执行攻击，允许戴着巴拉克拉法帽的黑客窃取你的敏感信息。你知道这是一个真正的 0 日，因为它已经有了一个域名，一个标志，这一次，[有一个视频](https://www.youtube.com/watch?v=ynB1inl4G3c)用简单的术语解释任何人都可以理解为什么天要塌下来。该视频在音轨中使用了尤克里里琴，这意味着它制作得非常好。

预示攻击依赖于英特尔的软件保护扩展(SGX)指令，该指令允许用户代码分配私有内存区域。这些私有内存区域，或称*飞地*，是为虚拟机和 DRM 设计的。

## 伏笔如何工作

伏笔攻击利用投机执行，这是现代 CPU 的一个特征，最近出现在新闻中是因为 [Meltdown 和 Spectre 漏洞](https://hackaday.com/2018/01/05/lets-talk-intel-meltdown-and-spectre/)。伏笔攻击读取受 SGX 保护的内存内容，使得攻击者能够复制并读取私钥和其他个人信息。还有第二种伏笔攻击，称为伏笔-NG，它能够读取 CPU 的 L1 缓存中的任何内容(实际上是内存中的任何内容，只需一点点工作)，也可能用于读取运行在第三方云上的其他虚拟机中存储的信息。在最坏的情况下，在 AWS 或 Azure box 上运行你自己的代码可能会暴露出*在同一个 AWS 或 Azure box 上不是*你的数据。此外，对熔毁和幽灵攻击的对策可能不足以防止预兆

伏笔攻击背后的研究人员已经与英特尔进行了交谈，制造商已经确认伏笔会影响所有支持 SGX 的 Skylake 和 Kaby Lake 核心处理器。支持 SGX 的凌动处理器不受影响。对于预示的 NG 攻击，更多的处理器受到影响，包括第二代到第八代核心处理器，以及大多数 Xeons。这在当前部署的所有英特尔 CPU 中占了很大比例。[英特尔发布了一份安全公告](https://www.intel.com/content/www/us/en/security-center/advisory/intel-sa-00161.html)，详细列出了所有受影响的 CPU。