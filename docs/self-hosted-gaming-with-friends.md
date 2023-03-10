# 与朋友一起玩自助游戏

> 原文：<https://hackaday.com/2022/12/26/self-hosted-gaming-with-friends/>

游戏最好的部分之一是和朋友一起玩游戏，但这通常需要每个人都有同样昂贵的硬件。不过，几乎每个人都有一台带浏览器的电脑，所以如果你想和没有和你一样游戏机的朋友玩在线游戏，他们现在只需打开一个网络浏览器就可以玩了，这要感谢这个名为 [Qwantify](https://qwantify.vercel.app/) 的项目。

不过，要实现这一点有几个要求。至少需要一个人有一台带 GPU 的电脑来运行托管游戏的 docker 容器，但一旦完成，任何有浏览器的人都可以连接到它并玩游戏。[整个项目也是开源的](https://github.com/wanjohiryan/qwantify)，由于它目前是一个非常年轻的项目，只支持 AMD 和英特尔 GPU，但它确实有一个相当直观的用户界面以及一些其他功能，如允许各种游戏外设和支持 Twitch 和 YouTube 的流媒体游戏。

在像《我的世界》这样的游戏中，能够托管自己的游戏服务器是很常见的，但是我们很高兴看到一些自我托管的东西将这个想法带到了一个新的水平。自从我们都在谈论云游戏以来，我们还没有见过如此雄心勃勃的东西，但至少这次游戏可以在我们自己的硬件上运行。