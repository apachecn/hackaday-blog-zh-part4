# 照亮通往每个组件的道路

> 原文：<https://hackaday.com/2020/01/26/light-the-way-to-every-component/>

你如何组织你的组件和模块库存？如果一堆难以控制的来自中国的防静电袋和信封被塞进一个纸箱听起来很熟悉，那么你需要[Dimitris Tassopoulos]的帮助。他将零件整理到抽屉中，并创建了一个数据库，然后[通过一个 ESP8266 和一串可寻址 led](https://www.stupid-projects.com/component-database-with-led-indicators/)将其链接起来，以照亮任何给定组件所在的单个抽屉。这是一个天才的想法，正如你在休息时间下面的视频中看到的那样。

幕后是一个位于 SQL 数据库之上的 web 服务器，有一个 PHP 前端。它运行在 Banana Pi 板上，但也可以运行在任何其他类似的 SBC 上。ESP8266 有一个 REST API，当搜索一个组件时，web 服务器连接到该 API，并从该 API 中知道哪个 LED 发光。

LED 灯条不是大多数读者熟悉的那种带子，而是我们可能更习惯于作为圣诞灯的那种灯串。这些 led 灯之间的间距为 100 毫米，便于放置在每个抽屉的后面。结果是一个非常有效的零件库存系统。我们并不完全确定它会完全消除这里的防静电包的潮流，但我们仍然印象深刻。

 [https://www.youtube.com/embed/TJP2OHLnWME?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/TJP2OHLnWME?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

