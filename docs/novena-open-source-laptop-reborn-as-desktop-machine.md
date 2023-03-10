# Novena 开源笔记本电脑重生为台式机

> 原文：<https://hackaday.com/2022/02/23/novena-open-source-laptop-reborn-as-desktop-machine/>

当你用了 5 年的笔记本电脑报废了，通常是时候更换了。但是[安德鲁·梅纳杜]的 Novena 笔记本电脑是完全开源的。他可以完全接触到所有的文件，所以他决定试着修复它。有一天，电源电路板化为乌有——他将此归因于电池健康状况不佳，因为他没有足够频繁地使用它。鉴于他的使用模式，他决定将 Novena 换成台式电脑。

他用一个新的直通电源板进行了转换，计算机启动了，但没有显示。似乎电源故障也导致了额外的电路中断。[Andrew]陷入了电路板和芯片交换的深兔子洞，一切都无济于事。最终，显示屏突然活跃起来，他得出结论，问题出在 EEPROM 配置设置上，而不是 LCD 显示硬件。

![](img/16d3ac9770d46bcafd676013e7543735.png)

Experimenting with LCD Outputs on the Mainboard

令人欣慰的是，当需要时，你可以很容易地为你的计算机旋转一个替换 PCB。但这种情况远非主流。此外，所有项目，无论开源与否，都面临着部分过时的问题，甚至是 Novena。早在 2019 年，正是因为这个原因，创始人[Bunnie]和[Xobs]在该项目的五周年纪念日发布了一份[终止声明](https://www.crowdsupply.com/sutajio-kosagi/novena/updates/novena-five-year-anniversary)。事实上，诺维娜的可用性甚至持续了五年，这是由于预先购买的关键部件。

早在 2014 年我们就写过[诺维娜，最近](https://hackaday.com/2014/04/02/bunnie-launches-the-novena-open-laptop/)[写了 MNT 改革项目](https://hackaday.com/2021/08/26/hands-on-mnt-reforms-the-laptop/)。你对这些开源笔记本项目有什么想法？你有没有在五年或更长时间后修复的笔记本电脑？请在下面的评论中告诉我们。