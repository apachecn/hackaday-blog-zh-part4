# P-51 驾驶舱在当地制造商的帮助下重新制造

> 原文：<https://hackaday.com/2020/01/22/p-51-cockpit-recreated-with-help-of-local-makerspace/>

令人惊讶的是，人们很容易误判进入黑客日提示热线的提示。在过滤掉无处不在的垃圾邮件后，快速浏览一下提示标题通常会形成一个快速的印象，结果证明这是完全错误的。最近的一个提示就属于这种情况，从主题行来看，它似乎是一个飞行模拟器驾驶舱。我脑海中的画面是一个模型驾驶舱，挂在飞行模拟器或其他现成的飞行游戏上，其中许多我们已经看过很多年了。

我对格兰特·霍布斯承担的项目大错特错了。他的驾驶舱模拟器比我想象的要多得多，在与他交换了几封电子邮件以获得所有细节后，我觉得我必须分享导致下面短片的一系列黑客攻击，以及他如何设法建立这个场景的故事，尽管之前没有使用常用工具的经验。

## 一本小说和一部电影

[https://player.vimeo.com/video/379072773](https://player.vimeo.com/video/379072773)

格兰特制作短片已经有一段时间了，主要是与历史小说作家约翰·德怀尔合作。格兰特的短裤被用作约翰的书的宣传片，很好地捕捉了约翰小说的时代和背景。这些电影大多不需要什么特殊的布景，而是依靠库存镜头和老式服装来实现它们的外观和感觉。约翰的最新小说将改变这一切。

这部名为 [*野马*](https://www.johnjdwyer.com/mustang) 的小说以二战中的一名优秀战斗机飞行员为中心。格兰特用短片来宣传这本书的想法受到了最近克里斯托弗·诺兰电影*敦刻尔克*的启发，这部电影展示了在一架喷火战斗机的驾驶舱中拍摄的复杂场景。格兰特想要一个类似的外观，并开始安排使用一个真正的 P-51 野马拍摄。这带来了直接的问题。首先，没有多少老式飞机留下来，那些仍然在飞行的飞机通常在驾驶舱里有过时的仪器，如全球定位系统。此外，格兰特希望这些仪器能够像飞机在空中一样做出反应，并让座舱盖投射到驾驶舱的阴影暗示出空中机动。当飞机被困在跑道上时，这种效果很难实现。

 [![Beautifully detailed switch plates...](img/57acaac62c906416a5ab991a9e2bd82c.png "Panel made with laser-cut plastic and original switches")](https://hackaday.com/2020/01/22/p-51-cockpit-recreated-with-help-of-local-makerspace/panel-made-with-laser-cut-plastic-and-original-switches/) Beautifully detailed switch plates… [![and pilot lights.](img/44c332f41a33a004f578ebc65de6dcbc.png "Instrument made with laser-cut plastic and original indicator lights")](https://hackaday.com/2020/01/22/p-51-cockpit-recreated-with-help-of-local-makerspace/instrument-made-with-laser-cut-plastic-and-original-indicator-lights/) and pilot lights.

这时格兰特意识到需要一个万向驾驶舱模拟器。它可以有一个精确的仪表板，可以放置在户外，利用自然光和真实背景而不是 CGI，可以俯仰，滚动和偏航来模拟飞行。这将是完美的，这将拯救这个项目。只有一个问题:他不知道如何建造它。

## 援助之手

格兰特明智地向他当地的黑客空间达拉斯创客空间寻求帮助。在那里，他不仅找到了自己缺少的工具，还找到了拥有必要技能并愿意分享这些技能的志趣相投的人。他们开始在驾驶舱仪表板上工作，最终包括实际飞行硬件和模拟仪器的组合。这些假仪器使用步进器和 Arduino 来驱动针头，针头由一个定制的 iPad 应用程序控制，该应用程序用于在拍摄过程中实时制作它们的动画。真正的仪器，如人造地平线和转向滑动指示器，由真空泵提供动力，并对模拟器在万向节上的运动做出反应。

[![](img/5ccfe70c2d3daa9ba5d11caf27499185.png)](https://hackaday.com/wp-content/uploads/2020/01/1-p51-mustang-cockpit-exterior.jpg)

The gimballed cockpit set for exterior shots. The wide horizon and natural lighting combined with the 3-DOF gimbal make for a very realistic effect.

将这个令人信服的面板安装到某物上是一个完全不同的任务。格兰特主要依靠 DMS 成员的经验来设计一个足够坚固的结构来支撑演员，并允许产生令人信服的效果所需的动作。驾驶舱模型由等离子切割金属板和胶合板制成，安装在重型三轴万向节上，包括一个来自托盘千斤顶的巨大轴承，用于偏航轴。

[![](img/2c09c2f420ce304ee8092ee3d57e83eb.png)](https://hackaday.com/wp-content/uploads/2020/01/4-p51-mustang-cockpit-manned.jpg)

Set and talent, ready for action.

格兰特最初计划将模型放在山顶进行拍摄，就像敦刻尔克的喷火模型放在悬崖边上，以提供一个无障碍的地平线来模拟飞越英吉利海峡。当证明这在后勤上具有挑战性时，他在机场跑道上搭建了一个平台，并使用巧妙的相机遮挡来避免拍摄地平线。Grips 手动移动模拟器，而 Grant 操纵假仪器并拍摄结果，我认为这是不言自明的。如果预算——以及现场安全——能够支持模拟巨大的四叶片野马推进器，这种幻觉就完全了。

我真的很喜欢钻研这个项目以及它所包含的所有技巧。电影魔术和其他东西一样都是关于黑客的，至少在镜头后面是这样，很高兴看到有限的预算能做些什么。我们最近推出了一部低预算但高风格的科幻电影，我们还与网飞系列电影【T4 迷失太空】的回放设计师[进行了深入探讨，既在这些页面中，也作为一次聊天](https://hackaday.com/2018/10/29/seth-molson-is-designing-the-future-one-show-at-a-time/)。