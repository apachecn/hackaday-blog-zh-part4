# 装饰灯箱让你猜时间

> 原文：<https://hackaday.com/2018/10/19/decorative-light-box-lets-you-guess-the-time/>

通过使用太阳的当前位置来显示时间并没有什么革命性的变化——尽管我们可以假设这很可能是古代的“生活帮”。另一方面，*通过使用太阳的当前位置来显示*时间是【Rich Nelson】创造[日循环时钟](https://www.youtube.com/watch?v=Sy7FVV2LId8)的灵感来源，这是一个费城天际线的变色灯箱，实时模拟一个完整的昼夜循环——包括伺服控制的太阳和月亮。

在其核心，时钟使用一个带有实时时钟模块的 Arduino 和 TimeLord 库来确定日出和日落时间，以及基于给定位置的当前月相。太阳和月亮显示在一个 1.44 英寸的液晶显示屏上，这个显示屏是数字钟的两倍，以防你需要更准确的时间。正如你在链接视频中看到的，在这个项目中，[Rich]通常会以他自己的方式规划和关注细节，从而产生一个令人印象深刻的干净建筑，肯定值得作为礼物送给他的兄弟。如果你想为自己建造一个，GitHub 上有 Arduino 源代码和所有的 T2 机械部件。

一个有趣的下一次迭代可能是增加互联网连接，将当前的天气情况混合到光的行为中——这不是我们第一次看到用光来代表[天气。当然，](https://hackaday.com/2018/01/14/pi-weather-lamp-puts-lava-lamps-to-shame/)[模拟北极光](https://hackaday.com/2015/08/06/arduino-borealis-combines-leds-and-paint/)也是一个选择。

 [https://www.youtube.com/embed/Sy7FVV2LId8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Sy7FVV2LId8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

