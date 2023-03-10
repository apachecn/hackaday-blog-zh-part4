# 微型柏林时钟复制品也可以计算秒数

> 原文：<https://hackaday.com/2022/07/05/tiny-berlin-clock-replica-also-counts-seconds/>

如果你是一个钟表爱好者，并且曾经访问过柏林，你可能对 Budapester Straß上的柏林钟很熟悉:一个由黄色和橙色灯组成的极简设计，以 5 为基数的数字系统显示时间。自 1975 年以来，这座钟一直在向少数能看懂它的人报时，它只是这座城市里能找到的几座不寻常的钟之一。

柏林居民[jjoeff]决定制作一个微型复制品，恰当地称为柏林 Uhr Nano，以便在一天中的任何时候观看这种不寻常的展示。围绕 Wemos D1 迷你，它连接到 WiFi，以同步其内部时钟到 NTP 时间服务器。然后，它驱动一个包含 39 个 WS2812 LEDs 的定制 PCB，以正确的格式显示时间。但与最初的不同，它还包括一个完整的计数器来显示秒数；较大的时钟只闪烁一盏灯来显示秒的流逝。

它由 500 毫安的锂电池供电，只需将一根带子穿过 PCB 上的插槽，就可以变成手表。除了显示时间之外，它没有任何调节按钮或其他功能，与原来的功能相同，只是采用了便携式格式。我们之前已经见过[一个稍大的木制柏林时钟复制品](https://hackaday.com/2015/12/01/light-duty-timekeeping-arduino-berlin-clock/)，以及[一个圆形的](https://hackaday.com/2020/05/14/passing-the-time-by-reading-the-time/)，它使用了相同的 base-5 编码方案。

 [https://www.youtube.com/embed/jFn_5Lrx8zE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/jFn_5Lrx8zE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

