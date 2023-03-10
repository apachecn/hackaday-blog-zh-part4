# 拆开你的 ISP 的路由器

> 原文：<https://hackaday.com/2020/04/02/peel-apart-your-isps-router/>

无论您的家庭互联网连接是通过 ADSL、光纤、电缆，甚至是卫星，在您的 ISP 和您的计算机之间的某个环节上，您的家中将会有一个路由器。对我们中的一些人来说，这是一个我们自己买的模型，并加载了一个定制的发行版，但对大多数人来说，这是一个由我们的 ISP 提供的盒子，受他们的设置和限制。[Paddlesteamer]就有这样一个路由器，一个由 Turkcell ISP 提供的华为型号，[决定对它的设置](https://0x90.psaux.io/2020/03/01/Taking-Back-What-Is-Already-Yours-Router-Wars-Episode-I/)做一点窥探。

在一个由三部分组成的故事中，我们看到了这款设备的分解，从揭开外壳到逆向工程其更新过程，再到钻研其固件，最后完全取消其所有限制。这是一个令人着迷的过程，我们在其中学到了很多东西，比如中间人攻击是如何在路由器与 ISP 的连接上进行的，或者它包含一个授权的 SSH 密钥，似乎给了华为一个后门。你可能永远也不会用你的 ISP 路由器来做这件事，但是在你没有意识到的情况下，知道他们会把什么东西放在你家里是值得的。

路由器黑客的黄金时代可能已经过去，因为树莓 Pi 之类的已经取代了多余的路由器，成为廉价 Linux 主板的来源，但正如这向我们表明的那样，仍然需要不时地潜入路由器内部。毕竟，[锁定路由器已经不是什么新现象了](https://hackaday.com/2011/06/09/hacking-into-your-routers-administrative-interface/)。

Via [黑客新闻](https://news.ycombinator.com/item?id=22683422)。