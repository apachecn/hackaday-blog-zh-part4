# 点击这个红色的大按钮，立即进行社交媒体排毒

> 原文：<https://hackaday.com/2022/09/30/slap-this-big-red-button-for-an-instant-social-media-detox/>

危险的机器，比如那些能迅速把你变成一团红雾或冒烟的煤渣的机器，往往有一个大的红色按钮，无论威胁是什么，都可以立即停止。好吧，如果有比社交媒体更危险的机器被发明出来，我们不确定它会是什么，这就是为什么我们很高兴这个社交媒体死亡开关的存在。

[Gunter Froman]的发明背后的想法是为社交排毒提供一个物理接口，这是一种阻止或抑制某些应用程序和网站连接的服务。SocialDetox 阻止使用 HTTPS 域名系统(DoH)访问，或者针对特别讨厌和容易上瘾的应用程序，使用特定服务的 VPN 访问。这项服务确实需要订阅，其费用因你想要保护的设备数量而异，但老实说，收费似乎相当合理。

虽然 SocialsDetox 可以设置为定期阻止访问，比如说，如果你想让家庭晚餐成为一个无社交时间，那么可能会有需要立即取消社交访问的情况。这就是红色大按钮的由来，它连接到一个 Wemos D1 迷你。按下 kill 开关会向[发送一个 API 请求](https://apidocs.socialsdetox.com/)来启用或禁用该服务，让你从仇恨和嫉妒的漩涡中解脱出来，我们似乎都离不开这种漩涡。当然，除了 hack aday——这里完全不是这样的。

具有讽刺意味的是，使用物联网设备来限制对社交媒体的访问对我们来说并不陌生，但你可以使用你所拥有的工具。除此之外，我们喜欢这里的物理接口，这让我们想起了[这个适合洞](https://hackaday.com/2021/06/15/spam-caught-in-a-tin-of-spam/)的外壳。