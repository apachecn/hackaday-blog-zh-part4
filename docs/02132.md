# 每个数字钟都是由模拟元件组成的

> 原文：<https://hackaday.com/2019/02/12/every-digital-clock-is-made-of-analog-components/>

2008 年，斯德哥尔摩的一家艺术工作室发布了 ClockClock，这是一款带有模拟心脏的数字时钟。这个时钟使用 24 个独立的模拟时钟——时针和分针——以数字方式显示时间。世界疯了，Pinterest 炸了，每个人都想要一个数字模拟时钟，直到下一个有趣的项目分散了大众的注意力。

这是十年前，对于一个深入步进电机、计时和 3D 打印部件的项目来说，我们还没有看到一个 DIY 项目将这些工具放在一起，构建一个克隆的时钟。直到现在，那是。受到时钟的启发，他决定制作自己的。

对于塑料位，24 个模拟时钟中的每一个都是由 PLA 打印出来的。到目前为止，这正是我们所期待的。时钟的诀窍是独立地移动每个模拟时钟的时针和分针。这是通过一个双轴——就像一个真正的时钟——和两个步进电机完成的。每个步进电机由每个模拟时钟中的单个 PCB 控制，具有两个 360 步进驱动器、一个双电机驱动器和一个 ATMega328pb 微控制器。作为一个整体，各个模拟时钟由 I2C 控制，由一个“卫星”板作为主控。

虽然这个构建缺少一些细节，特别是如何将手连接到步进电机上，但这是一个令人惊叹的项目。有人终于造出了一个时钟，而且不像原来那样要花上几千美元。你可以看看下面的模拟/数字时钟的一些视频。

 [https://www.youtube.com/embed/MNlFprewN-A?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/MNlFprewN-A?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/6o0vmoWVZDw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/6o0vmoWVZDw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

