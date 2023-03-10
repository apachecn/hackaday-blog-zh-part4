# 定制游戏手柄可以自行重新编程

> 原文：<https://hackaday.com/2019/09/21/custom-game-pad-can-reprogram-itself/>

在最激烈的时刻，游戏玩家的生死取决于他们输入机制的速度和用户友好性。如果你是团队 PC，你有两个控制器要担心。很多时候，玩家会选择一个独立的游戏键盘，而不是通用的 104 键盘。

当[约翰·西尔维娅]心爱 Fang 游戏板去参加天上的着陆聚会时，他看到了一个机会，可以按照他的要求制造一个定制的替代品。此外，他找不到一个他想要的布局。机械开关是必须的，他选择了那些我们最近经常看到的类似樱桃 MX 的 Gaterons。

这款 37 键游戏手柄(John)为了向 Fang 致敬，将其命名为 Eyetooth，它有几个突出的特点。首先，由于内置的宏命令，任何键都可以直接从键盘上重新编程。这是键盘异常！

其中一个宏切换可选的自动重复功能。[John]说这不是用来作弊的，尽管你完全可以用它来作弊，如果你愿意的话。他在身体上无法足够快地发送密钥来满足一些单人游戏，所以他设计了这种方法作为变通办法。自动重复的频率可以使用向上/向下宏以 5 毫秒为增量进行调整。该项目的 GitHub 上有更多关于宏的信息。

Eyetooth 运行在 Arduino Pro Micro 上，所以你可以使用[John]的代码或者类似于[QMK 固件](https://docs.qmk.fm/#/)的东西。这个宝贝是如此开源，以至于[约翰]甚至有一个廉价获得高质量 grippy 脚的热门提示:去一元店寻找[橡胶鞋跟夹具](https://www.dollartree.com/assured-soft-rubber-heel-grippers-2ct-packs/228531)，旨在防止脚在鞋内滑动。

如果[John]发现自己做了大量的重新编程，[添加一个带有布局图的屏幕](https://hackaday.com/2018/05/26/a-custom-keypad-with-vision/)可以帮助他跟踪按键分配。