# SCPI:教你的设备成为实验室的通用语言

> 原文：<https://hackaday.com/2021/11/17/scpi-on-teaching-your-devices-the-lingua-franca-of-laboratories/>

人们有时认为出于自动化目的将设备与其他设备连接起来的概念是一个相当新的发明，这是可以理解的。然而，尽管最近(相对)大肆宣传物联网和“智能家居”，但几十年来，实验室一直在为运行复杂的测量和测试序列安装设备，工厂也在为自动化生产流程做同样的事情。

就像物联网设备的混乱世界一样，来自不同制造商的实验室设备具有大量不兼容的协议和接口标准。最终，这些将合并为 IEEE-488.1 (GPIB)作为物理层，到 1990 年，基于 IEEE-488 的第一个可编程仪器标准命令( [SCPI](https://en.wikipedia.org/wiki/Standard_Commands_for_Programmable_Instruments) )标准发布。

SCPI 定义了(顾名思义)与仪器交互的标准命令。在过去的几十年里，它为从示波器和电源到奇异的科学设备的一切事物提供了远程交互能力。业余爱好者现在可以购买的许多现成设备都具有通过以太网、USB 或 RS-232C 端口的 SCPI 接口，结合软件可以用来实现家庭实验室的自动化。

更好的是，给自己的设备添加 SCPI 功能也相对简单，只要它至少有一个 MCU 和一些与外界通信的方法。

## 重新发明轮子一点也不好玩

尽管为一个定制的小部件提出自己的通信标准很有趣，但坚持现有的标准，而不是在一堆标准中添加另一个“标准”还是有很多好处的。一个很好的理由是，您将花费时间来制定一个可行的协议，该协议将涵盖所有边缘情况，并为将来添加新功能时的扩展留出足够的空间。

另一个原因是与现有软件的兼容性，这也涉及到为什么最终用户可能会对这个令人敬畏的新协议感到兴奋。使用 SCPI 时，它可以相当轻松地集成到现有的(实验室)自动化软件中，因为 SCPI 背后的整个概念是，除了一些必需的命令之外，每个仪器还将执行自己的一系列定制命令。

对于 LabVIEW 或 [Sigrok](https://en.wikipedia.org/wiki/Sigrok) 等软件的用户来说，理想的情况是设备说 SCPI 语，在最坏的情况下，当一个定制的 SCPI 命令还不可用时，必须为其编写一个定制的处理程序。这里永远不会改变的是基本的 SCPI 语法，允许新设备的快速引导，防止错误(没有完美的解析器)和代码的重用。默认情况下，SCPI 的基本命令集还支持同步机制等功能。

尽管如此，当你真正看到堆积在家庭实验室里的测量设备和可编程电源时，并不是所有的都讲 SCPI 语。Rigol [DS1104Z](https://sigrok.org/wiki/Rigol_DS1000Z_series) 示波器通过其以太网端口实现。猫头鹰的小兄弟 [XDM2041](https://sigrok.org/wiki/Owon_XDM2041) DMM (XDM1041)通过它的 USB 端口说 SCPI 语。到目前为止一切顺利，但电子负载(蜘蛛实验室 [Reload Pro](https://sigrok.org/wiki/Arachnid_Labs_Reload_Pro) )通过 USB 说出一个[自定义协议](http://www.arachnidlabs.com/reload-pro/usb-interface/)，这可能是 SCPI。

Manson [HCS-3304](https://sigrok.org/wiki/Manson_HCS-3xxx_series) 可编程电源对另一个定制协议做了同样的事情，手册修订版中列出的命令显然也经常是错误的。由于 Sigrok 目前只支持其中的一些设备，自动化测试将涉及一起破解我自己的解码器，而不是使用定制的 SCPI 设备命令进行一些高级别的摸索。

恰当地使用标准可以节省大量的时间、理智和白发。这就引出了下一个问题:将 SCPI 添加到一个人自己的令人敬畏的小部件中有多容易？

## 输入 LibSCPI

不是每个人都想从头开始编写自己的 SCPI 解析器，这就是为什么 SCPI 解析器库 v2，或简称为'[libscpi【T1]'是一个好的开始。执行现行的](https://github.com/j123b567/scpi-parser) [SCPI 1999](https://www.ivifoundation.org/docs/scpi-99.pdf) 标准。由于我们有兴趣在嵌入式设备上使用 SCPI，我们将看看提供的带有 LwIP (netconn) [示例](https://github.com/j123b567/scpi-parser/blob/master/examples/test-LwIP-netconn/scpi_server.c)的免费操作系统。这显示了运行在 FreeRTOS 线程中的 SCPI 服务器的实现。

SCPI 服务器在标准的 SCPI 端口(5025)上设置一个 TCP 侦听端口，之后可以通过任何 Telnet 客户端或类似的原始模式(即纯文本)向设备发送命令。注意，在这个服务器示例中，使用了 LwIP netconn 的`NETCONN_COPY`而不是`NETCONN_NOCOPY`。在使用链式 SCPI 命令时，这对于防止数据损坏(删除后使用缓冲区数据)至关重要。

要将 libscpi 与 USART 或其他接口一起使用，首先要做的是通过调用 `[SCPI_Init](https://www.jaybee.cz/scpi-parser/api/SCPI_Init/)`来设置库。下面的方法也必须在你的代码中实现:

*   `SCPI_Write(scpi_t* context, const char* data, size_t len)`
*   `SCPI_Flush(scpi_t* context)`
*   `SCPI_Error(scpi_t* context, int_fast16_t err)`
*   `SCPI_Control(scpi_t* context, scpi_ctrl_name_t ctrl, scpi_reg_val_t val)`
*   `SCPI_Reset(scpi_t* context)`

这些函数大多是不言自明的。从示例实现中可以看出，SCPI _ 写允许 libscpi 写入您选择的输出，而 SCPI _ 刷新用于刷新任何可能存在的输出缓冲区。SCPI _ 错误打印来自 libscpi 的错误信息，SCPI _ 重置重置设备，SCPI _ 控制用于写入控制通道(可选功能，此处为 TCP 端口 5026)。

为了让 libscpi 解析任何新的输入字符串(总是以换行符、`\n`或`\r\n`结束)，您的代码调用`[SCPI_Input](https://www.jaybee.cz/scpi-parser/api/SCPI_Input/)`，或者在单一命令的情况下，也可以直接使用`[SCPI_Parse](https://www.jaybee.cz/scpi-parser/api/SCPI_Parse/)`。

在 STM32 上使用 ST HAL 和 FreeRTOS 以及一个简单的 HTTP 服务器实现 libscpi 的例子可以在[这个 GitHub 库](https://github.com/MayaPosch/FreeRTOS_SCPI)中找到。这针对 Nucleo-F746ZG 开发板。

## SCPI 数字万用表

libscpi 示例还提供了一个数字万用表设备的示例实现。如果我们打开 [scpi-def.c](https://github.com/j123b567/scpi-parser/blob/master/examples/common/scpi-def.c) 中的命令定义和实现，它会让我们很好地了解定制设备实现需要什么。这从名为`scpi_commands`的命令表开始。

此表以模式的格式定义了所有命令，并关联了回调(除了核心命令之外，所有命令都在同一个文件中实现)，从 IEEE 强制命令开始，例如*CLS(清除状态):

`{ .pattern = "*CLS", .callback = SCPI_CoreCls,}`

命令前面的' * '(星号)表示它是必需的，[通用 SCPI 命令](https://na.support.keysight.com/pxi/help/latest/Programming/GP-IB_Command_Finder/Common_Commands.htm)，每个设备都必须执行。重要的有`*IDN?`，它查询(注意问号)设备的身份，`*RST`命令设备复位，`*WAI`告诉设备等待执行任何新命令，直到该命令之前的命令已经完成。

在这个必需命令块之后，我们得到了具有 DMM 功能的块:

```

{.pattern = "MEASure:VOLTage:DC?", .callback = DMM_MeasureVoltageDcQ,},
{.pattern = "CONFigure:VOLTage:DC", .callback = DMM_ConfigureVoltageDc,},
{.pattern = "MEASure:VOLTage:DC:RATio?", .callback = SCPI_StubQ,},
{.pattern = "MEASure:VOLTage:AC?", .callback = DMM_MeasureVoltageAcQ,},
{.pattern = "MEASure:CURRent:DC?", .callback = SCPI_StubQ,},
{.pattern = "MEASure:CURRent:AC?", .callback = SCPI_StubQ,},
{.pattern = "MEASure:RESistance?", .callback = SCPI_StubQ,},
{.pattern = "MEASure:FRESistance?", .callback = SCPI_StubQ,},
{.pattern = "MEASure:FREQuency?", .callback = SCPI_StubQ,},
{.pattern = "MEASure:PERiod?", .callback = SCPI_StubQ,},

```

在命令中混合使用大写和小写的原因与“模式”方面有关:在 SCPI，只需要模式的大写部分，为了简洁，命令的小写部分可以省略。如前所述，后面带问号的命令是一个查询。使用冒号是为了分隔定义 SCPI 接口的树层次结构的级别。

要使用此层次来测量单个串中 DC 的电压和电流，可以使用以下命令:

`MEASure:VOLTage:DC?;:MEASure:CURRent:AC?`

分号分隔各个命令，前导冒号将层次重置为命令树的根。后一个功能可用于创建非常简短的连接命令字符串，例如测量交流和 DC 电压:

`MEASure:VOLTage:DC?;AC?`

由于第一个命令将我们留在了`VOLTage`层级中，后续的命令将触发`AC?`查询。这意味着，一个设计良好的设备界面可以通过避免不必要的重复，使控制设备变得非常有效，即使是手动输入查询。

## 高级功能

当然，所有这些仅仅触及了 SCPI 能力的表面。除了纯文本输出，数字字符串还可以标记为十六进制(#H)、八进制(#Q)或二进制(#B)。参数可以和命令一起提供，用空格隔开。使用 libscpi，这些参数可以在回调函数中检索到。

还可以使用`*OPC`和`*WAI`命令以及`*OPC?`查询设置复杂的顺序和重叠命令序列。这些命令可以与状态寄存器命令和任何特定于器件的命令结合使用，以控制特定的时序。

SCPI 最好的一点可能是，它可以随着设备的复杂性而扩展，无论是简单的电压表，还是读取量子级扰动的科学仪器，底层协议都不会改变。由于不必每次都重新发明相同的基础，设备的开发者和用户可以专注于重要的事情。

就最终用户而言，这可能是拆开设备包装、插入设备并编程 SCPI 序列使其执行所需功能的经历。这是遵循既定标准的主要好处。

[标题图像:Rigol DS1104Z 示波器背面，以太网和 USB 端口可见。信用:里戈尔]