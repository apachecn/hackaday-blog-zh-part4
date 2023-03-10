# 本周安全:Twitter、Windows DNS、SAP RECON

> 原文：<https://hackaday.com/2020/07/17/this-week-in-security-twitter-windows-dns-sap-recon/>

Twitter 刚刚遭遇了多年来最大的安全漏洞。Mike 在周三警告过我们，但是有必要回顾一下其中的一些细节。故事仍在发展中，但似乎恶意行为者使用社会工程来访问内部 Twitter 仪表板。除了其他有趣的事情之外，这个仪表板还允许直接更改与帐户相关的电子邮件地址。一旦地址被更改为攻击者的，很容易进行密码重置并获得访问权限。

加密骗局中使用的比特币地址最终收到了价值近 12 万美元的比特币，所有这些都被转移到不同的账户中。这是一个古老而简单的骗局，但显然相当可信，因为这些消息是由经过验证的 Twitter 账户发布的。

![](img/018e570be1fabe13102a665f49fcb9aa.png)

Screenshot from [Motherboard](https://www.vice.com/en_us/article/jgxd3d/twitter-insider-access-panel-account-hacks-biden-uber-bezos)

已经发布了一系列截图，声称是攻击中使用的内部 Twitter 仪表板。由于那个仪表板，很多人都很惊讶。首先，Twitter 员工可以直接更改账户的电子邮件地址这一事实是自找麻烦。更有趣的是可以添加到帐户中的标签。“潮流黑名单”和“搜索黑名单”确实让人想起了封杀影子的传言，但在这一点上不可能知道细节。据 Motherboard 报道，Twitter 正在全面删除发布的截图，甚至暂停发布该截图的账户。当然，如果是假的，他们也会这么做，所以谁知道呢？

> 我们检测到我们认为是由一些人进行的协调社会工程攻击，他们成功地将我们的一些员工作为访问内部系统和工具的目标。
> 
> —推特支持(@推特支持)[2020 年 7 月 16 日](https://twitter.com/TwitterSupport/status/1283591846464233474?ref_src=twsrc%5Etfw)