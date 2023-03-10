# 不是总线的总线:破解 PCI Express 的乐趣

> 原文：<https://hackaday.com/2021/02/03/the-bus-thats-not-a-bus-the-joys-of-hacking-pci-express/>

PCI Express (PCIe)自 2003 年问世以来，一直是扩展卡和高速外部设备的主要数据互连设备。PCIe 的有趣之处还在于，它用串行链路取代了广泛使用的并行总线。PCIe 使用直接连接到 PCIe 端点的根联合体，而不是使用公共介质(迹线)连接多个设备的总线。

这类似于以太网最初使用总线配置，具有公共主干(同轴电缆)，但现代以太网(从 90 年代开始)转向点对点配置，由交换机辅助，允许在连接的点(设备)之间进行动态切换。PCIe 还提供添加交换机的能力，允许一个以上的 PCIe 端点(设备或设备的一部分)共享 PCIe 链路(称为“通道”)。

与 ISA 或 PCI 相比，这种从并行总线到串行链路的变化大大简化了拓扑结构，在 ISA 或 PCI 中，通信时间必须与总线上的其他 PCI 设备共享，并且只能进行半双工操作。捆绑多个通道以向特定端口或设备提供更少或更多带宽的能力意味着不需要专门的图形卡插槽，例如使用具有 16 个通道的 x16 PCIe 插槽。不过，这意味着我们使用的串行链路工作在数 GHz，必须以差分对的形式实现，以保护信号完整性。

这一切似乎有点超出了一般业余爱好者的能力，但仍然有办法享受 PCIe 黑客的乐趣，即使它们不涉及 7400 逻辑芯片的试验和用 100 MHz 预算示波器调试，就像 ISA 总线一样。

## 高时钟需要差分对

[PCIe](https://en.wikipedia.org/wiki/PCI_Express) 与 32 位 PCI 相比，1.0 版将最大传输速率从 133 MB/s 提高到 250 MB/s。如果使用四通道(约 1，064 MB/s)，这与 PCI-X 64 位连接(133 MHz)大致相同。这里，PCIe 通道的时钟频率为 2.5 GHz，每个通道内都有差分信号发送/接收对，用于全双工操作。

如今，随着越来越多的系统升级，PCIe 4 正慢慢被采用。这个版本的标准运行在 16 GHz，已经发布的 PCIe 版本 5 的时钟频率为 32 GHz。虽然这意味着大量的带宽(对于 x16 PCIe 4 链路来说超过 31 GB/s)，但它也伴随着产生这些快速转换、保持这些数据链路完整以及保持数据完整超过几毫米的成本。这需要一些有趣的技术，主要是差分信号和 SerDes。

[![](img/83f5c139fb28460eb3559fd89a08bd10.png)](https://hackaday.com/wp-content/uploads/2020/02/differential_signaling-themed.png)

Basic visualization of how differential signaling works.

[差分信号](https://en.wikipedia.org/wiki/Differential_signaling)通常用于许多通信协议，包括 RS-422、IEA-485、以太网(通过双绞线)、DisplayPort、HDMI 和 USB，以及 PCB，其中以太网 PHY 和磁性元件之间的连接采用差分对。线对的每一侧传导相同的信号，只是其中一侧具有反相的信号。两端具有相同的阻抗，并且类似地受到环境中的(电磁)噪声的影响。因此，当接收器将反转的信号翻转回来并将两个信号合并时，信号中的噪声将在一侧反转(负幅度)，从而抵消非反转侧的噪声。

这些协议向更低信号电压(以 [LVDS](https://en.wikipedia.org/wiki/Low-voltage_differential_signaling) 的形式)的发展以及时钟速度的提高使得差分对的使用变得至关重要。幸运的是，在定制的 PCB 设计上实现起来并不困难。通用 EDA 工具(包括 KiCad、Autodesk Eagle 和 Altium)提供了使差分对布线成为半自动事务的功能，使得确保差分对中的走线具有相同长度的艰巨工作变得更加容易。

## 鱼与熊掌兼得:SerDes

[![](img/dd0c5224e4594d9407dfa6c53dc7acd4.png)](https://hackaday.com/wp-content/uploads/2020/12/20050602_genesys2.gif)

Schematic diagram of a SerDes link.

串行器/解串器( [SerDes](https://en.wikipedia.org/wiki/SerDes) )是用于在串行数据和并行接口之间进行转换的功能块。在 FPGA 或通信 ASIC 内部，数据通常在并行接口上传输，并行数据被传入 SerDes 模块，在那里被[序列化以进行传输](https://www.design-reuse.com/articles/10541/multi-gigabit-serdes-the-cornerstone-of-high-speed-serial-interconnects.html)，反之亦然。PCIe PMA(物理媒体附件)层是位于 PCIe 的 SerDes 所在的[协议物理层](https://en.wikipedia.org/wiki/PCI_Express#Physical_layer)的一部分。具体的 SerDes 实现因 ASIC 供应商而异，但它们的基本功能通常是相同的。

当谈到生产自己的 PCIe 硬件时，一个简单的入门方法是使用带 SerDes 模块的 FPGA。人们仍然需要加载 FPGA 设计，包括实际的 PCIe 数据链路层和事务层，但这些通常是免费的，如 Xilinx FPGAs。

## PCIe HDL 内核

最近的 Xilinx FPGAs 不仅集成了 SerDes 和 PCIe 端点功能，而且 Xilinx 还提供了[免费的 PCIe IP](https://www.xilinx.com/products/intellectual-property/7_series_pci_express_block.html#overview) 模块(在 PCIe 2.1 版中仅限于 x8)用于这些硬件功能，这些功能(基于许可证)可以在商业上使用。如果你希望有一个稍微不那么专有的解决方案，也有开源的 PCIe 核心可用，如[这个 PCIe 迷你项目](https://opencores.org/projects/pcie_mini)在真实硬件上的 Spartan 6 FPGA 上进行了测试，并提供了 PCIe 到 Wishbone 的桥梁，以及[它的后续项目](https://opencores.org/projects/pcie_mini_axi4s_wb)，目标是 Kintex ultra scale+FPGA。

另一方面，英特尔(前身为 Altera) [的 IP 页面](https://www.intel.com/content/www/us/en/programmable/products/intellectual-property/ip/interface-protocols/m-pci-express-protocol.html)似乎强烈暗示给他们的销售人员一个个性化报价的电话。同样，格子有他们的销售人员随时准备接受你的电话为[他们惊人的 PCIe IP 块](https://www.latticesemi.com/Solutions/SolutionCategories/PCIExpress)。在这里，人们可以明确地看到像 PCIe 这样的协议的问题:不像 ISA 或 PCI 设备可以用一些 74xx 逻辑芯片和偶尔的微控制器或 CPLD 拼凑在一起，PCIe 需要相当专业的硬件。

即使购买了物理硬件(如 FPGA)，根据所选的解决方案，使用具有 PCIe 功能的 SerDes 硬件模块可能仍需要购买或连续许可(如工具链)。目前，Xilinx FPGAs 似乎是这里的“首选”解决方案，但这种情况在未来可能会改变。

这里还需要注意的是，PCIe 协议本身对 [PCI-SIG](https://en.wikipedia.org/wiki/PCI-SIG) 的成员正式可用。如果想从头开始实现庞大的 PCIe 规范，这使得已经很大的任务变得复杂，并且使得 PCIe 有开源 HDL 内核更加令人钦佩。

## 把它放在一起

[![](img/683ce38041ec4d2bfcd9c8eb0f5c0d48.png)](https://hackaday.com/wp-content/uploads/2020/12/pci-e-x1.gif)

PCI Express x1 edge connector drawing with pin numbers.

PCIe PCB 的基本电路板设计很容易让人联想到 PCI 卡。两者都使用具有相似布局的边缘连接器。 [PCIe 边缘连接器](https://www.multi-circuit-boards.eu/en/pcb-design-aid/pc-pci-boards.html)厚度为 1.6 毫米，间距为 1.0 毫米(PCI 为 1.27 毫米)，触指间距为 1.4 毫米，倒角角度与 PCI 边缘连接器相同，均为 20°。一个连接器至少有 36 个引脚，但在 x16 插槽配置中可以有 164 个引脚。

[![](img/1a4a5bee71bcf8e278b223b886da2d7c.png)](https://hackaday.com/wp-content/uploads/2020/02/PCI-express_PCIe_leiterplatte_en-themed.png)

PCIe card edge connector cross section.

与 PCIe 的一个重要区别是，与 ISA、PCI 和类似的接口不同，边缘连接器没有固定的长度。它们的长度由总线的宽度决定。在 PCIe 的例子中，没有总线，所以我们用一个单通道(x1 连接器)得到“核心”[连接器引脚](https://pinouts.ru/Slots/pci_express_pinout.shtml)。可以向该单个通道添加额外的“块”,每个“块”添加另一个绑定的通道，以便单个设备可以使用所有连接通道的带宽。

除了常规的 PCIe 卡，你还可以从一系列不同的 PCIe 设备中挑选，比如迷你 PCIe。无论选择何种外形，基本电路都不会改变。

这引发了一个有趣的问题:你的 PCIe 设备需要什么样的速度。一方面，更多的带宽是好事，另一方面，它也需要更多的 SerDes 信道，并且不是所有的 PCIe 插槽都允许安装每张卡。虽然任何配置(x1、x4、x8 或 x16)的任何卡都可以在 x16 插槽(机械)中安装和工作，但较小的插槽实际上可能无法安装较大的卡。一些连接器具有“开放式”配置，例如，如果倾斜，您可以将 x16 卡插入 x1 插槽。其他连接器可以“改装”成适合这种更大的卡，除非保修是一个问题。

PCIe 的灵活性意味着带宽随着绑定通道的数量以及 PCIe 协议版本而扩展。这允许适度降级，例如，如果将 PCIe 3.0 卡插入只能支持 PCIe 1.0 的插槽中，该卡仍将被识别并工作。可用带宽将严重减少，这可能是有问题的卡的问题。可用的 PCIe 通道也是如此，让人想起加密硬币矿工的故事，他们将 x16 个 PCIe 插槽分成 16 个 x1 插槽，以便他们可以运行相同数量的 GPU 或专门的加密硬币采矿卡。

## 到处都是 PCIe

PCIe 的这种灵活性也导致了 PCIe 车道被延伸到陌生而美妙的新地方。像英特尔的 [Thunderbolt](https://en.wikipedia.org/wiki/Thunderbolt_(interface)) (现在的 [USB 4](https://en.wikipedia.org/wiki/USB4) )这样的规格包括 PCIe 3.0 的多通道空间，这使得快速的外部存储解决方案以及外部显卡和内部显卡一样工作。

固态存储已经从 SATA 协议转移到 NVMe，后者实质上定义了直接连接到 PCIe 控制器的存储设备。这一改变使得 NVMe 存储设备可以安装到主逻辑板上，甚至直接集成到主逻辑板上。

显然，PCIe 是这些天要注意的事情。我们甚至已经看到，片上系统(SOC)，如在 [Raspberry Pi 4 板](https://hackaday.com/2020/07/01/adding-pcie-to-your-raspberry-pi-4-the-easier-way/)上发现的那些，现在有一个单独的 PCIe 通道已经被侵入，以人们认为不可思议的方式扩展那些板。随着 PCIe 变得越来越普及，这似乎是一个了解它的好时机。