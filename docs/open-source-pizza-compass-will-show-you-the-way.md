# 开源披萨指南针会给你指路

> 原文：<https://hackaday.com/2021/04/28/open-source-pizza-compass-will-show-you-the-way/>

在《加勒比海盗》中，杰克·斯派洛船长有一个被施了魔法的罗盘，它能指出持有者一生中最想要的东西。[由【乔·格兰德】创造的披萨罗盘基本上是同样的东西](http://www.grandideastudio.com/pizza-compass/)，除了它由粒子硼而不是伏都教咒语驱动。尽管取决于谁拿着这个东西，我们想象它们甚至指向同一个方向。

[乔]被 *Wired* 指派在三周内设计并制作披萨指南针，这个过程记录在下面的视频中。作为 Badgelife 的杰出人物，他的最终产品看起来比任何商业产品都更有吸引力。除了安装在手持 PCB 背面的粒子硼之外，还有一个 GlobalTop PA6H GPS 模块，一个 LSM303DLHC 罗盘和八个与丝网罗盘上的点对应的新像素。

[![](img/54882ba0e3fcd5878fb39a9c5afbca12.png)](https://hackaday.com/wp-content/uploads/2021/04/pizzacompass_detail.jpg)

From prototype to final product.

使用该设备很简单，只需按下按钮，然后走来走去，试图保持最顶端的 LED 灯亮着。在幕后，硼正在拉下谷歌 API 报告的最近的比萨饼店的坐标，并将其与用户当前的 GPS 位置进行比较。在实践中，这意味着披萨罗盘并不关心街道或建筑等细微差别，因此由用户来决定如何最好地保持在理想的方向上。因此，如果你想要新鲜的切片，不只是按照一些转弯方向，还有一些适当的导航。

如果你不喜欢比萨饼，你可以重新编程指南针指向任何你希望的有价值的资源。正如视频结尾所解释的，[Joe]希望这是一个开源项目，因此它可以很容易地适应社区的不同任务。不过说实话，如果你不喜欢披萨，那就很奇怪了。

事实上，我们在过去报道过一个非常类似的设备[，它会将用户指向最近的白色城堡或五个家伙](https://hackaday.com/2018/11/17/meat-seeking-raspberry-pi-leads-you-to-flavortown/)，但是出于对该项目的尊重，披萨罗盘处于另一个联盟。当你在团队中拥有【乔·格兰德】的[天赋和经验，即使是最平凡的小玩意最终看起来也像一件艺术品](https://hackaday.com/2019/08/09/def-con-27-the-badge-talk-or-that-one-time-joe-grand-sourced-30000-gemstones/)

 [https://www.youtube.com/embed/aY0OtOy6lcE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/aY0OtOy6lcE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

