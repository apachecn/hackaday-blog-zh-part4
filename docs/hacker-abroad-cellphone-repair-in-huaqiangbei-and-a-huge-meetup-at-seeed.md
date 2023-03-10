# 海外黑客:华强北的手机维修和 Seeed 的大型聚会

> 原文：<https://hackaday.com/2019/03/25/hacker-abroad-cellphone-repair-in-huaqiangbei-and-a-huge-meetup-at-seeed/>

中国深圳是传说中的华强北电子市场的所在地。周五是我在上海度过的第一个完整的一天，之前三天我都在上海。我们出发得有点晚，因为我们的航班凌晨 1 点多才到达，第一天晚上我们住在一家机场酒店。我们与 Scotty Allen 一起吃了一顿令人惊叹的饭，随后在电子市场有了一次非常独特的经历，不仅看到了商品，还见到了展示他们一些秘密的摊位老板。

这一天在 x . factory(Seeed Studio 运营的协作创意空间)以一场绝对爆满的聚会结束。他们安排了半打非常出色的硬件会谈，随着时间的推移，有大量的硬件被展示出来。他们不得不把我们赶出去，否则我们会整晚呆在这里！

## Seeed 聚会现场座无虚席

![](img/50f9809f7b0e60d0636fbed65dead1b1.png)

当我们到达 X.Factory 的时候，这里已经挤满了兴奋的黑客们，他们正在享用披萨、爆米花鸡肉和啤酒(出于某种原因，百威啤酒在这里很受欢迎)。Sophi Kravitz 和我就 [2019 Hackaday Prize China](https://hackaday.com/2019/03/21/hacker-abroad-massive-conference-brings-big-news-of-hackaday-prize-china/) 发表了演讲，这是一项专注于产品开发的设计挑战，可以通过中文文档参赛。在 Hackaday 奖举办五年后，有如此多令人惊叹的参赛作品可供炫耀，与第一次错过它们的人分享这些故事，以及那些准备加入挑战的人，真是令人兴奋。

 [![shenzhen-d1-01-01-starwars-business-cards](img/b63d236051e364a4f9f21f6bd258dc8d.png "shenzhen-d1-01-01-starwars-business-cards")](https://hackaday.com/2019/03/25/hacker-abroad-cellphone-repair-in-huaqiangbei-and-a-huge-meetup-at-seeed/shenzhen-d1-01-01-starwars-business-cards/)  [![shenzhen-d1-01-02-robot-business-cards](img/f29cf3a12de11ef5a3364967f07c58e5.png "shenzhen-d1-01-02-robot-business-cards")](https://hackaday.com/2019/03/25/hacker-abroad-cellphone-repair-in-huaqiangbei-and-a-huge-meetup-at-seeed/shenzhen-d1-01-02-robot-business-cards/)  [![shenzhen-d1-01-03-millenium-falcon-business-cards](img/4b6c77e6ea298d7f09175c7c7eb49956.png "shenzhen-d1-01-03-millenium-falcon-business-cards")](https://hackaday.com/2019/03/25/hacker-abroad-cellphone-repair-in-huaqiangbei-and-a-huge-meetup-at-seeed/shenzhen-d1-01-03-millenium-falcon-business-cards/) 

第一个硬件讲座是一个关于迭代 [PCB 名片的故事，这些名片可以被剪切和切割在一起以创建 3D 雕塑](https://www.facebook.com/Geeekclub-297810750885446/)。用红色你可以看到卡片的第一次迭代，它形成了一个机器人。但是 Nico 收到了很多积极的反馈，所以他继续前进。一路上，他开始将电路和元件融入设计中，你可以看到他建造的步行机，以及一只千年隼和其他几只。

 [![shenzhen-d1-02-01-robo-hat-team](img/1229596ccd644c1a17a9165f587f0ea5.png "shenzhen-d1-02-01-robo-hat-team")](https://hackaday.com/2019/03/25/hacker-abroad-cellphone-repair-in-huaqiangbei-and-a-huge-meetup-at-seeed/shenzhen-d1-02-01-robo-hat-team/)  [![shenzhen-d1-02-02-robo-drinking-demo](img/f0d0bf8caeb4ac7327703386899d14e9.png "shenzhen-d1-02-02-robo-drinking-demo")](https://hackaday.com/2019/03/25/hacker-abroad-cellphone-repair-in-huaqiangbei-and-a-huge-meetup-at-seeed/shenzhen-d1-02-02-robo-drinking-demo/) 

能在 Hackaday.io 上看到关于我最近注意到的一个项目的讨论真的很酷。 [Robo HAT MM1](https://hackaday.io/project/164285) 正在为[的众包活动](https://www.crowdsupply.com/robotics-masters/robo-hat-mm1)做准备，很高兴看到团队出来展示他们的工作演示。这是一个逻辑板，旨在使其更容易控制机器人的伺服电机。外形是作为 Raspberry Pi 的子板(hat ),但由于板载微控制器，它也能够进行独立控制。这是一个 ATSAMD21 运行电路 Python，板包括一个 IMU。最有趣的演示是一个机器人手臂，它有多个伺服系统，由加速度计的轴控制——但试图找出哪个轴映射到每个手臂的运动，使自己喝一口苏打水成为一项混乱而有趣的任务。早在 2017 年，琳达·罗(Linda Luo)在与学生合作建造基于张量流的自主赛车平台驴车(Donkey cars)时，烧掉了一些树莓 Pis，从而产生了 RoboHAT 的想法。

![](img/8f5176579921a9a876b7f953a8c8a885.png)

我没有机会与这个项目的创作者交谈，但我想提一下，因为我真的很喜欢这个背景故事。这是一个使用 iPad 的显微镜项目。iPad 有一个固定的平台，然后是一个可移动的平台，设计得像一个微型剪式升降机。将您的拍摄对象放在升降台上，并进行调整，直到放大倍率对准焦点。通过简单的放大观察树叶和其他植物群，这是一种帮助你的孩子对科学感兴趣的廉价方式。

 [![shenzhen-d1-04-01-underwater-camera-platform-prototype](img/9b23cf0a82b16ee1f37950764d26931b.png "shenzhen-d1-04-01-underwater-camera-platform-prototype")](https://hackaday.com/2019/03/25/hacker-abroad-cellphone-repair-in-huaqiangbei-and-a-huge-meetup-at-seeed/shenzhen-d1-04-01-underwater-camera-platform-prototype/)  [![shenzhen-d1-04-02-underwater-camera-platform-prototype-closeup](img/3dac6fa888297a343346c75387e9920a.png "shenzhen-d1-04-02-underwater-camera-platform-prototype-closeup")](https://hackaday.com/2019/03/25/hacker-abroad-cellphone-repair-in-huaqiangbei-and-a-huge-meetup-at-seeed/shenzhen-d1-04-02-underwater-camera-platform-prototype-closeup/) 

[开放海洋相机](https://openoceancam.com)是一个水下研究平台，其灵感来自 2017 年 Hackaday 奖得主[开源水下滑翔机](https://hackaday.io/project/20458-osug-open-source-underwater-glider)。我们只有很少的工具来进行长期的海洋物种观察。把相机放在那里带来了保持电力流动、存储图像和检索图像的挑战。GoPro 相机已经被用来做到这一点，但它们需要频繁的干预来更换电池。这个项目利用一个简单的电源来保持树莓 Pi 相机运行更长时间。这可以运行更长时间，并且需要更少的访问来更新电池和下载内容。

![](img/883462cde5a352356f090002e4c18f60.png)

有一个关于智能扬声器构建的演示。项目创建者提出了一个很好的理由，即制造一个智能扬声器比破解一个现有的更好，因为它打开了许多附加功能。他带领观众经历了原型的几次迭代，并展示了当前版本，该版本使用了 Raspberry Pi、ReSpeaker 麦克风阵列和单个扬声器，所有这些都在激光切割外壳中。

 [![shenzhen-d1-06-01-dexta-vr-glove-prototypes](img/afedd28e46decbaf739617ba9a6f72e8.png "shenzhen-d1-06-01-dexta-vr-glove-prototypes")](https://hackaday.com/2019/03/25/hacker-abroad-cellphone-repair-in-huaqiangbei-and-a-huge-meetup-at-seeed/shenzhen-d1-06-01-dexta-vr-glove-prototypes/)  [![shenzhen-d1-06-02-dexta-vr-glove-prototypes](img/d2f4e60528a89e869abf1ed9c970afd5.png "shenzhen-d1-06-02-dexta-vr-glove-prototypes")](https://hackaday.com/2019/03/25/hacker-abroad-cellphone-repair-in-huaqiangbei-and-a-huge-meetup-at-seeed/shenzhen-d1-06-02-dexta-vr-glove-prototypes/) 

在这次活动中见到 Dexta 团队真是太棒了。他们没有做讲座，但他们带来了他们的触觉反馈虚拟现实手套，并要求我尝试一下。

![](img/ab1313703e4e7a4da66f9a83e95d8726.png)要点是，当你在沉浸式虚拟现实环境中时，你可以在双手上佩戴一个，指关节附近的伺服系统会根据你握着的虚拟物体产生力反馈。固体和糊状物品之间的区别非常明显。而[手里拿着一颗虚拟跳动的心脏](https://twitter.com/szczys/status/1109091257463263233)每个手指都在跳动。每只手套大约有 6 小时的电池时间，团队已经通过了大约 50 个原型才能达到这一点。他们很快就要开始销售了，但是在你的客厅里有一套这样的电视机可能还需要一段时间。欢迎来到绿洲。

## 硬件市场的手机维修

当天早些时候，我和斯科特·艾伦前往华强北五金市场，看看我们能看到什么。我们的计划是在为[黑客日播客](https://hackaday.com/podcast)录制音频时走一遍。(请订阅，以便在本集发布时收到提醒。)斯科特当然是这些市场的生活专家，因为他一直在他的【YouTube 频道上报道这个话题。

在建筑物内拍照或多或少是被禁止的，所以不幸的是我不能和你分享太多的照片。但是当我们在轩豪展位停下来的时候，一个特别的惊喜出现了。这个柜台出售手机维修工具，由两兄弟经营，我已经安排了他们周六的播客采访。他们的摊位上堆满了有趣的工具，其中之一是手机屏幕对准夹具，用于在液晶显示器仍然良好的情况下更换手机屏幕的玻璃。我问的问题是，将高科技三明治粘合在一起的光学透明粘合剂(OCA)是如何产生的——是薄膜还是液体。他们的摊位不卖亚奥理事会，但过道对面的摊位卖，所以他们借了一个样品，我们继续交谈。当我问更多的问题时，Xua 说为什么我们不去看看它是怎么做的？

 [https://www.youtube.com/embed/f9VWqtI8Xwk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/f9VWqtI8Xwk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



他的朋友明拥有一个专门从事手机屏幕维修的摊位。有趣的是，Scotty 在其中一个视频中深入描述了这一过程([大约 6:11 进入](https://www.youtube.com/watch?v=leFuF-zoVzA) ) —工具和过程是相同的，但这是一个不同的展台。看了几分钟后，他们问我是否想把这个过程拍成视频。是的是唯一的答案，多么好的款待！视频中显示了以下步骤:

1.  测试破碎的屏幕，以确保液晶屏和触摸屏未损坏，只有玻璃需要更换
2.  使用加热的真空台和非常细的金属丝将玻璃与 LCD 分开
3.  用旋转工具清洁液晶显示器，然后用液体溶剂(谷歌翻译说这是:酒精和白油)
4.  将光学透明贴膜放在 LCD 上，并修剪多余部分
5.  清洁新玻璃，并使用夹具将其精确定位在 LCD 上
6.  用热压机激活胶水
7.  用真空室去除气泡

这个过程很快，因为这些技术人员知道他们的工艺。整个遭遇是关于市场力量的一课。需要做点什么吗？需要原材料吗？想学个流程？如果你有正确的关系，在这里可以做任何事情。

## 美食和好朋友

 [![Sophi and her sister Anna enjoy a meal together](img/8eefb5c3741f3e4599ba3ac87e2c4641.png "shenzhen-d1-09-03-sophi-and-anna")](https://hackaday.com/2019/03/25/hacker-abroad-cellphone-repair-in-huaqiangbei-and-a-huge-meetup-at-seeed/shenzhen-d1-09-03-sophi-and-anna/) Sophi and her sister Anna enjoy a meal together [![Bug on a stick](img/8cfca3f82f1f1e0715d532ce24685a10.png "shenzhen-d1-09-lunch-skewer")](https://hackaday.com/2019/03/25/hacker-abroad-cellphone-repair-in-huaqiangbei-and-a-huge-meetup-at-seeed/shenzhen-d1-09-lunch-skewer/) Bug on a stick [![Delicious rice paste patties with seasame seeds, and cucumber in soy and spicy pepper](img/a8a342036ff275c1e5af2123f85fdff7.png "shenzhen-d1-09-02-pickles")](https://hackaday.com/2019/03/25/hacker-abroad-cellphone-repair-in-huaqiangbei-and-a-huge-meetup-at-seeed/shenzhen-d1-09-02-pickles/) Delicious rice paste patties with seasame seeds, and cucumber in soy and spicy pepper

在这漫长的一天的两端是难以置信的食物、饮料和友谊。快到午饭时间时，他带我们去了一家很棒的餐厅。在某个时候，我会详细介绍微信生活整合体验，但这篇文章已经很长了。要点是餐桌上的每个人都可以扫描二维码并点菜(带有图片，用于发现你将要吃的东西)，食物就会开始出现。好吃！

 [![Eric Pan, Lily, and Violet took us to a craft beer place](img/c525a1671fcd90ecc5abebd96e1cb390.png "shenzhen-d1-10-seeed-studio-craft-beer")](https://hackaday.com/2019/03/25/hacker-abroad-cellphone-repair-in-huaqiangbei-and-a-huge-meetup-at-seeed/shenzhen-d1-10-seeed-studio-craft-beer/) Eric Pan, Lily, and Violet took us to a craft beer place [![Street art near the craft brewery](img/cc2459c132a5ab0efbfe3cce89851071.png "shenzhen-d1-11-street-art")](https://hackaday.com/2019/03/25/hacker-abroad-cellphone-repair-in-huaqiangbei-and-a-huge-meetup-at-seeed/shenzhen-d1-11-street-art/) Street art near the craft brewery

我非常感谢 Lily、Violet、Eric Pan 和 Seeed 工作室团队的所有人。他们不仅开门迎客，为聚会带来了令人难以置信的人群，还举办了一场别开生面的酒吧聚会。我们在一个地方停下来，那里有很棒的啤酒和美味的开胃菜，就在最初的柴火创客空间所在的大楼对面。Eric 告诉我们这是深圳第一批工业园区之一。在一个以推倒一切旧建筑而闻名的城市，在一个已经翻新和更新以供新用途的地方闲逛是一件有趣的事情。

## 接下来:会见店主

我的周六和电子市场店主的会议被预定了。大部分时间将集中在播客的音频上，但我会在下一期的《海外黑客》中分享一些有趣的内容。