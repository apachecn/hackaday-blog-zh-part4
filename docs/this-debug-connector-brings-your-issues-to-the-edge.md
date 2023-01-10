# 这个调试连接器将您的问题带到了边缘

> 原文：<https://hackaday.com/2020/11/28/this-debug-connector-brings-your-issues-to-the-edge/>

给定一个带有 ARM 处理器的未知 PCBA，它很可能会有标准的 10 针 0.05”或 20 针 0.1”调试连接器。这种不常见的通用性对于探索型黑客来说是一个福音，但是在设计电路板时，这种接头需要电路板空间，并且需要安装更多的元件来插入。字面上命名为[的 Debug Edge 标准](https://debug-edge.io/)是一个新的自由尝试来弥补这种不便。

“Debug Edge”这个名字说明了一切。这是一个调试，边缘连接器。PCBA 边缘的一种连接器，用于中断调试信号。卡边缘连接器并不新鲜，但它们通常要么将一个 PCBA 垂直插入另一个(如在 PCI 卡中)，要么平行放置它们(如在迷你 PCIe 卡或 m.2 SSD 中)。调试连接器更像是 PCBA 对接接头。

它利用了一个特殊系列的 [AVX 开口卡边缘连接器](https://www.avx.com/products/connectors/board-to-board/open-ended-card-edge-00-9159/)，设计用于拼接用于端到端照明的长矩形印刷电路板。这些产品的单批起价低至 0.85 美元(此处所示设计的零件号为 009159010061916)。DebugEdge 标准的设想是，该连接器沿着目标设备的边缘暴露，然后“拼接”到用于目标电源和调试的调试连接器中。

现在 debugger 主要作为一个标准存在，一组 KiCAD 足迹，以及 OSHPark 上的原型适配器板([调试器端](https://oshpark.com/shared_projects/NC93Zd5a)，[目标端](https://oshpark.com/shared_projects/Z0EhBlPD))。使用它的设备将集成目标端，开发人员将使用调试器端进行连接。该标准规定了 4、6、8 和 10 针种类(映射到可用连接器的尺寸，以上数字中的“010”规定了针数),提供了更高的连接级别，达到标准 10 针臂连接器的完全 1:1 映射。请记住，连接器是双面的，所以 4 针版本是一个微小的 4 毫米 x 4.5mm 毫米！我们很高兴看到这种蠕虫进入一两个小项目。

我们之前已经见过很多[无部件调试](https://hackaday.com/2017/08/04/pogo-pin-serial-adapter-thing/)和[编程连接器](https://hackaday.com/2016/12/20/jump-into-pogo/)。有喜欢的吗？请在评论中告诉我们！