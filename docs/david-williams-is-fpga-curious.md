# 大卫·威廉姆斯“对 FPGA 很好奇”

> 原文：<https://hackaday.com/2019/12/06/david-williams-is-fpga-curious/>

如果你没有注意到，我们在今年的超级大会上有一个 FPGA 主题。为什么？因为开源 FPGA 工具链正在成熟，也因为黑客(和学者)目前正在解决的许多问题已经变得足够复杂，值得使用它们。一个恰当的例子是:大卫·威廉姆斯是一名大学教授，他只想建立一个四足机器人项目。每条腿都有一套复杂的电机、电机驱动器、传感器和其他反馈机制。集中所有这些数据给机器人的网络带来了真正的压力，而且由于设备太多，微控制器耗尽了 GPIOs。用他的话说，这让他变得“对 FPGA 好奇”。

[![](img/72068a56d3c6b9a48ccf01231e6ceddd.png)](https://hackaday.com/wp-content/uploads/2019/12/cropped_shot_2019-12-05-200240.png) 如果你正在寻找一份关于开源 FPGAs 最新技术的介绍，这正是你要找的。David 涵盖了所有内容，从硬件描述语言的鸟瞰图，到整个基于 Yosys 的开源工具链，甚至到将软 CPU 嵌入 FPGA 结构。这只是前 18 分钟。([幻灯片](https://davidthings.github.io/spokefpga/hackaday_slides_2019_11_12/#/)供您欣赏，您可以观看插播在休息时间下面的讲话。)

演讲的后半部分更多的是他的个人经验和建议，基于他过去一年左右从 FPGA 新手到自己的机器人大师的经历。他强调了 FPGA 中的软 CPU 相对于预烘焙微控制器解决方案的多功能性。有了微控制器，你可以将所有外设内置到芯片中，但有了 FPGA，你就可以*编写自己的*外设。想要一个类似 SPI 的 10 线总线？把它编码好。您需要的外围设备简单或复杂都可以。

在硬件方面，大卫吹捧 PMOD 标准([合我们心意](https://hackaday.com/2016/11/09/my-life-in-the-connector-zoo/)！)并指出 PMOD 兼容设备的大生态。采用插件解决方案还意味着您的工程工作减少到构建一个载板，该载板可以容纳您选择的 FPGA 大脑板，并将其与一堆 PMODs 接口。很难有比这更简单的了。

David 对软件层也非常感兴趣，并鼓励在设计中重用 Verilog 代码。为此，他编写了自己的总线和互连标准，以及一些做缓冲数据、处理视频等工作的模块。虽然我们可能会选择开源标准 [WISHBONE 互连架构](https://opencores.org/howto/wishbone)，但 David 将一堆可能的信号捆绑在一起，称之为“管道”。与 WISHBONE 相比，David 的设计做出了一些明智的选择，从而大大简化了互连。他有[的代码来配合这一切](https://davidthings.github.io/spokefpga/code_library#code-library)，所以如果你有兴趣的话可以看看。我们只是推测，但是如果您编写了一个到 WISHBONE 连接器的“管道”,那么您将拥有两个世界中最好的东西。

[![](img/85d5573c515da1ee587f1f42a88b68ad.png)](https://hackaday.com/wp-content/uploads/2019/12/2019-Hackaday-Superconference-Badge-running-a-camera-hack-by-David-Williams_thumbnail.png) 终于，大卫不仅仅是吹口哨的迪克西。他拿起一台摄像机，通过盒式插槽将其插入他的 Supercon 徽章，并让它实时显示视频，所有这些都使用他之前编写的代码片段，并简单地与他的“管道”连接在一起。一个很棒的演示很有说服力。

总之，David 的演讲很好地总结了开源 FPGAs 目前的发展状况。无论您是初次尝试，还是技术一般的 FPGA 开发人员，这里都有适合您的东西。如果有什么不同的话，大卫呼吁结束围绕 FPGAs 的五十年的保密和知识产权囤积是一个我们可以支持的战斗口号。我们现在已经有了工具，硬件也变得便宜和容易获得。如果你正在寻找一个开始的地方，尝试来自 Supercon 的[自导式 FPGA 研讨会](http://bit.ly/fpga_badge_workshop)，然后可能是 Al Williams 的 [FPGA 训练营](https://hackaday.io/project/159720-fpga-bootcamp-0)。黑客 FPGA 革命的时机已经成熟。拿起武器。

 [https://www.youtube.com/embed/ME_e06ApxJA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ME_e06ApxJA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

