# 客观的酒店和绩效评估很难

> 原文：<https://hackaday.com/2022/08/25/objective-hotend-performance-measurement-is-hard/>

评估 3D 打印机和组件升级的性能比乍看起来更困难，主观观察可能会导致错误的结论。为了客观地确定不同 FDM 3D 打印机的最大流速，【mirage c】[正在开发一个强大的测试标准，该标准不仅仅由视觉观察支持](https://www.youtube.com/watch?v=02aufZ1OVvQ)。

定义最大流速阈值并不简单。一种常见的方法是运行测试打印，同时稍微增加每一层的流速，并目测判断最后一个可接受的层。随着时间的推移，很容易遗漏错误，或者无意识地与观察结果不一致。[MirageC]想要用测量来支持观察结果。为此，他用编码器轮测量细丝的真实进料速度，用测压元件测量挤压机上细丝的背压。鲍登管有助于将挤出机与移动的打印头的振动隔离。

经过大量测试后，[MirageC]确定数值阈值是期望流量和实际流量之间的特定偏差百分比。在 230°C 以上的温度下，[MirageC]发现，对于一种特定的 PLA 长丝，最后一层视觉上可接受的涂层始终在 5.75%左右的流速偏差。这并不意味着 5.75%将是所有细丝和喷嘴尺寸的神奇数字，但它确实提供了一个可测量的参数来支持视觉观察。

在一个充满问题的产品评论的世界里，这种对客观性的执着是一股清新的空气。如果你想升级你的 3D 打印机，那么[MirageC]的测试将是一个很好的信息来源。

 [https://www.youtube.com/embed/02aufZ1OVvQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/02aufZ1OVvQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



我们已经介绍了一些提高酒店流量的技巧，包括给[火山喷嘴](https://hackaday.com/2022/08/07/want-faster-extrusion-but-dont-have-a-volcano-nuts/)添加螺母，给喷嘴内部添加[铜线。](https://hackaday.com/2021/11/23/diy-high-flow-3d-printing-nozzle/)