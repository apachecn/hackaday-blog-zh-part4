# 这个 GPS 速度计挂在你的车把上

> 原文：<https://hackaday.com/2019/04/25/this-gps-speedometer-hangs-off-your-handlebars/>

如果你可以骑一辆没有车把的自行车，没有车把，没有车把，你可以做任何事情。你可以拆开一个遥控器，也几乎可以把它装回去。你可以监听两米中继器，你可以[建立一个 GPS 模块速度表](https://www.youtube.com/watch?v=AtdGkleeYi4)。这就是杰里米·库克(Jeremy Cook)所做的，只用了几个零件，一点 3D 设计，和一些方便的拉链带把它固定在车把上，车把。

这个版本的电子设备相对简单，基于 Arduino Pro Mini，因为这是你能找到的最小的开发板。这是一个 LiPo，一个 LiPo 充电电路，一个 GPS 模块和一个 RGB LED。代码从 GPS 模块获得一些数据，并计算出速度。然后，这被转换成一种颜色——红色、黄色或绿色，取决于你是静止的、低于 5 公里/小时还是高于 5 公里/小时。

所有这些电子设备都被塞进一个 3D 打印的外壳中。外壳的大部分是黑色印刷的，半透明的顶部是 LED 的巨大漫射体。仅仅两个拉链带把这个 GPS 速度计固定在车把上，从下面的视频来看，一切看起来都很棒。GPS 模块起初确实需要一些时间来获取数据，但这是断电几天的 GPS 单元的常见问题。要是有人做一个 GPS 模块可以不用节拍器保持时间[，不用节拍器](https://www.youtube.com/watch?v=HLUX0y4EptA)就好了。

 [https://www.youtube.com/embed/AtdGkleeYi4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/AtdGkleeYi4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

