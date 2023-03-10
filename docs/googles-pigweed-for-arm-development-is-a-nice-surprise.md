# 谷歌为 ARM 开发的 Pigweed 是一个不错的惊喜

> 原文：<https://hackaday.com/2020/03/21/googles-pigweed-for-arm-development-is-a-nice-surprise/>

为嵌入式开发设置环境传统上是一件痛苦的事情，因此供应商提供了集成开发环境来帮助弥补这一差距。谷歌已经开源了他们的嵌入式目标环境版本，称为嵌入式目标库，他们将其注册为 Pigweed。

二月份，谷歌[在美国专利商标局注册了猪草](https://uspto.report/TM/88781512/)的商标，它和一些细节一起出现在[谷歌开源博客](https://opensource.googleblog.com/2020/03/pigweed-collection-of-embedded-libraries.html)上。

这个存储库包含了谷歌所说的模块，但是仔细看看就会发现它还不止这些。Python 虚拟环境中打包了许多工具，包括 ARM 编译器、clang-format 工具和 Python 3.8 解释器，后者可以运行很多东西。Pigweed 附带的模块通过运行微自动化来帮助开发人员，例如 pw_watch 模块，它可以监控文件的更改并触发硬件上的构建、测试甚至刷新和调试。还有一个模块允许提交前检查，如林挺和格式。

Google 仍然不认为这个产品已经准备好生产了，尽管从我们目前看到的情况来看，它是许多人开始尝试嵌入式开发自动化需求的好地方。有人试过了吗？

如果你已经被自动化的惊人力量所鼓舞，并且想要深入自己，看看 BASH 中的[软件开发和 Python](https://hackaday.com/2018/02/27/software-development-in-bash/) 中的[持续集成。](https://hackaday.com/2020/01/06/continuous-integration-what-it-is-and-why-you-need-it/)