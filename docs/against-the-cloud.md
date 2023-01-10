# 逆着云

> 原文：<https://hackaday.com/2022/02/19/against-the-cloud/>

我们的一个作者正在写一篇关于在你自己的熨斗上托管你自己的(项目)网站的文章，而不是用现代的、云服务的方式。这已经在 Hackaday 总部引起了不小的骚动。2022 年谁会运行自己的服务器，为什么？

反对 DIY 的理由都很充分。如果你只是想建立一个静态网站，你可以在无数不同的地方免费完成。GitHub 的[页面](https://pages.github.com/)超级方便，你的内容是版本控制的附带好处。如果你想要一个物联网类型的数据记录和展示服务，也有很多这样的服务——我没有最喜欢的。如果你想要电子邮件，那么，我不必告诉你，美国一家大型搜索垄断公司提供免费账户，以低价吸收你的所有行为数据。无论你需要什么，很有可能在云的某个地方有适合你的服务。

[![](img/e44ecc93454e27238162a12cd73c92bf.png)](https://hackaday.com/5810163712_c0ee6a99a2_k_thumbnail/)

如果你只想得到提供的服务，那就太棒了。但是如果你想玩呢？或者学习引擎盖下的工作原理？这是黑客日！

例如，你可以为你的朋友和家人运行你自己的邮件服务器。前面提到的搜索垄断者可能会把你所有的电子邮件都标记为垃圾邮件，部分原因是他们不信任小的电子邮件提供商，部分原因是这是垄断中的“m”。但是如果你能让人们把这些地址列入白名单，你就成功了。然后你打开了一个充满乐趣和愚蠢的世界。你可以编写钩子来自动处理邮件，或者你可以创建无限数量的邮件帐户，甚至可以根据过去 30 年来最棒的反垃圾邮件工具 [Spamgourmet](https://www.spamgourmet.com/index.pl?printpage=faq.html) 动态创建。或者你可以自己发明。为你的亲戚建立一个邮件列表。或者做些傻事。

我曾经运营过一项服务，当一个特定的账户收到一封电子邮件时，附加的照片会被推送到一个网站上，标题是主题行。最奇怪、最不安全的即时照片博客。让它运行起来是几行 Bash 脚本，以及一下午的乐趣。云中是否已经存在这样的服务？大概吧。一个允许你有一点隐私，不跟踪你的一举一动？也许吧。但即使有，我能通过使用这项服务了解到`sendmail`吗？没有。

我听到你小声说“安全”，你是对的。这个系统是由最纯粹的黑暗制成的锁来保护的。但是，在运行这项服务的七年中，没有人猜到这个神奇的电子邮件地址，一次也没有。电子邮件地址的知识本质上是一个密码，但是如果我需要额外的安全性，我可能已经在 Bash 的几行代码中实现了它。网页本身是静态 HTML，所以祝你好运，[黑客](https://www.youtube.com/watch?v=KEkrWRHCDQU)！(该网站已经关闭了一段时间，所以你错过了机会。)

如果你只是想要服务，你可以被服务。但是如果你想成为一个服务器，一个一流的互联网公民，在天空拥有自己的云，也没有什么能阻止你。与使用别人的电脑不同，运行自己的电脑是一种邀请。这是一个巨大的，联网的沙盒。有无数有趣的想法，你可以在自己的盒子上实现，还有很多东西要学。如果你黑了别人的盒子，那就是犯罪。如果你自己黑，那是一种享受。

我知道这不合时宜，但试一试吧。(PDF，淫秽，错别字未改。)做自己的云。

This article is part of the Hackaday.com newsletter, delivered every seven days for each of the last 200+ weeks. It also includes our favorite articles from the last seven days that you can see on [the web version of the newsletter](https://mailchi.mp/hackaday.com/hackaday-newsletter-649368). Want this type of article to hit your inbox every Friday morning? [You should sign up](http://eepurl.com/gTMxQf)!