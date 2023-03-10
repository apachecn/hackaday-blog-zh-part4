# 比赛结果:树莓派表演

> 原文：<https://hackaday.com/2018/10/12/contest-results-raspberry-pis-put-on-a-show/>

一些最令人满意的项目是视觉化的。所有的网络路由器、数据记录器和恒温器都很棒。但是，我们是视觉动物，即使是一个不起眼的闪烁的 LED 也足以让你感到有点匆忙，甚至与寻找一个大的质数相比。我们想看看我们的社区可以用一个 Raspberry Pi 做些什么，所以我们[用 Pi 比赛](https://hackaday.io/contest/160366-visualize-it-with-pi)挑战你。

和往常一样，竞争很激烈，有很多很棒的项目。这次比赛展示了使用 LED 模块和组件为项目添加视觉效果的趋势。为什么不呢？它们足够便宜，一个集成良好的模块可以使项目的布线和集成变得简单。

我们没有看到你可能期望的那么多与媒体相关的项目，尽管有一个与*陌生人的事情*，一个与*创*，虚拟现实照明项目确实有一些*星球大战*的图像。项目范围从实用的储物盒标签到随着音乐节拍闪烁的古怪柠檬水瓶子。如果这些对你来说都不过瘾，甚至还有树莓 Pi 控制的射电望远镜。你可以在 [Hackaday.io](https://hackaday.io/submissions/visualize-it-with-pi/list) 上找到所有的条目。现在让我们看看哪些参赛作品成功打动了评委。

## 大奖:复古游戏 LED 显示屏

我们不得不说,[ makeTVee 的标题并没有公正地对待这个项目。在一些 led 上玩俄罗斯方块很有趣，但不止如此。我们猜测“[巨型壁挂式 Wi-Fi 控制复古游戏机](https://hackaday.io/project/11064-raspberry-pi-retro-gaming-led-display)”似乎太拗口了。看看下面的视频，了解一下这是怎么回事。

 [https://www.youtube.com/embed/mOMQ4rWU_1w?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/mOMQ4rWU_1w?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



我们喜欢对细节的关注，当然，还有尺寸。这也不仅仅是一匹只会一招的小马。你可以玩贪吃蛇或乒乓球，当然也可以自己玩。光是建筑就足以上墙，项目文档也很棒。

## 最佳深奥数据源

过去几周，国际空间站一直是新闻焦点。如今，跟踪电视台并不是什么大事，但是如何显示关于确切位置的数据呢？[Bornach]想要使用一个 LED 环，但发现他们没有将它们做得足够大，以获得良好的分辨率。旋转的发光二极管将采用滑环或一些其他方案来获取数据和电力到旋转的部分。相反，这个项目使用发光二极管和一个连接到步进电机的旋转镜。结果是[一个经度显示，用不同的颜色和线长代表人类城市在太空中的纬度](https://hackaday.io/project/161514-radial-led-projection-iss-tracker)。

[![](img/3ab8b85c7bb6bd6836e402bfcfa479e8.png)](https://hackaday.com/wp-content/uploads/2018/10/issdisk.png)

整件事只需要 36 个发光二极管，虽然你可能会想到，在镜子旋转的任何给定点，只有少数几个是可见的。[Bornach]计划使用霍尔效应传感器使显示器像指南针一样工作。还计划添加更多的 led，甚至将其投射到现有的表面，如墙壁上。迫不及待地想看看这些！

## 最佳互联网数据源

我们几乎觉得我们在激发[螺线管的]物联网 LED 矩阵显示器方面有所贡献。使用的 32×32 RGB LED 矩阵是在之前的 Hackday 比赛中赢得的！Raspberry Pi 是一个节点红色服务器，使用 MQTT。它将数据流传输到一个 ESP32，ESP32】驱动 LED 矩阵。当然，显示器可以接受来自任何服务器的数据。

[![](img/c231ca8fa2572c01418ba4c488b01e77.png)](https://hackaday.com/wp-content/uploads/2018/10/clock.jpg)

Node-RED 确实很酷，这将是一个让你体验它的好项目。文档是好的，除了一个单词时钟，甚至有一个快乐的扳手扔在屏幕上。随着 MQTT 无处不在，您一定会发现像这样的显示有用处。

## 最佳直连传感器

很难想象你如何改进一瓶柠檬水。但是[艾琳·Xi]通过制作一个带有声音探测器的瓶子来接收音乐节拍，并用灯光效果显示节拍，从而做到了这一点。

 [https://www.youtube.com/embed/2KdmDke1xrg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/2KdmDke1xrg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



顺便说一下，设计中的 Pi 是一个 Pi 零点，还有一个模拟转换器 ADS1015。该项目工程，但有改进计划，包括灵敏度控制和更好的包装与瓶子的组成部分。

## 哇！

我们总是对我们的黑客能提出的东西印象深刻，虽然这些是评委的最佳选择，但也有许多其他的[伟大项目在竞争](https://hackaday.io/contest/160366-visualize-it-with-pi)。从吉他英雄到桌上时钟，如果你花几分钟浏览，你一定会找到你喜欢的东西。

祝贺获奖者和所有参赛者提出了一些惊人的 Pi 项目。正如你所料，奖品包括一些 LED 环和带，以帮助照亮他们的下一个条目！也请务必关注我们即将到来的比赛。你必须参加才能赢。