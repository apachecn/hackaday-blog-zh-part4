# 如何在您的 FPGA 项目中添加 UART

> 原文：<https://hackaday.com/2018/09/06/fpga-pov-toy-gets-customized/>

能够在主机和项目之间进行通信通常是一项关键要求，对于 FPGA 项目，通过添加 UART 之类的子模块就可以轻松实现。通用异步收发器是一种便于与串行端口通信的硬件，因此您可以从计算机发送命令，并获得相应的消息。

上周我写了关于[的一个示例 POV 项目，它是学习](https://hackaday.com/2018/08/31/max1000-tutorial-is-quite-persistent/)的一个很好的例子。它不仅不平凡，而且很好地利用了主板的特性。但它将消息硬编码到 Verilog 中，这意味着每次想要更改它时，都需要重建 FPGA。添加 UART 将允许我们更新该消息。

好消息是这个演示是开源的，所以我把它放到了 GitHub 上，这样[你就可以跟随我的新演示](https://github.com/wd5gnr/max1000-tutorial)了。为了说明如何在这个项目中添加 UART，我做了一个简单的计划:

1.  以一种可以随时修改的方式存储文本
2.  插入 UART 以接收串行数据并存储为文本
3.  使用回车为新文本重置数据指针
4.  使用转义清除显示并重置数据指针

## 查找和添加 UART 内核

UART 是一个相当常见的项目，你会认为在 Quartus 中看到的 Altera IP 目录中会有一个。有，而且被埋没在大学项目下。它也有一些怪癖，因为它真的希望成为整个系统的一部分，而我只是想使用 UART。

实际上，对于这个应用程序，我们只需要接收器。我已经写了很多次这样的代码，但是最近我一直在使用一个过去某个时候得到的麻省理工学院许可的 UART。这里有几个版本，包括在[的 free cores](https://github.com/freecores)——它有许多可重复使用的 FPGA 位，以及在[的 OpenCores](https://opencores.org/project/osdvu) 。如果你四处看看，你可以找到从 UARTs 和 PS/2 接口到整个 CPU 的 FPGA 代码。没错，你也可以从官方的 IP 目录中找到很多，但你可能无法在其他 FPGA 家族中使用。例如，我正在使用的 UART 可以在 Lattice IceStick 或任何我想用的 FPGA 上正常工作。(我使用的版本比我能找到的任何其他版本都要新一点，即使是使用谷歌，所以请检查我的回购。)

UART 驻留在一个文件中[,很容易将它放入项目中，但是要克制这种冲动，采用一些更好的实践。我在顶层目录中创建了一个 cores 目录，并把它放在那里。](https://github.com/cyrozap/osdvu/blob/d18488c41141cfb1c7b29f5a5840510e727ae5a2/uart.v)

UART 接口非常简单，对于这个项目，我们不需要发射器，所以很多都是空的。代码如下:

```

uart #(
.baud_rate(9600), // default is 9600
.sys_clk_freq(12000000) // default is 100000000
)
uart0(
.clk(CLK12M), // The master clock for this module
.rst(~nrst), // Synchronous reset
.rx(UART_RXD), // Incoming serial line
.tx(UART_TXD), // Outgoing serial line
.transmit(), // Signal to transmit
.tx_byte(), // Byte to transmit
.received(isrx), // Indicated that a byte has been received
.rx_byte(rx_byte), // Byte received
.is_receiving(), // Low when receive line is idle
.is_transmitting(),// Low when transmit line is idle
.recv_error() // Indicates error in receiving packet.
);

```

很简单。波特率为 9600 波特，输入时钟频率为 12 MHz。clk 参数连接到那个 12 MHz 时钟，rst 参数得到一个正复位信号。nrst 信号为低电平有效，因此我在输入时将其反相。我连接了 MAX1000 板的两个引脚，尽管我不会使用发射器，因为我认为我可能会在某个时候使用它。

另外两个相连的信号是 rx _ byte——你可以猜猜这是什么——和 isrx，当串行端口上有东西进来时，isrx 变为高电平。

## 约束变化

信号 UART_RXD 和 UART_TXD 现在出现在顶层模块中:

```

module top (
input CLK12M,
input USER_BTN,
output [7:0] LED,
output SEN_SDI,
output SEN_SPC,
input SEN_SDO,
output SEN_CS,
output [8:1] PIO,
input UART_RXD,
output UART_TXD
);

```

然而，这还不够。您需要设置约束来匹配物理引脚。文档在这方面有点混乱，因为串行端口在 USB 芯片的端口 B 上，理论上可以是任何东西。我花了一点时间研究了一些例子，才弄清楚哪一个是哪一个。

在赋值编辑器中，我们需要的两个管脚被标记为 BDBUS[0]和 BDBUS[1]。我将这些引脚上的位置约束设置为 Enabled=No，这样它们就不会与我更具描述性的名称冲突。然后，我在任务编辑器中创建了这四个条目:

[![](img/ebbc6486617ba396effc531a7cff904c.png)](https://hackaday.com/wp-content/uploads/2018/08/assign.png)

那会起作用的。现在我们需要以某种方式将这些输入字符输入到 led 中。

## 数据存储

原始代码将文本设置为显示为一个赋值。这在编译时很紧凑，但不允许您在运行时更改消息(您需要重新编译并再次上传)。

```

assign foo[0] = &quot;W&quot;;

```

为了改进这一点，我将 foo 改为一个寄存器类型，并对它进行了初始化。(有些 Verilog 编译器不会合成一个初始块，但我正在使用的 Quartus 版本会。)然而，这与响应复位是不同的。它在配置时初始化寄存器，仅此而已。对于这个应用程序，我认为这很好。如果您想重新加载，请循环供电或强制重新配置，但按下用户按钮不会改变消息。

这就是变化的样子:

```

reg [7:0] foo [0:15];
initial
begin
foo[0] = &quot;W&quot;;
foo[1] = &quot;D&quot;;
foo[2] = &quot;5&quot;;

. . .

```

## 处理输入

通过这种新的配置，文本是可延展的，我们可以听到来自 PC 的数据。我们只需要把这些点联系起来。

```

// Let's add the ability to change the text!
// Note: I had to change the foo &quot;array&quot;
// To be more than a bunch of assigns, above, too

wire isrx;   // Uart sees something!
wire [7:0] rx_byte;  // Uart data
reg [3:0] fooptr=0;   // pointer into foo array
integer i;

always @(posedge CLK12M) begin
   if (isrx)    // if you got something
	    begin
		  if (rx_byte==8'h0d)
		     fooptr&lt;=0;
		  else if (rx_byte==8'h1b) 
		  begin
		      fooptr&lt;=0;
// Note: Verilog will unroll this at compile time
		      for (i=0;i&lt;16;i=i+1)
			  	   foo[i] &lt;= &quot; &quot;; 
		  end
		  else begin
		    foo[fooptr]&lt;=rx_byte;  // store it
		    fooptr&lt;=fooptr+1;   // natural roll over at 16
		  end
		end
end

```

这很简单。在每个时钟上升沿，我们观察 isrx。如果它很高，我们会查看字符是回车符(8'h0d)还是转义符(8'h1b)。不要忘记这一行是赋值语句，而不是“小于或等于”语句:

```
fooptr <= 0;
```

如果字符是别的什么，代码将它存储在 foo[fooptr]中。fooptr 变量只有 4 位，所以当我们递增它时，16 个字符的翻转会自动完成。

代码中唯一的另一个奇怪之处是在 FPGA 合成中使用了 for 循环。有些工具可能不支持这一点，但请注意 I 变量是一个整数。编译器足够聪明，知道它需要在编译时运行那个循环，并为主体生成代码。所以您可以很容易地用 16 行显式命名 foo 的每个元素来代替它。当然，for 循环必须有明确的限制，例如，对于可接受的循环数可能还有其他限制。

这就是全部了。一旦你加载了 FPGA，它看起来就像往常一样。但是如果你在 USB 串口上打开一个终端(在我的机器上是/dev/ttyUSB9 因为我有很多串口；您的几乎肯定会不同，如/dev/ttyUSB0)，将其设置为 9600 波特，您可以更改文本。

如果你的终端不做本地回应，你会打字瞎。从 FPGA 回显字符将是一个很好的练习，也将利用发送器。

## 下一步是什么？

如果你想进行实验，现在你已经有了一个可以读取加速度计的框架，只需多做一点工作，它就可以与 PC 进行交互。例如，您可以通过 PWM led 来控制终端的亮度。或者创建一个随时间滚动的更长的文本字符串。

现代 FPGAs 的一个吸引人的地方是它们可以容纳 CPU。即使这种廉价的主板也可以承载一个简单的 NIOS 处理器。这使您可以进行串行通信等操作，并使主机通信等管理工作变得更加简单。您仍然可以将 FPGA 的其余部分用于高速或高度并行的任务。例如，这个项目可以很容易地让 NIOS CPU 与 PC 对话，而 FPGA 处理运动检测和 led 驱动。正如我拒绝了“股票”UART，并得到了一个其他地方，有大量的替代 NIOS 将适合这个板。

如果你还想了解更多，请查看我们的 [FPGA 训练营](https://hackaday.io/list/160076-fpga-tutorials)。它们不是专门针对 MAX1000 的，但大多数材料都适用。当然，如果你愿意投入时间，英特尔会提供很多培训[。](https://www.intel.com/content/www/us/en/programmable/support/training/course/odswbecome.html)

 [https://www.youtube.com/embed/cGGR0vB_LdU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/cGGR0vB_LdU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

