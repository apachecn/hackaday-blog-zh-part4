# 在家加工 PCB 的指南

> 原文：<https://hackaday.com/2022/02/09/a-guide-to-milling-pcbs-at-home/>

如果你一直关注各种复古真空管项目，你可能会遇到[usagie electric]又名[David]的各种 PCB，他在自己的 Bridgeport EZ-Track 3 轴铣床上制作这些 PCBs 用他的话说，对于这项工作来说，尺寸太大了。在最近的一段视频中，[David]向我们展示了制作 PCB 样品的步骤，介绍了他的工作流程中的各种工具和程序。他指出，这些是他使用的工具，但无论使用什么工具，总体过程都应该是相似的。

*   验证逻辑设计的 Logisim
*   TINA-TI ，德州仪器的 TINA SPICE 模拟器版本
*   [设计用于原理图输入和 PCB 布局的 Spark PCB](https://en.wikipedia.org/wiki/DesignSpark_PCB)
*   [FlatCAM](http://flatcam.org) ，计算机辅助 PCB 制造工具

在这个视频中，[David]用四个真空管加上一个七段 VFD 管制作了一个半加法器电路，以显示合并的和与进位输出。瞬时开关用于产生两个加数。利用这个例子，他继续设计、模拟、构建和演示一个工作电路板。我们喜欢他使用加工过的插脚插座插件直接在电路板上构建真空管插座。

这个过程并不适合每个人。首先，布里奇波特轧机是一个很好的尺寸，和沉重的工具。也就是说，这些程序应该很好地适应其他铣床和雕刻机。我们应该指出，[大卫]主要是为真空管制造电路板，那里的电路走线宽度和间距都很大。如果你打算为 273 针 PGA 芯片制作家用 PCB，这种技术不适合你。

似乎[大卫]的真空管印刷电路板大部分是单面的，这是合理的。他们到处用电线连接来跳过痕迹。使这一过程适应双面 PCB 是可行的，但更复杂。你是在实验室铣双面板吗？如果是这样，请在下面的评论中告诉我们。

 [https://www.youtube.com/embed/AB84_vbH_e8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/AB84_vbH_e8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

