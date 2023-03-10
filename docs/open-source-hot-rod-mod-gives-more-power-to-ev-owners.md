# 开源的飞车手罗德 Mod 赋予电动车车主更多的权力

> 原文：<https://hackaday.com/2021/09/20/open-source-hot-rod-mod-gives-more-power-to-ev-owners/>

见见[丹尼尔·斯特]。[丹尼尔]自称是石油大亨。换句话说，他是一个热罗德谁不能离开不够好。仅仅因为他开着一辆 2012 款尼桑 Leaf 并不意味着他不寻求更多的刺激。已经升级了电池，【Daniel】将注意力转向了升级 80KW 逆变器。不仅[丹尼尔]成功了，[而且这项工作已经被记录了下来](https://youtu.be/Of2vCYgblY4)并且[在 GitHub](https://github.com/dalathegreat/Nissan-LEAF-Inverter-Upgrade) 上提供了开源代码。[丹尼尔]的部分使命是开放封闭的生态系统，让普通人也能接触到电动汽车的改装和维修。

为了获得额外的 50 马力，[Daniel]可以从 2018 年或更新的 Leaf 中更换 110 千瓦的动力传动系统，但选择了一种更便宜的仅更换 110 千瓦逆变器的路线。通过只更换逆变器，其他人可以更经济地进行改装。[Daniel]通过在逆变器中设置旋转变压器校正值，专业地记录了新型 110KW 逆变器如何与现有电机匹配。

![Swapping Connectors for the new Inverter](img/d0f56e3af91c0b8d4752ee9668729571.png)

Not for the faint of heart, the inverter swap requires changing connectors to a later style.

切割一辆仍在付款的汽车的线束是一项只有最专业的改装商才能做的工作，但 2012 年至 2018 年间连接器的变化使之成为必要。唯一需要的工具是钢丝钳、烙铁、热收缩管，也许还有一些液体勇气。

虽然黑客攻击成功了，但最初并没有获得任何性能提升，因为去往逆变器的 CAN 总线信号从未告诉它提供超过原始 80KW 的功率。攻击中的 CAN 总线人是通过添加一个 CAN 网桥设备来监听 CAN 总线上的流量，并根据[Daniel]的意愿进行弯曲。通过将 KW 信号乘以 1.3，80KW 信号变成了 110KW，从而实现了全速前进！在 0-100 公里/小时的时间里可以看到出色的增益，但[丹尼尔]还没有完成。他的下一步将是安装一个 160 千瓦的逆变器，让它更加疯狂。

一定要看休息下面的介绍视频。你可能也会对我们之前报道过的日产 Leaf 黑客事件感兴趣，比如[改装快速充电端口](https://hackaday.com/2021/06/28/retrofitting-fast-charging-to-a-nissan-leaf-ev/)、[从残骸中回收电池](https://hackaday.com/2015/04/29/jay-turns-over-a-new-leaf-scores-batteries/)，以及部分解决严重充电缺陷的。

 [https://www.youtube.com/embed/Of2vCYgblY4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Of2vCYgblY4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

