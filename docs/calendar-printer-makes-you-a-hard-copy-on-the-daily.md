# 日历打印机让你每天打印一份

> 原文：<https://hackaday.com/2020/11/29/calendar-printer-makes-you-a-hard-copy-on-the-daily/>

我们很幸运拥有基于云的日历，可以存储我们超忙生活中的所有相关数据，以便随时随地轻松访问。然而，有时当你厌倦了看屏幕时，一份硬拷贝是很好的。本着这种精神， [[lokthelok]生产了一种小巧的设备，可以打印出你每天的日程安排。](https://hackaday.io/project/166659-calendar-printer-useless-edition)

该设备使用一个 ESP32 连接到 WiFi，然后每天查询谷歌应用程序中给定用户的日历详细信息。在获取数据后，它被传送到一台热敏打印机，打印机以 9600 波特的速度串行连接。作为一个转折，[lokthelok]为这个项目制作了两个版本的固件。[主版本](https://github.com/lokthelok/CalendarPrinter/tree/master)简单抓取日历数据，整齐输出。[无用版本](https://github.com/lokthelok/CalendarPrinter/tree/master_useless)走得更远，把约会混在一起，乱序打印。如果你一天什么也没做，它会把剩余的热敏纸卷出来。

这是一个可以成为漂亮的桌面玩具的建筑，尽管我们怀疑过一段时间后扔掉每天的日历会变得令人厌倦。[或者，考虑一个时钟，为你突出显示你即将到来的事件](https://hackaday.com/2018/06/08/calclock-keeps-you-tied-to-the-mast/)。休息后的视频。

 [https://www.youtube.com/embed/wK4V5MEt4_o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/wK4V5MEt4_o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

