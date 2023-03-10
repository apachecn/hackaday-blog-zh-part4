# 来自斯坦福的开放式个人助理

> 原文：<https://hackaday.com/2019/12/01/almond-open-personal-assistant-from-stanford/>

虚拟个人助理的现状——Alexa、Cortana、谷歌和 Siri——还有待改进。语音识别基本上相当不错。但是，定制选项非常有限。除此之外，许多人在使用这些助手时担心他们的数据隐私。斯坦福开放虚拟助理实验室已经推出了[杏仁](https://almond.stanford.edu/)，它是开放的，据报道有更好的隐私功能。

像大多数其他虚拟助手一样，杏仁拥有决定它能做什么的技能。您可以在浏览器、谷歌手机或命令行应用程序中使用 Almond。这一切都存在于 [GitHub](https://github.com/stanford-oval) 上，所以如果你不喜欢某样东西，你可以随意修改它。

这些技能存在于一个叫做 Thingpedia 的类似市场的东西上。虽然没有商业设备多，但数量惊人。该助手可以与 Nest、GNOME、Gmail、Twitter、Slack 和许多其他服务集成。

自然语言处理令人印象深刻。以下是网站上的一些例子:

*   当《纽约时报》有一篇关于中国的文章时，把标题翻译成中文，然后用电子邮件发给我的朋友。
*   当我离开家时，关掉暖气。
*   当我在推特上发帖时，把帖子复制给脸书。
*   得到比特币价格然后发给我 Slack 上的同事。

这个网站有点花哨，GitHub 需要一些时间来解析。然而，[文档](https://almond.stanford.edu/doc/getting-started.md)可读性很强。

阿尔蒙德正在乞求在智能音箱上运行，并且有一种方法可以做到这一点。您甚至可以使用已经配置好的 docker 映像来运行它。

我们真正想做的是把杏仁[做成机器人](https://hackaday.com/2019/08/11/diy-personal-assistant-robot-hears-and-sees-all/)。现在，我们可能只是重新利用一个[谷歌树莓 Pi](https://hackaday.com/2017/05/16/sudo-google-assistant/) 。

 [https://www.youtube.com/embed/IUtURMngJr8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/IUtURMngJr8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

