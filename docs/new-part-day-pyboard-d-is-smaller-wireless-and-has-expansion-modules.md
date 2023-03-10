# 新零件日:Pyboard D 更小，无线，有扩展模块

> 原文：<https://hackaday.com/2019/03/20/new-part-day-pyboard-d-is-smaller-wireless-and-has-expansion-modules/>

历史上，微控制器有限的计算能力和存储空间意味着软件必须用低级语言编写。近年来，价格低廉的小型芯片变得足够强大，理论上可以运行更高级的语言，这激发了人们将这一理论变为现实的无数努力。当他们的 Kickstarter 资助的 pyboard 与开源软件一起交付时，MicroPython 在很大程度上实现了这一承诺。几年过去了，现在是升级 pyboard 的时候了:D 系列。

当最初的 Kickstarter 还在进行中的时候，我们已经和[Damien George]谈过了。自从推出 pyboard 和发布 MicroPython 源代码以来，我们已经在 ESP8266 和 [BBC micro:bit](https://hackaday.com/2017/12/02/exploring-the-bbc-microbit-software-stack/) 上运行了端口[。软件生态系统持续增长，最近我们关注了](https://hackaday.com/2016/07/21/micropython-on-the-esp8266-kicking-the-tires/) [LittlevGL 图形库](https://hackaday.com/2019/02/28/littlevgl-brings-gui-tools-to-micropython/)。但是，仅仅因为软件方面发生的所有浮华的动作并不意味着硬件方面一直停滞不前。

Pyboard-D 从原始 Pyboard 的 STM32F4 升级到更强大的 STM32F7 芯片。见证了 MicroPython 在联网宠儿 ESP8266 和 ESP32 上的流行，将有一个 pyboard D 变体，板载 Murata 1DX，用于 WiFi 和蓝牙连接。新的 pyboard 将非常紧凑，边缘连接有限，因此需要一个微调连接器来引出所有引脚。为了使新的 pyboard 回到它的教育和修补根源，一个分线板将把这些引脚分散在一个试验板友好的形状因子中。这些分线板还可以放置小的(12 毫米 x 12 毫米)瓷砖，以增加个人特色。

 [![Pyboard D breakout boards](img/e2000dfc2926d42623209eb4b04ecdef.png "Pyboard D breakout boards")](https://i0.wp.com/hackaday.com/wp-content/uploads/2019/03/pyboard-d-breakout-boards.jpg?ssl=1)  [![Pyboard D breakout board with tiles](img/eebb873c62d5c6a148e9fcd34d0c54a7.png "Pyboard D breakout board with tiles")](https://i0.wp.com/hackaday.com/wp-content/uploads/2019/03/pyboard-d-breakout-board-with-tiles.jpg?ssl=1) 

无线 pyboard D 显然会邀请运行 MicroPython 的 ESP32 进行比较测试，其硬件扩展瓦片会邀请与 Adafruit 的 Wings 进行比较。一旦它们被广泛使用，我们就能得到它们，看看它们的进展会很有趣。如果你在 FOSDEM 2019 上选择了一个更早的版本[，我们邀请你在评论中分享你的经验。](https://fosdem.org/2019/schedule/event/microcontrollers_python/)

[via [Adafruit 博客](https://blog.adafruit.com/2019/03/11/micropython-pyboard-d-series-update-micropython-micropython/)