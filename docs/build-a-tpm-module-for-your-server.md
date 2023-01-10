# 为您的服务器构建 TPM 模块

> 原文：<https://hackaday.com/2022/04/06/build-a-tpm-module-for-your-server/>

围绕 Windows 11 发布的一个大故事是，它需要支持 TPM 2.0 或可信平台模块才能运行。这采用了板载加密处理器的形式，微软声称这将有助于抵御恶意软件，但对雷德蒙来说可能更重要的是，它可以用来实施 DRM。标准的一部分涉及到硬件模块，[【赞】已经为 ASrock 服务器主板](https://zanechua.com/blog/diy-tpm-module)构建了几个这样的模块。

有问题的芯片是[英飞凌 SLB9965](https://www.infineon.com/cms/en/product/security-smart-card-solutions/optiga-embedded-security-solutions/optiga-tpm/slb-9665tt2.0/) ，经过一点研究发现，它或多或少直接映射到主板上 TPM 插座的引脚。这里有趣的事情在于它对 TPMs 的背景研究，此外还有与该主题相关的其他资源的链接。大多数需要 TPM 的读者可能会简单地购买一个，但是当涉及到这些事情时，所有的知识都是有用的。

我们的每周安全综述一直在关注 TPMs 的使用，甚至向我们展示了人们用来绕过模块的一些方法。