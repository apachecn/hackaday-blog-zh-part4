# FPGAs 的 x 射线视觉:使用 Verifla

> 原文：<https://hackaday.com/2018/11/09/x-ray-vision-for-fpgas-using-verifla/>

上次我谈到了[我如何采用开源的 Verifla 逻辑分析仪，并对其进行修改以增加一些额外的功能](https://hackaday.com/2018/10/12/logic-analyzers-for-fpgas-a-verilog-odyssey/)。正如我所承诺的，这一次我想用行动来展示它，这样你就可以把它融入到你自己的设计中。原始代码实际上并没有捕获您的数据。相反，它创建了一个 Verilog 仿真，可以产生与 FPGA 相同的输出。如果你试图做一些黑盒模拟，这可能是有意义的。我只是想查看数据，所以我创建了一个简单的 C 程序，它可以生成一个 VCD 文件，您可以使用像`gtkwave`这样的常用工具来阅读。它和原始文件都在 [GitHub](https://github.com/wd5gnr/verifla) 上，尽管其中一些没有更新以匹配新代码(特别是 PDF 文档和示例)。

如果你有足够多的引脚，当然，你可以使用外部逻辑分析仪。如果 FPGA 上有足够的空闲空间，可以在设计中放入像 SUMP 或 SUMP2 这样非常灵活的东西。然而，由于这些分析仪可从主机进行配置，因此它们可能有许多电路会与您的分析仪争夺 FPGA 空间。您可以在编译时配置 Verifla，这不太方便，但是占用的空间更小。

## 设置

我对原始代码的配置方式做了相当大的改动。特别是，我将`config_verifla.v`文件移到了项目目录下，并移出了库。然后我合并了文件中的几个条目，并重新排序。下面是一个示例文件的一部分(你可以在 [GitHub](https://github.com/wd5gnr/verifla/blob/master/verilog/verifla/config_verifla.v.template) 上阅读完整的文件):

```

// ********* TIMING and COMMUNICATONS
parameter CLOCK_FREQUENCY = 12_000_000;
// If CLOCK_FREQUENCY &amp;lt; 50 MHz then BAUDRATE must be &amp;lt; 115200 bps (for example 9600).
parameter BAUDRATE = 9600;
// The Baud Counter Size must have enough bits or more to hold this constant
parameter T2_div_T1_div_2 = CLOCK_FREQUENCY / (BAUDRATE * 16 * 2);
// Assert: BAUD_COUNTER_SIZE &amp;gt;= log2(T2_div_T1_div_2) bits
parameter BAUD_COUNTER_SIZE = 15;

// ********* Data Setup
// Number of data inputs (must be a multiple of 8)
parameter LA_DATA_INPUT_WORDLEN_BITS=16;

// ******** Trigger
// Your data &amp;amp; LA_TRIGGER_MASK must equal LA_TRIGGER_VALUE to start a complete capture
parameter LA_TRIGGER_VALUE=16'h0002, LA_TRIGGER_MASK=16'h0003;

// To help store more data, the LA counts how many samples are identical
// The next parameter is the size of the repeat count. Must be a multiple of 8 bits
// If the count overflows you just get another sample that starts counting again.
parameter LA_IDENTICAL_SAMPLES_BITS=16;

// ******** Memory Setup
parameter LA_MEM_ADDRESS_BITS=10; 
parameter LA_MEM_FIRST_ADDR=0,
          LA_MEM_LAST_ADDR=1023;
parameter LA_TRIGGER_MATCH_MEM_ADDR=513;
parameter LA_MAX_SAMPLES_AFTER_TRIGGER_BITS=24; 
parameter LA_MAX_SAMPLES_AFTER_TRIGGER=100000;

// Set this to 1 if you want to fill the buffer with a marker value
parameter LA_MEM_CLEAN_BEFORE_RUN=1;
parameter LA_MEM_EMPTY_SLOT=8'hEE;

// ********** Below this you shouldn't have to change anything

```

为了保持简短，我删除了大部分评论，但您可以在 GitHub 副本中找到详细的评论。显然，你需要设置时钟速度和波特率。您还需要告诉分析仪一次要采集多少样本。这必须是 8 的倍数，在这种情况下，我用 16。随着样本有一个重复计数，这是由`LA_IDENTICAL_SAMPLES_BITS`给出的大小。计数越大，可以压缩的重复数据值就越多，但是当数据不保持不变时，浪费就越多。

当然，这个文件只设置参数。你仍然需要连接你想要的信号。为此，您必须对代码进行简单的更改。

## 获取数据

在你的顶层模块中，你需要这样的东西:

```

top_of_verifla verifla(.clk(clk),.cqual(1'b1),.rst_l(lareset), .sys_run(1'b0),
.data_in({ctimer,6'b0,state}),
.uart_XMIT_dataH(RS232_Tx),
.uart_REC_dataH(RS232_Rx)
);

```

参数很简单:

*   clk–系统时钟
*   c qual–时钟限定符；设为低电平可忽略时钟周期
*   rst _ l–低电平有效复位
*   sys _ run–设置为高电平使分析仪运行(见下文)
*   UART _ XMIT _ dataH–串行发送引脚
*   UART _ REC _ dataH–串行接收引脚
*   data _ in–您想要捕获的数据。您可以使用括号将配置中指定的任意多的位连接在一起
*   trigqual(此处未使用)–设为高电平以启用触发
*   exttrig(此处未使用)–设置高电平触发，不考虑 trigqual
*   待命(此处未使用)–当系统待命并等待触发时，输出变高
*   触发(此处未使用)–当系统被触发时，输出变高

`sys_run`输入是原始代码的遗留物。如果你把它设置为 1，系统将会一直处于戒备状态。如果您的触发器频繁出现，这将使主机软件很难找到数据的开始，您可能会得到糟糕的结果。

我利用了这样一个事实，即许多工具将允许您使用系统 Verilog 特性，并为您通常不需要显式设置的参数提供了默认值。例如，`cqual`设置为 1，`sys_run`设置为 0。不幸的是，有些工具不能做到这一点。例如，我使用的英特尔/Altera 工具版本即使你在设置中勾选了系统 Verilog 框也无法识别。为了解决这个问题，你可以使用`to_of_verifla_nodef.v`中的另一个版本的模块。如果这样做，您必须自己设置所有的输入参数。

在正常操作中，模块处于空闲状态(假设`sys_run`为低电平),直到它通过串行端口接收到来自 PC 的命令。只有两个命令。二进制 0 重置该单元，1 使其进入待命状态。

正如我提到的，原始版本中的 Java 程序会执行此操作，读取数据，并构建一个可以创建输出波形的 Verilog 模型。我写了一个 C 程序,做了基本相同的事情，但是构建了一个 VCD 文件。小写命令行参数必须与 Verilog 配置文件中的设置相匹配。以下是帮助文本:

```
Usage: la2vcd [-B] [-W] [-F frequency] [-T timescale] -b baud, -t trigger_pos -c cap_width, -r repeat_width, -n samples -o vcd_file port_name
You need all the lower case options, although baud will default to 9600
-B output only bytes of capture
-W output only words (default is both bytes and words)
-F sets frequency in MHz (e.g., -F 250).
Or you can set the timescale (e.g, -T 1ns) with -T. 
Note the timescale should be twice the clock frequency. 
Default to 1nS and you do your own math.
```

其他参数(-B、-W、-F 和-T)是可选的。符合上述配置的典型命令行是:

```
la2vcd -B -F 12 -t 513 -c 2 -r 2 -n 1024 -o test.vcd /dev/ttyUSB0
```

请注意，宽度参数是以字节为单位的，因此配置中的 16 在命令行中将是 2。该命令将等待触发并读取数据，将其写入`test.vcd`。您可以使用任何 VCD 查看器打开该文件，例如`gtkwave`。

## 读取数据— gtkwave 技巧

一旦你有了 vcd 文件，你就可以在`gtkwave`中打开它。根据选项的不同，可能有信号字、单个字节或两者都有。此外，将出现时钟和触发输出。当然，你可以随意调整`gtkwave`的输出。

[![](img/2fb29260cdfe63719bbe9cccea1c8c94.png)](https://hackaday.com/wp-content/uploads/2018/10/gtkwave.png)

不过，有一些小技巧可以让生活变得更轻松。既然你可能在两个 VCD 文件中有模拟的和“真实的”数据，那么试试`twinwave`。这是一个围绕`gtkwave`的包装器，它启动两个会话并同步它们。因此，如果你在一组数据上滚动或放置一个标记，你会在另一组数据上得到同样的效果。只需运行，例如:

```
twinwave spin.vcd ++ test.vcd
```

另一个很好的技巧是，您可以制作一个包含数字和名称的 ASCII 文件，如下所示:

```
0 IDLE
1 RUN
2 PAUSE
```

如果该文件是 state.txt，那么您可以通过右键单击跟踪标签并选择 Data Format | Trace Filter File，将它与`gtkwave`中的跟踪相关联。然后，跟踪的值将显示为名称，而不是数字，这很方便。

## 动态数据的位置

事实是，从 FPGA 中提取实时数据应该是最后的手段。模拟通常是非常好的，花时间学习如何管理合成后模拟以后会有回报。毕竟，在模拟中，你可以鸟瞰任何你想看到的数据。然而，有些时候你必须看到真实硬件中发生了什么。

此外，插入任何类型的逻辑分析仪内核都会给你的设计带来一些变化，除非你打算永远把它留在那里。所以有局限性。但是如果你需要它，它有时会被证明是无价的。

我扩展了现有的开源 Verifla 项目，但我很想重写它。看起来你可以很容易地创建一个真正的循环缓冲区，并在一个普通的情况下提高内存利用率，在这种情况下你可以在装备后很快触发。话又说回来，这确实有效，所以也许正确的态度是“如果它没坏，就不要修理它。”

代码应该是相当可移植的。我个人在 IceStorm 和 Quartus 上都用过。最大的问题是已经出现的初始化代码和内存推断。最坏的情况是，对于特定的情况，你总是可以使用设备原语作为内存。

有趣的是，要么将它打包成一个带有用户界面的更大版本，要么获取 SUMP2 代码并创建一个专门用于嵌入的 fork。如果您接受挑战，请务必通过举报热线告知我们，这样我们就可以告诉所有人。