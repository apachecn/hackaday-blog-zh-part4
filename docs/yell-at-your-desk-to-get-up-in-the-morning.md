# 早上对着你的桌子大喊起来

> 原文：<https://hackaday.com/2019/02/05/yell-at-your-desk-to-get-up-in-the-morning/>

无论你喜不喜欢，立式办公桌都是办公室谈话的绝佳开场白。你怎么知道有人有立式办公桌？别担心，他们会告诉你的。立式办公桌有其优点，但为了获得最大的灵活性，许多人选择了一种可以根据需要升降的桌子。[Wassim]就有这样一张桌子，但发现按按钮对他的口味来说太 20 世纪了。自然，谷歌助手的整合是这里的关键。

[Wassim]开始打算捕获并欺骗桌面控制器给电机的信号，然后意识到简单地欺骗按钮按压可能更容易。这是通过几个 NPN 晶体管和一个 Onion Omega2+微控制器板实现的。然后是一个简单的例子，编写控制器来按下各种按钮，以响应通过 WiFi 接收到的 HTTP 请求。Google Assistant 的集成由 IFTTT 处理，尽管[Wassim]也讨论了实现完整智能家居 API 的可能性。

看着[Wassim]发出命令，桌子慢慢地响应起来，这很有趣。当然，还有其他方法，比如偷偷摸摸地用 PVC 来黑掉办公家具。

[Medium.com 的景色](https://medium.com/@wassimchegham/hey-google-set-my-desk-to-standing-mode-b21dcc40d4b5)