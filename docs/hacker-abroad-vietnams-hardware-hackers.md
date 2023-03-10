# 海外黑客:越南的硬件黑客

> 原文：<https://hackaday.com/2019/03/27/hacker-abroad-vietnams-hardware-hackers/>

关于 Hackaday 的全球帝国，一个不幸的事情是，你经常不能亲自见到你的同事。因为我在中国，而且就在隔壁，我真的很想去越南见见肖恩·博伊斯，他已经为 Hackaday 写了几年了，但我们从未见过面。我建议，如果我们组织一次聚会或不聚会，我们就可以实现这个目标。肖恩很快就相信胡志明市的硬件黑客会大规模出动，他是对的！周日晚上，我们第一次 Hackaday 越南聚会，座无虚席。

非常感谢 [Fablab Saigon](https://fablabsaigon.org/) ，他立即支持这个活动的想法，并立即将这个消息传播出去。肖恩安排好了演讲者，并预定了一个绝佳的地点:一家咖啡店的三楼，那里有美味的饮料和甜点，但更重要的是有一个很棒的展示空间。

 [![Demonstrating the WS2812 strip added to a backpack.](img/d8d4483f26de4ab72c2ee5a32fb86d67.png "02-vietnam-meetup-blinky-backpack")](https://hackaday.com/2019/03/27/hacker-abroad-vietnams-hardware-hackers/02-vietnam-meetup-blinky-backpack/) Demonstrating the WS2812 strip added to a backpack. [![Everyone crowded around to see the textile work to make the slit for the lights](img/522f63f849245dec06987a6db0b4cbaa.png "03-vietnam-meetup-more-blinky-backpack")](https://hackaday.com/2019/03/27/hacker-abroad-vietnams-hardware-hackers/03-vietnam-meetup-more-blinky-backpack/) Everyone crowded around to see the textile work to make the slit for the lights

我以谈论我一直在玩的一些模拟电路开始了这个晚上，但这个晚上最引人注目的项目是这个 LED 增强型背包，它是由[mạnh·昆](https://hackaday.io/mqcrexcel)制造的。在袋子的小口袋里有一个垂直开口，隐藏了 10 英寸长的 WS2812 LED 灯条。由于 STM32 开发板，它闪烁着图案，这是那些“蓝色药丸”枫树迷你克隆之一。有趣的是，每个人都认为这个包是用一个狭缝设计的，但事实证明，Mạnh 自己添加了这个狭缝，并使它看起来像是设计的一部分。

 [![Original wood print uses 5 basic colors and has seashells in the paper for better brigthness](img/7ff7b81934b74cbb9830912439c7240f.png "04-vietnam-meetup-wooden-printing")](https://hackaday.com/2019/03/27/hacker-abroad-vietnams-hardware-hackers/04-vietnam-meetup-wooden-printing/) Original wood print uses 5 basic colors and has seashells in the paper for better brigthness [![Heavy block used for printing. Making your own with CNC is much lighter and easier process](img/6534f9360482932cb9ddeee4d43369d2.png "05-vietnam-meetup-Mai Nguyen-wooden-prints")](https://hackaday.com/2019/03/27/hacker-abroad-vietnams-hardware-hackers/05-vietnam-meetup-mai-nguyen-wooden-prints/) Heavy block used for printing. Making your own with CNC is much lighter and easier process [![Block printing kits for kids](img/b229cb9decea43701476d1c99991ddbc.png "17-vietnam-meetup-block-printing")](https://hackaday.com/2019/03/27/hacker-abroad-vietnams-hardware-hackers/17-vietnam-meetup-block-printing/) Block printing kits for kids

接下来， [Mai Nguyen](https://www.curiousmeye.com/) 介绍了她的雕版印刷。她是在受到雕版印刷令人惊叹的艺术作品的启发后开始这个项目的，当时雕版印刷是用于艺术的尖端技术——这就是这里的照片……我盯着她的版画看了太久，忘了给它们拍照。她有一道工序是[用数控机床铣出块](https://ingovietnam.weebly.com/)，其余工序沿用原工艺。

 [![16-vietnam-meetup-sean-boyce-talk](img/9152fbae3a8dbbc7df2424036518ca6a.png "16-vietnam-meetup-sean-boyce-talk")](https://hackaday.com/2019/03/27/hacker-abroad-vietnams-hardware-hackers/16-vietnam-meetup-sean-boyce-talk/)  [![Larger bot the size of a box of cereal](img/5c340f61466fbaa90afd2e44ebd2b249.png "07-vietnam-meetup-large-robot")](https://hackaday.com/2019/03/27/hacker-abroad-vietnams-hardware-hackers/07-vietnam-meetup-large-robot/) Larger bot the size of a box of cereal [![Small cellphone-controlled bot the size of playing cards](img/b83f3d3de5900ba923a71bb5447b3093.png "08-vietnam-meetup-small-robot")](https://hackaday.com/2019/03/27/hacker-abroad-vietnams-hardware-hackers/08-vietnam-meetup-small-robot/) Small cellphone-controlled bot the size of playing cards

肖恩·博伊斯做了一个关于他建造的两个机器人项目的报告。大的那个有一个独立的控制器，由另一个项目遗留下来的部分拼凑而成。小的由你的手机控制。演讲的精彩部分在于，Sean 做了很好的工作，解释了如何为远程控制系统建立一个通信方案，这样你就不会不小心把机器人从桌子上弄下来或者撞到别人的胫骨上。他使用 UDP 并在大约每 75 毫秒的定时循环上发送数据包。无效命令会将执行置于故障保护模式。

[![](img/7ec3974b76cb0a93733d06b2f91c224e.png)](https://hackaday.com/2019/03/27/hacker-abroad-vietnams-hardware-hackers/09-vietnam-meetup-dream-factory/)[![](img/4bd21d0934962efb49aecb5796315bd0.png)](https://hackaday.com/2019/03/27/hacker-abroad-vietnams-hardware-hackers/10-vietnam-meetup-arduino-day/)[![](img/55c911bdeab22758ac81a86071d781c2.png)](https://hackaday.com/2019/03/27/hacker-abroad-vietnams-hardware-hackers/15-vietnam-meetup-smart-doll/)

我们以三场会谈结束了会议。Alex 谈到了他的公司为建立一个名为“梦工厂”的创意空间所做的努力，该空间将作为硬件加速器和以教育为重点的技术中心。Nguyễn Quốc Bảo 做了一个关于即将在 HCMC 举办的 Arduino 日的演讲，最后的演讲是关于添加树莓 Pi、扬声器、摄像头和其他部件来创造一个智能娃娃。

## 总是应该有一个庆功宴

就像我们的大多数活动一样，每个人都想留下来研究硬件——我们必须在讲座结束后做大约 45 分钟。但是场地要关闭了，他们不得不把我们赶出去，所以我们去了下一个地方。黑暗之心有很棒的精酿啤酒，他们甚至从街上的一个地方给我们订了一些披萨。

 [![Hard to see, but there are hordes of scooters on this road](img/89a2c0744ff8b92efad28b695ccb2dbd.png "01-vietnam-scooter-traffic")](https://hackaday.com/2019/03/27/hacker-abroad-vietnams-hardware-hackers/01-vietnam-scooter-traffic/) Hard to see, but there are hordes of scooters on this road [![Helmets! Mike Szczys (left), Sean Boyce (right)](img/c7f5b5ec7bed49c8b34a5f8960d55dc0.png "11-vietnam-meetup-late-night-scooter-ride")](https://hackaday.com/2019/03/27/hacker-abroad-vietnams-hardware-hackers/11-vietnam-meetup-late-night-scooter-ride/) Helmets! Mike Szczys (left), Sean Boyce (right) [![Afterbar](img/484404d235272dae90c694b78b53cbf6.png "12-vietnam-meetup-afterbar-and-pizza")](https://hackaday.com/2019/03/27/hacker-abroad-vietnams-hardware-hackers/12-vietnam-meetup-afterbar-and-pizza/) Afterbar

我真的没有一个好的方式来表达 HCMC 的摩托车交通有多疯狂。步行时，你慢慢地涉入汹涌的摩托车流中，希望水流对你有利。在车流中开车是另一回事。你可以在 Vimeo 上找到一些很好的例子，但是除非你晚上跳上一辆小型摩托车，在街上行驶，否则你无法理解。幸运的是肖恩是一个伟大的车手，他有第二个头盔，我只是*认为*这是多么愚蠢，而不是真的有一个事件后悔。

 [![13-vietnam-lettuce-wraps-food](img/99a0977dcd0edd48a5fbf196c31a9e74.png "13-vietnam-lettuce-wraps-food")](https://hackaday.com/2019/03/27/hacker-abroad-vietnams-hardware-hackers/13-vietnam-lettuce-wraps-food/)  [![Squeezing juice from sugarcane, then add hand squeezed kumquats](img/0dc614ea222a4a12d8af35625e93773c.png "14-vietnam-sugar-cane-kumquat-water")](https://hackaday.com/2019/03/27/hacker-abroad-vietnams-hardware-hackers/14-vietnam-sugar-cane-kumquat-water/) Squeezing juice from sugarcane, then add hand squeezed kumquats

至于有趣的食物，这里有一个非常薄，做得非常好的鸡蛋，可以作为猪肉，虾，绿豆和豆芽的碗。把它包在莴苣壳里，蘸酱就行了。我还不得不尝试街车上的饮料。机械化奇迹从甘蔗中榨出液体。他们把它倒在冰上，榨几个金橘汁调味，然后送你上路。好吃！

在越南开始的这一天很短，但我们通过努力在周一完成所有的事情来弥补。《黑客出国》下期*的话题*包括参观胡志明市的五金市场和电子市场，喝三种咖啡，吃遍全城。回头见！