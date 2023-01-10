# 通过即时消息路由 IP 是可能的，但不切实际

> 原文：<https://hackaday.com/2019/05/28/routing-ip-over-instant-messages-is-possible-yet-impractical/>

Telegram 是一款即时通讯应用，因其专注于安全和加密而闻名。它被政府官员、记者和偏执狂使用，除了短信功能外，还可以处理 VoIP 电话。[PiMaker]想知道所有这些加密技术能否得到很好的利用，[并决定尝试通过电报路由 IP，就像你做的那样](https://github.com/PiMaker/Teletun)。

这个项目被称为 Teletun，它很有效！它使用 [telgram-cli](https://github.com/vysheng/tg) ，这是一个即时消息网络的命令行界面。实际的 IP 路由是用 Python 脚本处理的，[皮梅克]建议在使用中，用户应该“p *射线到神的怜悯”。*据报道，带宽有限，但延迟可低至 100 毫秒，这表明 Telegram 确实是一个相当即时的信使。

对于任何有抱负的黑客来说，在即时消息服务上建立隧道都是很好的实践，但对于任何实际用途来说，这可能都不实用。如果你能想到一个，除了激怒情报人员窃听你的通讯，把它写在下面的评论里。否则，考虑其他古怪的方式来使用电报。