# 像 1982 年一样记录数据

> 原文：<https://hackaday.com/2018/07/26/data-logging-like-its-1982/>

如果你想记录电压或电阻，没问题。你可以花 100 美元买一个带蓝牙的万用表，如果你真的很喜欢，你还可以买一个带图形显示的自动记录数值的万用表。事情并不总是这么便宜和容易，但总有办法做到。

早在 80 年代，惠普的台式设备背面就有 GPIB、HP-IB 或 IEEE-488 连接器。这是一个 8 位接口，与允许远程控制测试设备的并行端口没有什么不同。为了很好地展示这实际上是什么样子， [[AkBKukU]发布了一个视频](https://www.youtube.com/watch?v=r2sCBrEOe84)通过 GPIB 将一个旧的台式万用表连接到一台老式电脑上。

用于这一技术革新壮举的计算机是一台[惠普 80 系列](https://en.wikipedia.org/wiki/HP_series_80)，桌面计算机历史上的一个脚注，但它确实有一个定制的 CPU 和 ROM 中的 BASIC。正如你对老式惠普设备的期望，计算机背面有几个插槽用于连接接口盒，包括调制解调器、语音合成器，当然还有可以说 IEEE-488 的 HP-IB 接口。

万用表通过菊花链并行接口连接到计算机后，只需编写一点 BASIC 语言就可以读取电位计和热敏电阻。只要再多加一点代码，这台计算机甚至可以绘制出电阻随时间变化的图表。这是 1982 年的数据记录，这是一个极好的例子，说明我们到底走了多远。

 [https://www.youtube.com/embed/r2sCBrEOe84?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/r2sCBrEOe84?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

