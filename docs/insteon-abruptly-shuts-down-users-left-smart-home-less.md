# Insteon 突然关闭，用户失去了智能家居

> 原文：<https://hackaday.com/2022/04/25/insteon-abruptly-shuts-down-users-left-smart-home-less/>

在今天这个“以前发生过并且肯定会再次发生的可预测的事情”中，智能家居公司 Insteon 吹嘘其围绕专有通信标准构建的设备生态系统，[在没有警告的情况下关闭了他们的服务器](https://arstechnica.com/gadgets/2022/04/shameful-insteon-looks-dead-just-like-its-users-smart-homes/)。近二十年来， [Insteon](https://en.wikipedia.org/wiki/Insteon) 过去一直提供智能灯开关、调光器、继电器、各种传感器、恒温器等产品，这些都是常见的家庭自动化产品，所有这些都连接到一个舒适的系统中。纵观 Insteon subreddit 的历史，[有迹象表明，该公司的衰落已经持续了大半年，但情况基本稳定——直到大约一周前，当用户醒来时，发现他们的智能家居网络的](https://www.reddit.com/r/insteon/comments/tvdeqt/soap_box_rant_insteon_should_just_pack_it_up/)[部分停止工作](https://www.reddit.com/r/insteon/comments/u3oj4o/my_hub_is_now_offline/)，移动应用程序不再响应，公司的资源和基础设施也停止了。此外，C 级管理层[已经删除了他们在 LinkedIn 上的简介](https://staceyoniot.com/insteon-is-down-and-may-not-be-coming-back/)，不再提及 Insteon 和 SmartLabs (Insteon 的母公司)。

瞬间，Insteon subreddit 活跃起来。人们理所当然地对被留在黑暗中感到愤怒，他们正在寻找答案——好像是在嘲笑他们，Insteon 的主页声称所有服务都在运行。其他人，已经预料到关闭最终会发生，开始[收集](https://www.reddit.com/r/insteon/comments/u5rrsb/owners_manuals_and_all_of_the_developer_docs/)和[重新托管](https://www.reddit.com/r/insteon/comments/u5j0n1/i_downloaded_all_the_quick_starts_and_owners/)迅速消失的文档，[互相帮助](https://www.reddit.com/r/insteon/comments/u78pwa/curious_about_efforts_to_keep_your_insteon_stuff/)在此期间保持他们的技术，以及[寻找替代平台](https://www.reddit.com/r/insteon/comments/u45pxs/insteon_and_home_assistant_ha/)。事实证明，用户不要在工厂重置他们的 Insteon hubs 是非常必要的，因为作为初始配置的一部分，他们必须与当前的 Insteon 服务器通信，努力[验证 SSL 证书](https://www.reddit.com/r/insteon/comments/u4an53/hub_2245222_online_reverse_engineering_efforts/)。可悲的是，相当多的用户，没有意识到并通过通常的解决方案使他们的网络再次运行，现在剩下的集线器基本上是砖砌的，除了少数幸运的人。

![screenshot of an eBay auction listing for an Insteon modem, going as high as $386](img/3851993a2c93b8ced7e2e1ebe3051ea1.png)

A modem capable of connecting an Insteon network to a Raspberry Pi – its original price being $80

服务停止一周后，Insteon [发布了一个更新](https://www.insteon.com/news2022)，这个更新[没有让任何人感到惊讶，也没有解决任何用户还不知道的问题](https://www.reddit.com/r/insteon/comments/u8cdg8/statement_by_insteon/)；将公司的财务崩溃归咎于疫情，甚至没有为受影响最大的人提供任何解决方案。生态系统的专有部分——代码、证书和文档——牢牢地卡在了清算的边缘，很明显，对于那些依赖 Insteon 来维持家庭运转的人来说，没有可预见的恢复正常的迹象。

用户一直在继续前进，智能家居平台，无论是开放的还是封闭的，都在欢迎这些新来的难民。HomeAssistant [做了一个介绍](https://www.reddit.com/r/insteon/comments/u7k6n4/hey_insteon_users/)让用户放松，并支持他们迁移到不同的平台。他们目前甚至有一名专门的开发人员致力于改善 Insteon 的文档和软件集成，用户已经[与他们的 HomeAssistant migration 分享成功故事](https://www.reddit.com/r/insteon/comments/u7k6n4/hey_insteon_users/)！其他平台，如 HOOBS、OpenHAB 和 HomeSeer，[也紧随其后](https://staceyoniot.com/with-insteon-down-possibly-for-good-what-options-do-you-have-for-your-devices/)。Raspberry Pi 的不足没有帮助，集成也不完美，但它们似乎比用户期望的要超前几英里，距离他们所坚持的破碎系统也有几光年的距离。当然，移动平台不是唯一需要解决的问题。为什么这样的事情不断发生？为什么我们一直回归到专利技术支持的智能家居模式？我们应该做些什么来改变这种情况，使其在未来不再发生？

时不时地，又有一个智能家居系统的基础设施被关闭，让用户束手无策，他们的硬件变得毫无用处。即使是大公司也不安全——我们已经看到了 2016 年[谷歌附属的 Revolv](https://hackaday.com/2016/04/07/alphabet-to-turn-off-revolvs-lights/) ，2020 年 [Charter](https://hackaday.com/2020/01/18/another-iot-debacle-charter-offers-home-insecurity/) (在美国称为 Spectrum)，以及 2021 年[三星的 SmartThings](https://hackaday.com/2021/07/19/samsung-shuttering-original-smartthings-hubs/) 。当百思买在短时间内关闭其智能家居产品时，我们进行了一次深入的对话，讨论为什么会发生这种情况，以及我们必须吸取的教训。毕竟，不仅仅是智能家居系统容易出现这种情况，甚至像[义眼](https://hackaday.com/2022/02/18/bionic-eyes-go-dark/)这样的设备也是如此。

我们感谢[Andrew]与我们分享这些！