# 用这个自助结账游戏练习你的购物技巧

> 原文：<https://hackaday.com/2022/05/18/practice-your-shopping-skills-with-this-self-service-checkout-game/>

自助结账已经成为世界各地超市的一个普遍特征，疫情冠状病毒加速了这一趋势。虽然有些人可能会哀叹失去了人与人之间的联系，但其他人喜欢自己扫描的机会:通过一点练习，自助服务可以提供非常快速的结账体验。当然，假设机器能够识别每个产品，内置的重量传感器工作正常，你不会被随机选中。

如果你想在不花很多钱的情况下练习结账游戏，你可能想看看[Niklas Roy]和[Kati hyypp]的最新项目: [Bonprix 是一款游戏，目标是在 90 秒的时限内扫描尽可能多的物品](https://niklasroy.com/bonprix/)。安装在 [Eniarof](https://www.eniarof.com/maintenance) DIY 节上，它的设计类似于一个典型的超市收银台，有一个显示器，一个条形码扫描仪和一个装满随机物品的购物篮。屏幕指示接下来应该扫描哪个项目；如果你太慢，收银台会开始打折，这显然是你不想要的。当 90 秒结束时，机器会吐出一张收据，显示你的总分。

收银台由木托盘和纸板制成；里面是一台运行 Linux 的笔记本电脑，带有一个通过 USB 连接的手持条形码扫描仪。LED 条提供一束明亮的红光来指示扫描区域，当条形码被成功扫描时变成绿色。Arduinos 控制发光二极管和红黄相间的大“开始”按钮，而 ATM 的热敏打印机在每场比赛结束时打印收据。

除了一点乐趣，Bonprix 项目试图解决与消费者文化和自助结账相关的问题:让顾客自己做工作公平吗？他们应该为此得到报酬吗？鼓励人们尽可能多的消费是道德的吗？

虽然这是我们第一次看到自助结账的电脑游戏，但我们已经深入研究了使这一切成为可能的迷人的条形码技术。[看看这个](https://hackaday.com/2015/11/02/the-eloquence-of-the-barcode/)！

 [https://www.youtube.com/embed/c2M7-jrn_cI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/c2M7-jrn_cI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

