# 摆动门电机来帮助打开一个巨大的服务器窗口

> 原文：<https://hackaday.com/2022/04/11/swing-gate-motors-come-to-help-for-opening-a-giant-servery-window/>

[马丁·罗伯茨]写信给我们，告诉我们他的公司[海景工作室]负责的一个建筑。创造一个四米宽、能够垂直打开的窗户不是一件容易的事，它必须定制，因为建造这种窗户的当地公司除了铝以外不适合使用任何东西——对于窗户的规模来说是不够的。考虑到玻璃本身的巨大重量、支撑玻璃的结构要求以及要施加的机械载荷，需要进行一些仔细的规划。

首先，这个窗户必须是电动的，因为一般人不可能把它拉起来。由于对现有的线性致动器选择不满意，他们去了一家五金店，发现[一些摆动门致动器](https://www.bunnings.com.au/richmond-automatic-gate-opener-for-double-swing-gates_p3962443)，在车间测试中，它们证明自己能够处理超过要求的重量。事实上，他们能够毫不费力地把马丁抬离地面。

[![](img/b27ff528de9437e631be330f8e4ad6bc.png)](https://hackaday.com/wp-content/uploads/2022/04/servery-window-inner-cropped.jpeg)

Note the jack helping hold the panel in place.

从那里，是时候弄清楚机械部件了——为窗户建造一个足够坚固的框架，焊接框架，弄清楚安装和杠杆的复杂性，测量要处理的负载，并添加气体支柱。[海景工作室]发布的 14 分钟视频很好地涵盖了机械部分的本质，嵌入在下面，所以我们不会重复它。相反，我们的重点是[Martin]在信中与我们分享的 swing gate 硬件重用部分。

摆动门控制器的内置功能，如可调限位开关支持、软启动/停止和可配置的过载/失速保护，证明了它们有助于窗户操作的平稳性和安全性。至于它的自动化部分，他们将电机控制器与众多 Sonoff 设备中的一个连接到一个基于家庭助理的系统中，然后甚至将其与亚马逊 Alexa 集成，同时添加了一个 *2001:太空漫游*复活节彩蛋。换句话说，电动旋转门硬件和这个服务器窗口建设原来是一个完美的匹配对方。

我们欣赏这种独创性，并希望这个故事的精神可以指导其他处于类似情况的黑客，他们的任务是构建超出当地公司工具包范围的东西。[Martin]说他已经能想到这些东西的一些意想不到的应用——一个额外的重型可调工作台或一个高度可调的特大床。限制线性致动器的可用性是一个痛点，以至于[人建造](https://hackaday.com/2018/10/04/homebrew-linear-actuators-put-the-moves-on-this-motion-simulator/)甚至 3D 打印他们自己的，因为负载[大](https://hackaday.com/2022/02/17/building-a-high-capacity-linear-servo-actuator/)和[小](https://hackaday.com/2021/12/25/mini-linear-actuators-from-dvd-drive-parts/)。

 [https://www.youtube.com/embed/Ec6DicLj_3I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Ec6DicLj_3I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

