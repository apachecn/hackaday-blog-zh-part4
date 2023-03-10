# 电子邮件服务声称它不存储你的邮件

> 原文：<https://hackaday.com/2018/11/10/e-mail-service-claims-it-doesnt-store-your-mail/>

最近有很多关于公司滥用你的数据，包括你的电子邮件的新闻报道。此外，这些巨大的数据仓库是黑客最喜欢的目标。即使你信任大公司，你也在赌他们的安全。Criptext 声称他们拥有(可能是)有史以来最私密的电子邮件服务。它使用开放的[信号协议](https://en.wikipedia.org/wiki/Signal_Protocol)，只在你的设备上存储私人密钥和加密邮件。所有访问你邮件的应用程序都是开源的，所以可以推测，有人最终会发现任何后门或漏洞。

目前，这项服务是免费的，该公司报告称，即使付费服务准备就绪，仍将有一个免费层。当然，你也可以发送和接收普通的电子邮件。您也可以使用发送给其他人的密码短语(可能不是通过电子邮件)，这样他们就可以阅读加密的邮件。

但是，如果你想一想，至少有一个问题。如果他们不存储您的消息或密钥，那么您需要登录才能有人给您发送邮件！显然，如果你登录了但没有连接到互联网，Criptext 服务器会存储你的电子邮件，直到你回来，尽管这只是涉及到发件人使用你的公钥——他们仍然不能阅读服务器上的邮件。

不过，你可以有多个设备，所以这可能不是一个大问题。拥有多台设备也可以作为备份，因为它们没有你邮件的副本。事实上，这是他们常见问题中的一个条目:

> 问:我丢失了我的设备，我能找回我的电子邮件吗？是的，你可以用你的其他设备同步你的电子邮件。如果你丢了所有的设备，那你就惨了。

目前，您可以获得 Android、iOS、Linux 和 Mac 的客户端。Windows 版本即将推出。自然就没有网页版了。

还有其他的安全邮件服务，如 [Hushmail](https://www.hushmail.com/) 和 [Protonmail](https://protonmail.com/) 。然而，这些确实存储了你的一些数据。GMail 有一些加密的电子邮件扩展，尽管在谷歌最近的重新设计后，一些已经停止工作。 [FlowCrypt](https://chrome.google.com/webstore/detail/flowcrypt-encrypt-gmail-w/bnjglocicdkmhmoohhfkfkbbkejdhdgc) 是一个仍然有效的。

当然，有些人认为使用[可见加密](https://www.theregister.co.uk/2016/01/27/nsa_loves_it_when_you_use_pgp/)是一个危险信号，它本身就会引起注意。这时你[隐藏你的加密数据](https://hackaday.com/2018/11/07/shakespeare-in-a-zip-in-a-rar-hidden-in-an-image-on-twitter/)。虽然代码是开源的，但过去也有过[问题](https://hackaday.com/2018/05/14/pgp-vulnerability-pre-announced-by-security-researcher/)和审查良好的代码的后门最终被发现，但有时不会持续很长时间。