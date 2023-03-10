# 如果你能测量它，你必须展示它

> 原文：<https://hackaday.com/2021/05/01/if-you-can-measure-it-you-must-display-it/>

你什么时候能确定你记录了足够的数据？当你记录所有数据的时候！当然，上述半开玩笑的格言也有例外，但这无疑是一个好的开始。尤其是因为如今在 SD 卡上存储数据是如此容易和便宜，几乎没有理由不记录您的项目可能产生的几乎每一点数据。即使没有 SD 卡，许多微控制器也有足够的板载闪存，甚至 RAM，来处理你扔给它们的任何东西。那么，诀窍就是从这些数据中找到意义，至少对我来说，这通常意味着画出漂亮的图画。

本周，一款简单而优雅的步进电机诊断工具给我留下了深刻的印象，它是由【Zapta】开发的。本质上，它是一个简单的设备:它是一个“黑色药丸”开发板，两个电流传感器，一个用于存储设置的 EEPROM 和一个触摸屏。鉴于我们大多数拥有 3D 打印机的人都依赖步进电机来完成工作，进行一些诊断当然很有趣。

[![](img/74bada0f27615feb42fa003d3452b74a.png)](https://hackaday.com/wp-content/uploads/2021/04/phase_screen_accelerating_thumbnail.png) 通过记录步进电机每一相上的电压和电流测量值，你可以了解到正在发生的事情，至少如果你能可视化所有这些数据的话。这就是[Zapta]的工具大放异彩的地方。它绘制电流与电机速度的关系图，以检测阻抗问题。首先调整电流是一个与利萨如模式的快照，它会跟踪您的挤出机的进展或寻找整个印刷作业中跳过的步骤。它通过许多精心设计的图表来完成所有这些工作。

我和[尼克拉斯·罗伊]谈论这个，他说“哦，看看我的悬浮滑板电池记录器”。又来了！它与电池串联，记录电流和电压，充电或放电。图表可以让您直观地了解一段时间内的用电量，实时时钟可以让您将其与使用悬浮板的视频同步，以帮助您更好地理解数据。

你还在等什么？传感器很便宜，存储器也很便宜，而且事后绘制数据图表的工具也很多。如果你没有记录所有相关的数据，你就错过了一些有价值的见解。如果是的话，[我们很想看看你的项目](https://hackaday.com/submit-a-tip/)！(提示，提示。)

This article is part of the Hackaday.com newsletter, delivered every seven days for each of the last 200+ weeks. It also includes our favorite articles from the last seven days that you can see on [the web version of the newsletter](https://mailchi.mp/hackaday.com/hackaday-newsletter-649368). Want this type of article to hit your inbox every Friday morning? [You should sign up](http://eepurl.com/gTMxQf)!