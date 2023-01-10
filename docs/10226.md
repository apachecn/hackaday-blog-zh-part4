# IRC 永远不会消亡

> 原文：<https://hackaday.com/2021/05/22/irc-will-never-die/>

本周开源世界的大混乱围绕着最大的 IRC 服务器运营商 Freenode T1。无论何处尘埃落定，无数重要的开源项目都使用 Freenode 的 IRC 服务器作为用户反馈的主要渠道，许多活跃的社区称之为 Freenode home。例如，你会称之为 3D 打印机的东西，以及驱动它的大多数软件，都是在 Freenode 的#reprap 中头脑风暴出来的。如果你想得到 Linux 发行版的帮助，几分钟之内你就可以直接进入相关的渠道，因为编写、打包或维护它的人可能正在 Freenode 上等着聊天。

但是，假设 Freenode 明天被烧毁，就像一些人建议的那样。那又怎样？我的看法是这无关紧要。Freenode 不拥有 IRC，建立一个 IRC 服务器本质上是微不足道的，真正重要的是在线社区——他们可以毫不费力地拿起并移动到其他地方。

[![](img/5d7e17bf54abbb24fbcd3bbb878eb2d9.png)](https://hackaday.com/wp-content/uploads/2021/05/freenode-troubles-thumb2.jpg)

这并不是说我们没有从 Freenode 的志愿者管理员和操作员多年来为这项事业所做的贡献中受益。IRC 服务器不会自己运行，几年前，Freenode 的管理员与垃圾邮件发送者进行了一场史诗般的战斗，并取得了胜利。保持 IRC 的大规模运行和为你的朋友建立一些东西是不同的事情，所以 Freenode 的人们绝对值得我们感谢。

但是看， [IRC 是一个古老的协议](https://en.wikipedia.org/wiki/Internet_Relay_Chat)，而[是一个简单的协议](https://en.wikipedia.org/wiki/List_of_Internet_Relay_Chat_commands)。事实上，编写一个 IRC 机器人非常简单，只需要用 Python 写几十行代码，使用*而不是*外部库。你需要做的就是通过套接字发送纯文本。你可以做到这一点——这是一个很好的人际关系网。

IRC 对黑客来说很有趣，但是如果你想要一个用户友好的 GUI 客户端，你有很多选择。如果你只是想尝试一下，甚至还有免安装的网络客户端。见鬼，你可以[在一个小时左右安装你自己的服务器](https://www.unrealircd.org/)。

因此，说 Freenode 的消亡是 IRC 的终结就像说 Hotmail 的终结是电子邮件的终结一样。总的来说，几乎没有人真正使用 IRC——Freenode 有 78000 名用户，而 Slack 有 1000 万——IRC 用户非常精明，如果不是十足的极客的话。这些人可能会在菜单中找到服务器字段，并将其从`irc.freenode.net`更改为`irc.whatever.org.`

除了我们在`irc.freenode.net`上的传统#hackaday 频道，还有一个在`irc.libera.chat`上设立的频道。两者都没有太多的行动——IRC 往往是一个缓慢的对话，所以如果有人在一个小时后回复你，不要惊慌——但如果你想顺便访问，我们会在那里。IRC 永远不会死！

## 2021 Hackaday 大奖开始啦！

如果您错过了我们的公告，[今年的黑客日大奖将在](https://hackaday.com/2021/05/18/2021-hackaday-prize-rethink-refresh-and-rebuild/)揭晓！我们都经历了艰难的一年半，这让我们很多人开始认真思考我们的世界。你希望今后如何改变它？50 名参赛者将重新思考，刷新和重建他们的方式进入 500 美元，大奖是 25，000 美元。去黑吧！

This article is part of the Hackaday.com newsletter, delivered every seven days for each of the last 200+ weeks. It also includes our favorite articles from the last seven days that you can see on [the web version of the newsletter](https://mailchi.mp/hackaday.com/hackaday-newsletter-649368). Want this type of article to hit your inbox every Friday morning? [You should sign up](http://eepurl.com/gTMxQf)!