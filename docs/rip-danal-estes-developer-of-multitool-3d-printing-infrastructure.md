# 多工具 3D 打印基础设施开发商 RIP Danal Estes

> 原文：<https://hackaday.com/2020/06/13/rip-danal-estes-developer-of-multitool-3d-printing-infrastructure/>

上周，[Danal Estes]去世了。这让我们当中许多有幸在网上与他互动的人感到震惊。[Danal]不仅是 3D 打印社区的积极贡献者，他还是一个热心肠的人，和他相处很有趣。不到一年前，我在网上认识了[Danal]。但是我欠他一笔债，他帮我把我在网上发布的一组设计文件转化成了一个硬件爱好者的成熟社区。

这是我最好的一张照片，从认识他的改变工具的 3D 打印爱好者那里，我看到了这个人类伙伴的一些遗产。

## 了解一个在线社区建设者

去年九月，我通过 Thingiverse 在网上第一次见到[Danal]，当时他发布了一个 [Jubilee](https://hackaday.com/2019/11/14/jubilee-a-toolchanging-homage-to-3d-printer-hackers-everywhere/) 的 [*make*](https://www.thingiverse.com/make:710529) ，这是我几周前发布的一个换刀机设计。在 Jubilee 只是互联网上的一组文件和说明的时候，我对世界上有人在那里建造一个复制品感到兴奋。为了更好地了解这些人，并找出他们装配过程中的任何关键点，我创建了一个 Discord 聊天服务器。[Danal]第一个加入并开始用图片讲述他的故事。

 [![IMG_0759_R](img/95279b2b8d2c28c69fc6712fc82ea5a2.png "IMG_0759_R")](https://hackaday.com/2020/06/13/rip-danal-estes-developer-of-multitool-3d-printing-infrastructure/img_0759_r/)  [![IMG_0758](img/ed50e48551c47626c7e3b9ef05d0ffc2.png "IMG_0758")](https://hackaday.com/2020/06/13/rip-danal-estes-developer-of-multitool-3d-printing-infrastructure/img_0758/) 

随着一个充满好奇的不和谐群体的成长，关于这台机器的问题开始出现。它有多大？工具更换是如何进行的？我试着回答尽可能多的问题，在 Thingiverse 上放了一个 FAQ 简介，但是几个星期后，发生了另一件事:*【Danal】开始回答问题*。不仅如此，他几乎和每一个在服务器上介绍自己的人打招呼。我不明白一句简单的“欢迎加入”有什么价值这是在某人在一个萌芽中的网络社区的第一个帖子之后，但[Danal]做了。所以他就这么做了。他让你觉得来到互联网的这个角落是受欢迎的。在一个满是不喜欢重复自己的工程师的世界里，[Danal]似乎意识到他的重复互动对另一端的人来说是新的；这使得它值得去做。

![](img/dc852c14873a7320373785eb9eb170ab.png)

Danal’s first tool changes

随着时间的推移，问题不断,[Danal]继续向人们提供问题的答案——甚至是重复的问题。与此同时，他发布了自己机器的进度图。在某种程度上，社区的其他人在这段时间似乎都在屏住呼吸，看着[Danal]发布状态报告；等着确信这些文件真的变成了有用的东西。然后，不到一个月后，[Danal]发布了他第一次成功换刀的视频。成功了！几乎可以肯定的是，受到[Danal]成功的鼓舞，更多的人开始建造他们自己的机器。但是[Danal]是第一个复制禧年的人。

自从我在九月份发布项目文件以来，已经有超过二十台机器在野外被制造出来。我相信，开始的灵感来自于之前完成的人的成功，这种成功又来自于第一个完成的人的成功:[Danal Estes]。为此我欠他一个人情:因为他激励了一群人跟随这一冒险。

 [![IMG_0387](img/4da746d4ab19fb7bf8eb9bb48bdbb6b8.png "IMG_0387")](https://hackaday.com/2020/06/13/rip-danal-estes-developer-of-multitool-3d-printing-infrastructure/img_0387/)  [![IMG_0421_1 (1)](img/0a5e6eb346fbb311b813bd226e4074ef.png "IMG_0421_1 (1)")](https://hackaday.com/2020/06/13/rip-danal-estes-developer-of-multitool-3d-printing-infrastructure/img_0421_1-1/) 

## 商品化的自动喷嘴对准

[Danal]不仅向新的禧年社区肯定了机器设计。在项目的短暂时间内，[Danal]戴上了他的软件帽子，开发了一个基于机器视觉的自动化工具对准系统，他称之为 TAMV。事实证明，工具尖端校准是任何多喷嘴 3D 打印机的棘手问题之一。工具必须相对于彼此对齐，使得它们印刷的每种独特材料在最终的印刷中对齐。目前的做法是繁琐和手动的。你可以通过[打印一个游标尺](https://e3d-online.dozuki.com/Guide/12+-+Multi-Material+Calibration./114?lang=en)或者用朝上的显微镜拍照来测量偏移量。[Danal]将这个棘手的问题视为完全自动化过程的机会，所以他这样做了。

![](img/8013b95d58146ec6aa8984719ec1f560.png)

仅仅两个月后，[Danal]带着一份关于 Jubilee Discord 的公告回来了，展示了[*【TAMV】*](https://github.com/DanalEstes/TAMV)，又名:*刀具对准机器视觉*。通过在他的 Jubilee 前面安装一个朝上的网络摄像头，[Danal]只需运行他的一键脚本，他的机器就会自动校准每一个可用的工具，比大多数人用以前的方法更好。它通过依次拾取工具，将它们放入相机视野，然后测量它们的偏移量来实现这一点。更重要的是，他以开源的方式发布了整个代码库，通过一个他自己编写的简单安装脚本和设置说明，就可以使用一个商品化的解决方案，将一个棘手的问题变成了过去。

在 Hackaday 上，读到人们在家里舒适的工作台上克服的惊人壮举，真是令人羞愧。但令人振奋的是，看到同样的壮举以一种让我们打开它，从中学习，并在它的基础上建设的方式展现出来。记录你已经完成的工作，并希望其他人可以效仿，这是一种优雅的行为。[Danal]是亲切的。

## 项目中讲述的共享故事

随着[Danal]成为 Discord 上最活跃的社区成员之一，我们开始更多地了解他的其他项目。对[Danal]来说，3D 打印机是一个次要项目，就像它们是创造性项目的其他工具家族中的工具一样。用这些机器武装起来后，[Danal]让它们在飞行机器上工作，从几乎无法通过入口控制翼展的非凡遥控飞机(当然是 3D 打印的)到可以搭载飞行员的真实世界飞机的控制台。

[![](img/35bf6d368670dc5788b6b4f2e1faf83e.png)](https://hackaday.com/2020/06/14/dial-in-your-multi-headed-3d-printer-with-2020-machine-vision/img_0851e/)[![](img/5bd3017dff46c88f52582281e995605a.png)](https://hackaday.com/2020/06/14/dial-in-your-multi-headed-3d-printer-with-2020-machine-vision/f4u_corsair_parts/)[![](img/387a0db55d91fc20e9f8da6815654a07.png)](https://hackaday.com/2020/06/14/dial-in-your-multi-headed-3d-printer-with-2020-machine-vision/img_1386/)[![](img/02f93287db25c79ddcbec29395cc263e.png)](https://hackaday.com/2020/06/14/dial-in-your-multi-headed-3d-printer-with-2020-machine-vision/danals_panel/)

了解[Danal]的冒险经历总是一件乐事。越来越多的爱好者渴望回到我们的工作台，听到他在投影方面的兴奋是他们的食物。他冒险经历的框架足够温暖，让你觉得你不仅仅想让自己有一点这种生活方式，你也可以让 T2 有这种生活方式。我希望(Danal 的)遗产的这一部分是我们在线人可以继续的:在一个硬件黑客社区中，对新来者的共同礼貌和热情态度。

谢谢你，伙计。我已经开始想你了。