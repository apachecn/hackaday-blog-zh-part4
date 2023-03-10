# 不要把你的 3D 打印机调到中间的 C 档

> 原文：<https://hackaday.com/2022/04/03/3d-printering-dont-tune-to-a-middle-c-after-all/>

![](img/181350a227b2d0536178e708f1c92f11.png)

Layer shift caused by the belt being way too loose.

3D 打印机皮带张力似乎是一件简单的事情——你设置张力，然后不时检查它是否良好。如果它变得很松，那么牙齿可能会滑动，你会得到一些转移，破坏它，但这是一个简单的修复。但是，我们听到你问，你如何确定什么是正确的张力？嗯，[这里有一个视频，展示了一些测量技术和对一台典型的 3D 打印机的分析](https://www.youtube.com/watch?v=zoKmmT0a7jk)(视频，嵌入在下面)，使用的只是一套行李秤。一个简单的理论认为，更紧的皮带张力会导致步进电机轴承上的径向负载增加，这又会由于摩擦而导致电机温度升高。在其中一条皮带上设置几个张力值后，注意到张力值在该范围的上限，导致测得的温度增加 2 摄氏度，并且噪音大幅增加。这对发动机不好。

查看典型 NEMA17 步进电机的规格表，显示最大工作径向力的值为 28N，因此简单地说，导致负载超过该值的张力值只会缩短电机寿命。即使设置非常宽松，打印质量也不会发生明显变化，直到皮带松弛到足以使轴运动明显滞后于电机输入。

正如《迷失科技》所言，也许那句将皮带张力调到“中间 C”的老话可能真的太紧了，给你带来的问题比它解决的问题还多？

显然，这些年来我们已经报道了许多 3D 打印机黑客，就像这个[巨大的皮带驱动打印机](https://hackaday.com/2018/01/04/huge-3d-printer-ditches-lead-screw-for-belt-driven-z-axis/)，只是要小心，即使是像[皮带夹这样简单的东西也会因为糟糕的设计而出错](https://hackaday.com/2018/12/16/how-not-to-design-a-3d-printed-belt-clamp/)，最后，当我们考虑皮带驱动时，这里有一个[很酷的皮带驱动挤压机](https://hackaday.com/2021/12/23/back-to-back-belts-drive-filament-in-this-unique-extruder-design/)供我们思考。

 [https://www.youtube.com/embed/zoKmmT0a7jk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/zoKmmT0a7jk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[赞]的提示！