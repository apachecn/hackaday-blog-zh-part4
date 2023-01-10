# 机器鱼利用摄像头和发光二极管聚集在一起

> 原文：<https://hackaday.com/2021/01/18/robotic-fish-swarm-together-using-cameras-and-leds/>

在过去的几十年里，机器人技术突飞猛进，但在机器人群体的分散协调方面，它们远远落后于生物群体。哈佛大学韦斯研究所的研究人员正在努力缩小这一差距，并开发了一种名叫 [Blueswarm](https://www.seas.harvard.edu/news/2021/01/robotic-swarm-swims-school-fish) 的机器鱼，它可以在没有外部集中控制的情况下表现出群体行为。

在真正的鱼群中，一条鱼的运动依赖于它周围的鱼。为了让每条机器鱼估计其邻居的位置，它们配备了一组 3 个蓝色发光二极管，身体两侧各有一个摄像头。受珊瑚鱼启发，四个振荡鳍提供 3D 控制。鳍片的致动器是一个简单的旋转磁铁，位于一个接受交流电的线圈内。每条鱼的板载电脑是一个树莓 Pi W，摄像头是树莓 Pi 的摄像头模块，带广角镜头。利用摄像头计算出的位置信息，学校可以协调其运动，以分散开来，聚集在一起，围成一圈游泳，或找到一个物体，然后会聚在其上。如果你对细节感兴趣，可以免费获得完整的学术文章。

[与光的交流](https://hackaday.com/2015/12/11/hackaday-explains-li-fi-visible-light-communications/)取决于它所通过的介质的清晰度，在这种情况下，是水——而条件可能很快成为一个限制因素。长期以来，潜艇一直面临着同样的挑战。两个当前的替代解决方案是 ELF 无线电和声音，这两个都在[Lewin Day]关于[水下通信](https://hackaday.com/2020/07/15/the-many-methods-of-communicating-with-submarines/)的优秀文章中涉及。

 [https://www.youtube.com/embed/1pflbeDRkUs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/1pflbeDRkUs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



谢谢你的提示！