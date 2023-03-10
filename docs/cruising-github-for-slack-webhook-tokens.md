# 为 Slack Webhook 令牌巡航 GitHub

> 原文：<https://hackaday.com/2019/08/16/cruising-github-for-slack-webhook-tokens/>

GitHub 是一个非常强大的共享源代码的工具，它对现代黑客的价值是不言而喻的。但是毫不费力地分享你的资源至少有一个缺点:现在全世界都更容易发现你什么时候搞砸了。过去，如果你不小心把用户名或密码留在了你网站上的一个 tarball 中，你可以在别人发现之前把它删除。但是把这样的东西放到 GitHub 上，你就有麻烦了。

举个例子，看看这个工具[，它从 GitHub 中抓取由【Michele Gruppioni】](https://github.com/Gruppio/SlackWebhooksGithubCrawler)编写的 Slack webhooks。利用 Slack webhook 链接具有可预测的格式这一事实，该工具搜索存储库来查找错误地包含认证令牌的代码。有了令牌，攻击者现在就有能力向该通道发送未经请求的消息。

但是[Michele]克制住了自己，在用他的工具搜索 GitHub 后，他没有滚动他可以访问的 6500 多个空闲频道。相反，他给他们发送了一条友好的消息，解释他们的 webhook 令牌在 GitHub 上可用，并给了他们一个链接，他们可以在那里获得关于他的项目的更多信息。

[![](img/20eba77a69b0a95206a64161ec81ecbb.png)](https://hackaday.com/wp-content/uploads/2019/08/slackweb_detail.png)

事后联系他的大多数人都感激他发出了一个温和的警告，而不是令人讨厌的东西。尽管如此，我们还是建议希望以这种方式暴露漏洞的人要谨慎。虽然(米歇尔)有着高尚的意图，但尴尬的管理员责怪信使的情况肯定不是没有过。

如果使用得当，webhooks 可以非常方便地将数据推送到你选择的聊天平台。我们之前已经看过一个实际的例子[一个气象站将当前的状况推入一个不和谐的频道](https://hackaday.com/2018/02/15/creating-a-discord-webhook-in-python/)。只是尽量不要意外地将您的身份验证令牌提交给世界上最大的开源项目数据库，否则您可能会得到比您期望的更多的东西。