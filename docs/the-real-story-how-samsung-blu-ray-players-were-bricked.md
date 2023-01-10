# 真实故事:三星蓝光播放器是如何被砌砖的

> 原文：<https://hackaday.com/2020/07/19/the-real-story-how-samsung-blu-ray-players-were-bricked/>

今年 6 月，许多三星蓝光播放器的用户发现他们的设备不再可用。陷入了启动循环，关于问题原因的猜测很普遍。现在看来，问题已经很清楚了——[一个格式错误的 XML 文件可能是问题的原因(通过注册表)。](https://www.theregister.com/2020/07/18/samsung_bluray_mass_dieoff_explained/)

问题源于存储用户数据并通过互联网将其传回三星的日志系统。记录和发送回哪些数据由 XML 文件管理，该文件包含控制这种行为的策略设置。据一位消息人士称，6 月 18 日发布在三星服务器上的 XML 文件中有一个畸形的列表元素。这导致播放器的主软件例程崩溃，导致播放器重新启动。

事实上，XML 文件在引导序列中很早就被解析，甚至在检查固件更新或新的 XML 文件之前，这加剧了失败。这使得三星无法通过无线方式推出更新或修复，也是为什么播放器会陷入不断重启的循环中。

据报道，[该文件可以在这个网址](https://configprd.samsungcloudsolution.net/openapi/dict/logpolicyconfig)找到，虽然现在是一个更新版本，不应该砖球员。三星不得不求助于邮寄修复方案，其中技术人员可以使用服务工具手动从播放器的存储中删除有问题的 XML 文件，允许它再次干净地启动。[虽然这表明我们最初的假设是错误的](https://hackaday.com/2020/06/26/ask-hackaday-what-can-be-done-with-your-bootlooping-blu-ray/)，我们很高兴看到问题的解决方案，尽管这需要很多麻烦。

【感谢 broeckelmaier 的提示！]