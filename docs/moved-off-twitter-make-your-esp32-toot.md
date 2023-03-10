# 离开了推特？发出你的 ESP32 嘟嘟声

> 原文：<https://hackaday.com/2022/11/09/moved-off-twitter-make-your-esp32-toot/>

自从 Twitter 几天前被埃隆·马斯克正式接管以来，已经进行了大规模的裁员，一系列有问题的决定，以及社交媒体平台未来的不确定性。因此，有相当多的人，尤其是那些在技术和黑客领域的人，已经决定转移到分布式和开源的乳齿象服务(或至少用它们来连接他们的账户)就不足为奇了。

当然，黑客们会紧随其后，而且[Toby]分享了一个简单的基于 ESP32 的[乳齿象客户端库](https://github.com/ringtailsoftware/lyuba)供我们开始使用。乳齿象实例上的消息被称为“嘟嘟”，而不是“推特”，这与该平台的猛犸象吉祥物一致。这个名为 Luyba 的库能够发送嘟嘟声，并包含一个演示固件。使用 C++构建，支持平台。IO，它应该适合相当多的项目，让你轻松地将 toots 发送到你找到的任何地方，正如[图书馆辅助演示 toot 所示。](https://fosstodon.org/@lyuba/109309836413664053)

你能用你的 MCU 上的这样一个库做什么？事实证明，有相当多有趣的东西——一个[家庭自动化界面](https://hackaday.com/2009/07/19/home-automation-via-twitter/)、一个[生物陷阱](https://hackaday.com/2016/03/21/critter-twitter-trap-traps-critters-pings-twitter/)、一个在线 [BBC 基本解释器](https://hackaday.com/2020/03/07/tweet-your-bbc-basic-code-to-the-cloud/)，或者，如果有图像支持，一个摄像头[无论指向什么都可以发出鸣叫](https://hackaday.com/2019/06/28/be-on-twitter-without-being-on-twitter/)。黑客给了微博服务 API 访问权限和一些代码，这很有趣。也就是说，尽管 Twitter 多年来给我们带来了很多好处，但乳齿象可以很容易地做得更好，在[容易游戏化的“趋势”侧栏](https://hackaday.com/2022/02/05/gaming-twitters-trending-algorithm-to-make-a-point/)、自动裁剪算法中发现的[偏差](https://hackaday.com/2020/09/23/community-testing-suggests-bias-in-twitters-cropping-algorithm/)和[混乱的内部安全政策之间。](https://hackaday.com/2022/08/26/this-week-in-security-in-mudge-we-trust-dont-trust-that-app-browser-and-firefox-at-pwn2own/)