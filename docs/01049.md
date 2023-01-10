# 即使在德国，制造电动滑板车也是合法的

> 原文：<https://hackaday.com/2018/10/23/building-an-electric-scooter-thats-street-legal-even-in-germany/>

有时候，一个成功的项目不仅仅是确保所有的电子在正确的时间处于正确的位置，或者建造一些在自身重量下不会倒塌的东西。许多项目包含了相当数量的社会工程才能算作成功，尤其是那些如果按原计划建造可能会导致逮捕和监禁的项目。这样的项目通常被称为“有趣的项目”

在过去的几个月里，我们一直在跟踪[Bitluni]的 DIY 电动滑板车制造，它一直在跟踪这些东西的通常轨迹——拿一辆无动力滑板车，用 250 W 轮毂电机取代后轮，添加电子稳定控制系统，电池和油门，然后就可以上路了。然而，当他的街道测试与德国法律发生冲突时，事情发生了非常有趣的转变，德国法律将小型电动汽车的时速限制在令人打哈欠的 6 公里。不愿意把自己闷死，Bitluni 找到了一个变通办法:仅由电动机*辅助*的车辆有一个更合理的 25 公里/小时的速度限制。因此，他添加了一个带有陀螺仪和加速度计模块的 Arduino，并编写了一个程序，只在骑手踢了几次踏板车后为车轮提供动力——不需要油门。发动机停了一会儿，需要再推一两下才能重新启动。刹车杆会让马达熄火，就像把滑板车侧着放一样。这是一个相当聪明的设计，虽然它可能无法阻止*警察*的进攻，但你不能说他没有尝试过。

[Bitluni]有相当多的构建，从[软件定义的电视](https://hackaday.com/2018/02/22/software-defined-television-on-an-esp32/)到[糟糕的 3D 扫描仪](https://hackaday.com/2018/07/23/fail-of-the-week-how-not-to-make-a-3d-scanner/)到[精确的酒杯重击](https://hackaday.com/2018/07/31/the-precise-science-of-whacking-a-wine-glass/)。你应该看看他的东西。

 [https://www.youtube.com/embed/QhxD5owuN8g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/QhxD5owuN8g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



谢谢你的提示，[Baldpower]。