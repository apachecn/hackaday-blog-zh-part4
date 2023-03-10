# 降临节日历追踪圣诞节前的日子

> 原文：<https://hackaday.com/2018/11/12/advent-calendar-tracks-the-days-until-christmas/>

万圣节结束了，黑客们需要新的点子来进行更多的黑客攻击，他们该怎么办呢？当然是为圣诞节做点什么。这就是[达里奥·布莱滕施泰因]在制作[他的降临节日历](https://imakethings.ch/christmas-calendar/)时所做的，既是一种装饰，也有助于灌输一些圣诞精神。

在 SketchUp 中设计，它是一个安装在干净的胡桃木外壳中的 WS2812 LED 灯条。光线透过 3D 打印的 PETG 盖子扩散，盖子上覆盖着乙烯树脂，勾勒出一天的轮廓。当然，它必须连接到互联网，因此基于 ESP8266 的 WEMOS D1 迷你板从 NTP 服务器获取日期和时间。红色照亮了星期天，紫色照亮了平安夜。

这似乎正是像[vk2zay]这样的黑客在他们一年一度的[降临节电路日历](https://hackaday.com/2014/12/12/2014-advent-calender-of-circuits/)中可以用来获得灵感的东西，在这个日历中，每天都会制作不同的电路，直到圣诞节。