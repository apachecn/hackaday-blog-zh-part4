# 凭借意志力修复一个坏掉的游戏安装程序

> 原文：<https://hackaday.com/2021/10/29/fixing-a-broken-game-installer-by-sheer-force-of-will/>

如今，我们很少在实体媒体上购买游戏。即使在购买旧书时，我们通常也是从网上下载。正如[Slortibort]所发现的，这些旧游戏中的一些还没有被正确地移植到他们的新交付平台上。因此，是时候深入游戏文件[并解决问题了。](https://madeupexplorations.wordpress.com/2021/10/25/heroes-of-might-and-magic-v-hammers-of-bait-and-switch/)

问题中的游戏是基础游戏《英雄无敌 v》的命运之锤扩展包(Slortibort 的合作伙伴从育碧购买了它，并运行了安装程序。然而，安装程序会报告它无法从基本游戏中找到原始文件，并且无法启动。

修复这个问题绝非易事，需要使用[Sexy Installshield Decompiler](https://github.com/tylerapplebaum/setupinxhacking/blob/master/SID/sid.txt)深入安装程序的内部，看看哪里出了问题。最后，它归结为一些注册表项诡计，但[Slortibort]如何到达那里的路线很值得一读。

这是一个很好的例子，说明了将游戏转移到数字发行的一些问题；必须适当注意把它做好。即便如此，你还是有输掉比赛的风险。当然有好处，但总要有所取舍。