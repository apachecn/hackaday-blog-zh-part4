# 探测电动车电池信息的 CAN 总线

> 原文：<https://hackaday.com/2022/07/27/probing-can-bus-for-ev-battery-info/>

CAN 总线(和 OBD-II)在汽车中的广泛采用在很大程度上是一种标准化日益复杂的发动机维护及其满足现代排放标准需求的方式。虽然表面上听起来有点枯燥，但三十年来，这种通信总线在几乎所有乘用车中的存在和标准化导致了一些有趣的副作用，比如它在这个项目中的用法[显示了一些关于电动汽车电池的额外信息](https://pierremuth.wordpress.com/2022/07/24/electric-car-battery-dashboard-gauge/)。

关于它没有太多的信息，但它是一个很好的概念证明，证明了一些可以在车辆中打开的东西。这一构建基于雪铁龙 C-Zero(本质上只是一款重新注册的三菱 i-MiEV)，并使用 CAN 总线上的信息来显示有关电池充电状态的特定信息，否则这些信息不会显示在汽车显示器上。它还包括一个专门用于这一目的的新的辅助显示器的构建，该构建足够圆滑，看起来像是汽车的标准部件。

虽然肯定还有其他(或许更简单)与 CAN 总线接口的方式，但这种方式使用现成的电子器件，如 Arduino 兼容的微控制器，是永久性安装的，并且有一个我们非常喜欢的定制外壳。如果你刚刚开始探索你自己汽车的 CAN 总线，有一些[优秀的工具可供](https://hackaday.com/2019/07/22/developing-an-automatic-tool-for-can-bus-hacking/)检验。

感谢[詹姆斯]的提示！

 [https://www.youtube.com/embed/ng3ovxGFdM4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ng3ovxGFdM4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

