# 在你检查你的邮件之前毁坏你的邮件

> 原文：<https://hackaday.com/2021/06/05/wreck-your-mail-before-you-check-your-mail/>

每隔五年左右，我想是时候回顾一下我的电子邮件流程了。(哦不！)我运行我自己的邮件服务器，[你也应该运行](https://mailinabox.email/)，但这意味着我要自己解决管理、搜索、存档和索引这些问题。(耶！)

老实说，有时候我有点像勒德分子。实际上，我已经使用 Mutt 或者它的衍生产品 [NeoMutt](https://neomutt.org/) 大约 15 年了，在此之前，我已经使用了 10 年左右的鼠标密集型图形邮件阅读器。如果电子邮件是关于输入文字，或者偶尔附上图片，没有什么比一个简单的文本界面更好的了。但是这些简单的邮件客户端缺少的是良好的搜索。所以我决定认真对待这件事。

基本上是一个电子邮件数据库。它是一个电子邮件搜索器、标记器和索引器，但除此之外别无它用。好的一面是它的*快得惊人。搜索和提取标记子集比在大 G 上来回发送相同的数据更快，而且我有更多的灵活性。太牛逼了。当然，好的老杂种狗不需要太多就能工作。一切都可以。是 Linux/UNIX。*

[![](img/6f5be945f2af6b3ec5053171ca551299.png)](https://hackaday.com/wp-content/uploads/2021/06/astroid_logo.png) 但我想要一个认真对待标签而不是文件夹流的电子邮件客户端，让搜索成为一流的导航策略。Mutt 来自 90 年代，当时电子邮件还处于青少年时期。我最终选择了[星形线](https://astroidmail.github.io/)，目前正处于蜜月期，仍在进行配置，以便它们能够正常工作*但总的来说，我很享受这种改变。当然，有些键映射是不同的，所以如果你收到我的一封显然是发给别人的电子邮件，那么，你知道发生了什么。*

所以我在这里，当某些邮件到达时，自动标记脚本将 MQTT 消息发送到我的家庭自动化系统，标记系统区分重要性和紧迫性以及定义的主题。它不会监视我，跟踪我点击的链接，或者[未经我允许记录我的每一次网上购物](https://www.wired.com/story/google-tracks-you-privacy/)。它基本上非常适合我，我现在很开心。

而这一切。整整一个下午的乏味工作，尝试不同的软件包，调整配置脚本。总而言之，这是一个令人麻木的努力，我很乐意不重复，直到我们都直接用我们的神经植入物撰写电子邮件。但是有多少人对你的电子邮件设置感到满意呢？

This article is part of the Hackaday.com newsletter, delivered every seven days for each of the last 200+ weeks. It also includes our favorite articles from the last seven days that you can see on [the web version of the newsletter](https://mailchi.mp/hackaday.com/hackaday-newsletter-649368). Want this type of article to hit your inbox every Friday morning? [You should sign up](http://eepurl.com/gTMxQf)!