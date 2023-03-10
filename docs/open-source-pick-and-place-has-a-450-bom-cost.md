# 开源的“取放”有 450 美元的 BOM 成本

> 原文：<https://hackaday.com/2020/05/11/open-source-pick-and-place-has-a-450-bom-cost/>

让你的头发花白和抽筋的手休息一下，从表面贴装元件填充板。这是拾放机的工作，多年来，印刷电路板组装(PCBA)行业的这些工具越来越接近家庭商店的现实；有些型号的价格跌到了 1 万美元以下。但是如果你不是专业地做它，那些仍然是 unobtanium。

另一方面，这个项目的成本可以解释为一个项目本身。你不是在购买一个 450 美元的商店工具，你是在购买材料来[追逐建造一个开源取放机器的狂热梦想](https://github.com/sphawes/index)。这里有两个主要部分，一个 X/Y/Z 机床，它也可以旋转基于真空的零件拾取器，以及卷出要放置的元件的进料器。所有这些都在起作用，但在它成为一台“一劳永逸”的机器之前，还有很长的路要走。

[![](img/c07a3fbb937316edc424185ca1bb74ce.png)](https://hackaday.com/wp-content/uploads/2020/05/component-feeder-index-open-source-pick-and-place-machine.jpg) 橡胶以两种方式接触抓放机:送料器和光学放置。喂食器是[斯蒂芬·霍斯]做了大量工作的地方，[所有这些都在他一月份开始的视频系列](https://www.youtube.com/watch?v=dAFleHaPjEY&list=PLIeJXmcg1baLBz3x0nCDqkYpKs2IWGHk4)中展示。PCB 和 3D 打印的堆叠悬挂在机架组件的前轨上，可根据胶带宽度进行调整，并使用有趣的 PCB 编码器轮和蜗轮来微调进料。[Stephen 的]主控制板是和 Arduino Mega 的斜坡保护板，运行定制版本的 Marlin，可以与多达 32 个这样的馈电线一起工作。

到目前为止，看起来他还没有解决视觉系统，尽管[材料清单](https://docs.google.com/spreadsheets/d/1N7jMZ2upi8-9_jjJnl2xC9bYtZuE1wX5Qzoa-qs21eY/edit#gid=476120456)确实包括“向下摄像头”，证实这是一个计划中的功能。视觉在商业产品中至关重要，至少有一个向下的摄像头用于精确定位电路板，通常还有一个向上的摄像头用于确保元件的位置和方向(如果不是每个目的都有多个摄像头的话)。没有这些，机器将是航位推算，这可能导致漂移超过电路板的大小和放置运行的持续时间以及轴向不对准。然而，添加视觉不应该是一项地面工作，因为[斯蒂芬]选择使用 [OpenPnP](https://github.com/openpnp/openpnp) 来驱动机器，而那个项目[已经有了视觉支持](https://github.com/openpnp/openpnp/wiki/Camera-Lens-Calibration)。与馈线的复杂性相比，这将更容易添加。

[Stephen]承认仍有许多工作要做，他很乐意在馈线设计的性能方面得到帮助，并在完善的道路上充实功能。尽管我们怀疑，就像在 3D 打印机的早期一样，像这样的项目永远不会真正完成。至少这将使他的下一批发光二极管更容易制造。

 [https://www.youtube.com/embed/GtZcnIEi710?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/GtZcnIEi710?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



【感谢尼尔斯！]