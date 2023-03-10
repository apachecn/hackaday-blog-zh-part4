# 用机器人创作大型多米诺艺术

> 原文：<https://hackaday.com/2021/07/29/create-large-scale-domino-art-with-a-robot/>

创作大型多米诺艺术展览是一个漫长而伤脑筋的过程，撞上一张多米诺意味着从头开始。为了使制作这些展示的过程自动化，一个由[Mark Rober]、[John Luke]、[Josh]和[Alex Baucom]组成的团队建造了[Dominator](https://www.baucomrobotics.com/domino-robot)，这是一个能够在 24 小时内放置 10 万个多米诺骨牌的机器人。休息后的视频。

![](img/7493353797d86a4d7f81199c6f7303cb.png)

[马克·罗伯]已经考虑这个想法几年了，在[马克]在 2019 年湾区创客博览会上的一次演讲中提到它后，这个项目终于启动了。为了实现这一目标，该团队创建了一个完整的多米诺骨牌铺设系统，包括自动装载站、精确的室内定位系统和机器人本身。该机器人围绕一个铝型材框架建造，骑在三个由精密伺服电机驱动的全向轮上。安装在机器人前面的一个大托盘可以一次容纳和释放 300 张多米诺骨牌。主控制器是 Raspberry Pi 4，它从 Marvelmind 室内定位系统和一个向下的红外摄像头接收定位信息，该摄像头会在地板上寻找反射标记。装载系统使用传送系统将不同颜色的多米诺骨牌送入工业库卡机器人，机器人将这些多米诺骨牌放入一个可以同时容纳多层的管道网格中。

[约翰·卢克]和[乔希]建立了机械，而[亚历克斯]处理电子和软件。[Alex]还写了一系列优秀的帖子(上面有链接)，详细介绍了开发过程、硬件、控制系统、软件架构和轨迹生成。他还在 [GitHub](https://github.com/alexbaucom17/DominoRobot) 上发布了所有代码。

[马克·罗伯]在 YouTube 上因合作雄心勃勃的项目而闻名，如[自动靶心靶](https://hackaday.com/2017/03/22/dartboard-watches-your-throw-catches-perfect-bullseyes/)、[针对包裹窃贼的闪光炸弹](https://hackaday.com/2018/12/17/hacker-makes-a-flawless-booby-trap-strikes-back-against-package-thieves/)和[制导保龄球](https://hackaday.com/2019/11/24/cheating-at-bowling-the-hacker-way/)。

 [https://www.youtube.com/embed/8HEfIJlcFbs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/8HEfIJlcFbs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

