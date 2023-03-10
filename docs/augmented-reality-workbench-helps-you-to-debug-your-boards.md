# 增强现实工作台帮助你调试你的电路板

> 原文：<https://hackaday.com/2022/11/18/augmented-reality-workbench-helps-you-to-debug-your-boards/>

无论你的设计技巧有多先进，你都有可能需要花一些时间在你的主板上追踪从组装室回来的 bug。测试和调试 PCB 通常需要在电路板、布局和原理图之间进行大量的交叉检查，即使对于稍微复杂的设计，这也会很快变得令人厌烦。为了让这项任务变得简单一点，华盛顿大学的[Ishan Chatterjee]和他的同事们设计了[增强现实调试工作台](https://dl.acm.org/doi/pdf/10.1145/3526113.3545684)，简称 ARDW。

ARDW 由一个带有防静电垫的实验室工作台、一系列测量仪器和一台 PC 组成。您只需将电路板放在工作台上，在 KiCAD 中打开原理图和布局，然后像往常一样开始测量和调试您的设计，但真正神奇的是，当您在 KiCAD 中选择一个新图标，将原理图和布局导出到 ARDW 系统时。从那时起，您可以选择原理图中的元件，并使它们不仅在布局上高亮显示，而且在您面前的物理电路板上也高亮显示*。这可能是最好的视觉演示，正如团队成员在下面嵌入的视频中所做的那样。*

由于一组跟踪桌子上所有东西运动的摄像机和一台将信息叠加在 PCB 顶部的视频投影仪，实现了组件的真实突出显示。所有这些都支持各种有用的调试功能:例如，有一个选项可以突出显示所有组件上的第一个引脚，从而可以对每个组件的方向进行简单的视觉检查。您可以选择所有不填充(DNP)实例，并立即查看所有高亮显示的凸台是否为空。如果你不确定你在看哪个元件，只要用你的万用表探针指向它，它就会在原理图和布局图上突出显示。由于万用表和 ARDW 软件之间的数字链接，您甚至可以将探针放在网上，并自动记录电压以供将来参考。

除了设计和构建 ARDW，该团队还使用一组人类测试对象进行了可用性研究。他们特别喜欢在拥挤的电路板上快速定位元件的能力，但发现在线测量系统由于其有限的位置精度而有点笨重。因此，未来的工作将集中于提高投影图像的分辨率，并使系统更加紧凑和坚固。所有软件都可以在该项目的 GitHub 页面上免费获得，虽然当前的系统对于业余爱好者来说看起来有点复杂，但我们已经可以想象它是生产环境中的一个有用工具。

这甚至不是第一次将增强现实用于 PCB 调试:我们在 2019 年 Hackaday 超级大会上看到了[一个有点类似的系统](https://hackaday.com/2020/02/05/debugging-pcbs-with-augmented-reality/)。AR 也可以在设计和原型制作阶段派上用场，正如[这个 AR 试验板](https://hackaday.com/2019/05/27/the-augmented-reality-breadboard-of-the-future/)所展示的那样。

 [https://www.youtube.com/embed/RbENbf5WIfc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/RbENbf5WIfc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

