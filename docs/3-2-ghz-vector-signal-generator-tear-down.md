# 3.2 GHz 矢量信号发生器拆除

> 原文：<https://hackaday.com/2020/03/17/3-2-ghz-vector-signal-generator-tear-down/>

【信号路径】[钩住了一个花哨的罗德&施瓦茨矢量信号发生器](https://www.youtube.com/watch?v=ocSl8LtqzzM)，它可以达到 3.2 GHz，但遗憾的是它不能正常工作。它上电了，甚至输出了 1 GHz 的信号，但是幅度输出非常错误。有趣的是，输出的相对变化是正确的，只是绝对输出幅度偏离了相当多，并且随着频率而变化。这开启了一个侦探的工作，你可以跟随下面的视频。

该仪器相当高端，即使在自检期间也没有报告任何问题。这意味着所有的内部组件可能都是好的，无论什么是错的，都可能在输出附近。服务手册的框图并不十分有用，特别是考虑到所有的处理部分似乎都工作得很好。

这是一个很好的借口，只要看看这个精心制作的仪器内部。考虑到输出幅度随频率变化，可以很好地推测问题将涉及某个或某些元件，这些元件包含电抗，或者是故意的，或者是由于某种故障模式。

这只义务猫除了给乐器找了一个令人满意的位置之外，似乎没有太多意见。跟踪输出显示，一些快速二极管对功率进行采样，并触发反向功率保护继电器。这些二极管很容易通过光学显微镜透过透明的外壳看到。

事实证明，控制继电器的 MOSFET 总是保持继电器关闭，更换 MOSFET 可以恢复正常操作。我们不认为继电器是电容，但处于关闭位置的微型继电器在这些频率下确实表现出电容。如果它正常开启，输出应该不会衰减。但由于故障 MOSFET 保持开路，它提供了一个电容路径，降低了输出信号的幅度。

我们喜欢打开东西只是因为，但是当我们自己做不到的时候，别人做的视频也差不多。测试设备可能是我们最喜欢的，但是[旧东西](https://hackaday.com/2019/03/29/teardown-of-a-50-year-old-modem/)也很有趣。

 [https://www.youtube.com/embed/ocSl8LtqzzM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ocSl8LtqzzM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

