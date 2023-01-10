# 本周安全:脸书黑了你的电子邮件，电网上的网络，和一个讨厌的零日

> 原文：<https://hackaday.com/2019/05/01/this-week-in-security-facebook-hacked-your-email-cyber-on-the-power-grid-and-a-nasty-zero-day/>

啊脸书。只有你能把电子邮件验证搞得这么糟糕，还能让一百万人交出他们的电子邮件地址密码。是的，你没看错，脸书的电子邮件验证方案是要求用户提供他们的电子邮件地址和电子邮件帐户密码。在验证过程中，[脸书自动下载了账户的联系人列表](https://www.businessinsider.com/facebook-uploaded-1-5-million-users-email-contacts-without-permission-2019-4)，没有任何警告，也没有办法选择退出。

这里的可怕程度令人难以置信，但也许我们需要一个新的安全规则来应对这种情况。不要给一个在线服务不同服务的密码。为了在这种情况下使用密码，有必要以纯文本方式处理它。目前还不确定脸书储存了这些密码多长时间，但他们最近还透露，他们已经在内部以纯文本形式储存了数百万脸书和 Instagram 密码。

这也不是脸书第一次因为严重的隐私恶作剧被曝光:2018 年初，脸书安卓应用[在没有通知用户的情况下上传电话记录](https://arstechnica.com/information-technology/2018/03/facebook-scraped-call-text-message-data-for-years-from-android-phones/)。马克·扎克伯格最近[概述了他的计划](https://www.facebook.com/notes/mark-zuckerberg/a-privacy-focused-vision-for-social-networking/10156700570096634/)，让脸书重新关注隐私。时间会证明是否会发生真正的变化。

### 网络可以代表任何东西

你有没有注意到“网络”已经成为一个毫无意义的时髦词，尤其是当通常的嫌疑人使用它的时候？能源部发布了一份报告，其中包含一个模糊但有趣的事件描述:“导致电力系统运行中断的网络事件。”这件事被新闻媒体注意到了，从那以后人们就一直在猜测。令人沮丧的是“网络事件”一词所涵盖的广泛含义。这是真正的袭击吗？是崔妮蒂关闭了发电站，还是实习生被电线绊倒了？


### 开窗户的车

你开的是 2015 款现代途胜吗？好消息是，你可能有一个非常容易破解的信息娱乐中心。坏消息是，你有一个运行 Windows CE 的非常容易被黑客攻击的信息娱乐中心。[James]在 Twitter 上分享了他正在进行的一些研究，既有趣又令人担忧。jawdropping 的启示是，当插入闪存盘时，信息娱乐系统会自动执行“HyundaiUpdate.exe ”,无需任何验证。请记住，[的第一次高调的汽车开发](https://hackaday.com/2015/08/22/how-those-hacker-took-complete-control-of-that-jeep/)也是通过信息娱乐中心完成的。

### Java 反序列化零日

当云提供商受到勒索软件攻击时会发生什么？这是甲骨文 WebLogic Server 的一些用户在 CVE 2019-2725 的一个严重的 0 天漏洞浮出水面后做出的决定。归结起来就是 Java 如何进行反序列化，将平面数据解包回对象。虽然外部数据总是要被怀疑，但 Java 在反序列化方面有一个长期存在的问题，即在反序列化过程中，序列化的数据可能会覆盖范围内的其他变量。这里有一个明显的安全弱点，但是 Java 语言中的一个补丁会破坏无数已部署的应用程序。

简而言之，暴露 WebLogic 的服务器是易受攻击的，并且很可能已经受到勒索软件攻击。Oracle 已经发布了修复此特定问题的紧急补丁。

有关 Java 反序列化攻击的详细介绍，请查看下面的演示:

 [https://www.youtube.com/embed/VviY3O-euVQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/VviY3O-euVQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



### 正误表

上次我们讨论了影锤攻击，从那以后卡巴斯基实验室发布了他们的调查结果的技术报告。那里有一些更有趣的细节，所以去看看吧。

请记住，请将您的建议发送给我们，以便我们在本周的下一期《安全》杂志上看到。