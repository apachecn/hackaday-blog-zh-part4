# 老式米重生为蒸汽朋克时钟

> 原文：<https://hackaday.com/2021/01/03/vintage-meters-reborn-as-steam-punk-clock/>

漫画《工具是英雄》的供应商[Build Comics]从垃圾场拯救了另一对旧的老式模拟仪表[，将它们转换成一个仪表时钟](https://buildcomics.com/meters/meter-clock/)。故事中真正的英雄是他们可信赖的工具——麦克 X 刀，TS 先生的台锯和他可信赖的夹钳，G. Rinder 的角磨机，Weldy 的焊工，尖眼的标记，由 Sandy 的砂光机和 Jiggy 的锯子。正在接受手术的德雷克&戈勒姆(伦敦)电表看起来类似于二战结束后的老式硬件，比如在科学博物馆群发现的这个[费兰蒂安培计](https://collection.sciencemuseumgroup.org.uk/objects/co8409627/ferranti-ammeter-ammeter)，这使得它们至少有 75 年的历史了。

![](img/0bab122e43586133179cd63c1178e866.png)

A small cam is used to engage the DST switch.

正如你所料，转换过程让人想起他们以前的项目。原始的动圈运动被丢弃，指针被连接到一个伺服机构，该伺服机构将作为新的运动。新表盘准备用小时和分钟取代原来的安培标记。为了保留一些原有的魅力，新的表盘有从旧表盘复制的变色和污点。

曾经用来将指针与刻度盘上的零标记对齐的固定螺钉现在被用来启动一个微型开关，启动夏令时。另外两个按钮提供了一个方便的界面来调整时间。精确时间信号来自连接到 Arduino 的 DS3231 RTC 模块。一对七段显示器连接到 Arduino，以便更容易设置时间。一块橡木板被金属角形框架包围，被用作安装两个仪表的底座，这样时钟就可以挂在墙上。

如果你想建造一些更复古的仪器，[建造漫画]你有没有盖一个[经典天气显示器](https://hackaday.com/2020/08/08/vintage-gauges-turned-classy-weather-display/)或[植物水分计](https://hackaday.com/2020/08/15/vintage-ammeter-becomes-plant-moisture-gauge/)。

 [https://www.youtube.com/embed/xIpjMHv_k6I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/xIpjMHv_k6I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

