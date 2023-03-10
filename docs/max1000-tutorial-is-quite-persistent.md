# 用这种视觉黑客的持久性来学习 FPGA

> 原文：<https://hackaday.com/2018/08/31/max1000-tutorial-is-quite-persistent/>

每个人都想尝试一下 FPGA 开发，这里有一个很好的方法。您可以使用 30 美元的开发板构建自己的视觉暂留显示器。这是一个有趣的项目，您将学到很多关于 FPGA 设计的知识，以及如何使用 Quartus 设计软件。

这篇文章的灵感来自于[vpecanins]，他做了一个示例项目，你前后挥动板子，一条消息就会出现在半空中。它使用的是 MAX1000，这是一款非常强大但很奇怪的 FPGA 板，价格约为 30 美元。它包含一个 Intel max 10(Intel 什么时候开始做 FPGAs 的？记住，[英特尔早在 2015 年就收购了 altera](https://hackaday.com/2015/06/01/intel-buys-altera-for-16-7-billion/)。我觉得该板很奇怪，因为它还包含一个加速度计，可以使用 SPI 与之对话。对于普通 FPGA 板来说，这有点奇怪，但搭配八个板载 led，非常适合本演示。

因为我没有找到这个例子的任何书面文档，所以我想我们可以帮助您，带您一步一步地参观这个项目。更重要的是，在以后的文章中，我将向您展示如何对本教程进行一些重要的修改，这将使它作为其他项目的基础更加实用。

为了激励自己，看看下面的视频，看看这个项目是做什么的。我修改了文字(WD5GNR 是我的呼号)，当然。现实生活中效果更好，但是视频会给你思路。FPGA 监控加速度计，颠倒 led 闪烁的顺序以形成字符。这是一个非常令人印象深刻的演示，因为它利用了该板的独特功能，非常重要，而且如果您刚刚入门，也不会有太多的 Verilog 内容。

## 先决条件

首先，你需要[安装 Quartus](https://fpgasoftware.intel.com/18.0/?edition=lite) 。精简版是免费的，非常有能力。您可以[下载文件](https://github.com/vpecanins/max1000-tutorial)，打开 demo02_led_text 目录下的 test0.qpf 文件。如果你的 Quartus 版本比原来使用的文件更新，你可能会得到一个关于替换数据库的讨厌的对话框。你可以放心地同意这一点。

## 文件浏览

[![](img/dc8b26056e1a43bfc20c187b3b5c19c5.png)](https://hackaday.com/wp-content/uploads/2018/08/file.png) 在 Quartus 内部的项目导航器上，你可以选择文件，你会看到项目只有几个:

*   top . v–主要的 Verilog 代码。
*   programming _ chain . CDF–这个文件应该告诉 Quartus 如何将配置编程到芯片中，但是它丢失了。不过这不是问题。这不是真的必要，而且很容易再造。
*   font _ rom . qip–一个组件，使用 Altera IP(知识产权)创建一个包含字符模式的 ROM。
*   SPI _ master . v–与加速度计对话的代码。
*   macro . do——这个文件实际上并不存在，显然是作者早期工作遗留下来的。
*   sequencer . v–使用加速度计的代码。

[![](img/ba64bcaf9459c0ab9cbdc4b70c26f74d.png)](https://hackaday.com/wp-content/uploads/2018/08/mega.png) 如果你在列表中展开 font_rom.qip componet，你会看到那里隐藏着一个 Verilog 文件。那个文件是由一个 IP 向导生成的，所以当你可以看它的时候，你不需要去碰它。它使用 Altera Sync RAM IP 块创建一块内存。需要注意的一点是，Verilog 文件指定了一个 init 文件，它是 font5x7.hex。这是一个标准的十六进制文件，包含 ROM 的内容。对了，这是一个名存实亡的 ROM。它是在 RAM 中实现的，但没有写入它的接口，所以从设计的角度来看，它是只读的。然而，它不是非易失性的。每次重新配置 FPGA 时，它都会被重写。

同样，所有这些都是通过回答 IP 向导中的一些问题来设置的。您应该能够使用参数编辑器打开 IP 来更改它，但是似乎缺少一些文件来允许这样做，或者可能是作者手动设置的。然而，如果你去 Quartus 中的 IP 目录并打开库|基本函数|片上存储器| ROM: 1 端口，你可以看到这个过程。如果你想练习，用你自己的 ROM 替换现有的 ROM 是很容易的。

## 顶部模块

顶部模块有一个 12 MHz 系统时钟接口、用户按钮(用作复位)和 8 个 led。它还包含与 SPI 加速度计对话的信号，以及似乎用于调试的 8 位并行 I/O(该设计只是将一些内部信号复制到这些引脚)。

[![](img/bc06c6b800f4e326a54687ad6cda18a8.png)](https://hackaday.com/wp-content/uploads/2018/08/task.png) 要告诉软件那些港口需要去哪里，需要设置位置约束，作者已经做了。有很多方法可以做到这一点。然而，一种方法是找到 Quartus 的 tasks 部分并选择“完整设计”然后，您会看到一个“分配约束”的文件夹打开并选择编辑引脚分配。在这里，您可以设置顶层模块的所有 I/O 引脚——它们的名称、引脚类型以及它映射到 FPGA 上的哪个引脚。

如果您愿意，您可以使用主菜单上的任务项，并选择任务编辑器。我更喜欢这样，因为它像一个易于阅读的电子表格格式。如果你还没有启动项目，你怎么知道发光二极管和其他东西在哪个引脚上？该数据在板的[技术参考手册中。目录中还有一个电子表格记录了作业。](https://wiki.trenz-electronic.de/display/PD/TEI0001+TRM)

模块的其余部分创建 SPI 器件和序列器器件。如果您注意到，序列器有一个单一的输出“方向”,它被映射到模块中的 dir 信号。其他连接只是日常事务，如时钟和与 SPI 器件的连接。

## 积木是做什么的？

在文件的剩余部分[中有一系列的 always 块。这些通常对应于一个逻辑块，当与 posedge 或 negedge 关键字结合时，通常定义一个触发器电路。](https://github.com/vpecanins/max1000-tutorial/blob/75d5d30f9cdadf8a7ac602717cf9a1644552da2f/demo02_led_text/top.v)

```
always @(posedge CLK12M or negedge nrst) begin
	if (!nrst) begin
		divider &lt;= 32'b0;
		divider_out &lt;= 1'b0;
	end else begin
		if (divider != div_coef) begin
			divider &lt;= divider + 1;
			divider_out &lt;= 1'b0;
		end else begin
			divider &lt;= 32'b0;
			divider_out &lt;= 1'b1;
		end
	end
end

```

第一个简单地将时钟分频，因为 12 MHz 有点快。您可以通过更改文件顶部附近的 div_coef 值来调整速度。第二个模块处理 ROM 寻址。每个字符是 ROM 中连续的 5 个字节。因此 addr_lsb 从 0 计数到 4，然后翻转，将 char_inc 设置为 1，作为转到下一个字符的信号。

```
always @(posedge CLK12M or negedge nrst) begin
	if (!nrst) begin
		addr_lsb &lt;= 3'b0;
		char_inc &lt;= 1'b0;
	end else begin
		if (divider_out) begin
			if (addr_lsb == 3'b101) begin
				addr_lsb &lt;= 3'b0;
				char_inc &lt;= 1'b1;
			end else begin
				addr_lsb &lt;= addr_lsb+1;
				char_inc &lt;= 1'b0;
			end
		end else begin
			char_inc &lt;= 1'b0;
		end
	end
end

```

另一个 always 块处理字符地址。foo 数组中存储了 16 个字符。pos 变量从零开始，并在 char_inc 置位时递增。它在 16 岁时翻转。这是一个很好的防御性编程，因为你可以把 16 这个数字改成别的数字。然而，4 位计数器无论如何都会翻转到 16 位，所以在这种情况下，这有点多余，如果工具优化了这种逻辑，我也不会感到惊讶。

```
always @(posedge CLK12M or negedge nrst) begin
	if (!nrst) begin
		addr &lt;= 10'b0;
	end else begin
		if (dir) begin
			addr &lt;= {foo[4'b1111 - pos] - 'h20, 3'b101 - addr_lsb};
		end else begin
			addr &lt;= {foo[pos] - 'h20, addr_lsb};
		end
	end
end
```

foo 数组是您可以更改消息的地方。严格来说，它真的不是一个数组。只是一些被索引的作业。这意味着目前你不能在不重建 FPGA 的情况下改变消息，但是我们将在下一期解决这个问题。然而，一切事物的真正核心是下面的总块。它形成一个地址，其中最高位是当前字符减去 20 个十六进制数。减法会删除不可打印的字符。底部位是从 0 到 4 计数的 3 位。这意味着 ROM 中的第一个位置是一个空格，占用了前 5 个字。然后剩下的依次是 ASCII 字符，各取自己的 5 个字。

然而，这个地址有一个奇怪的属性。如果 dir 位从加速度计设置，则提供高位的字符通过从 1111 二进制数中减去 foo 的索引而端到端“翻转”。底部的位也通过从 5 中减去它们来翻转。这使得 foo 索引变为 15，14，13…而不是 0，1，2…并且也使得行计数向后。

因此，如果 dir 为 0，则消息从左向右播放，如果 dir 为 1，则反向播放。文件的其余部分很简单。代码实例化 ROM 并将其输出分配给各种 led。

## 其余的…

我将让您自己探索 spi_master.v 和 sequencer.v 文件。不过，我要指出，sequencer 是状态机的一个很好的例子。有 11 种状态，电路从一种状态移动到下一种状态，以从加速度计发送和接收它需要的数据。例如，这是前三个状态的代码:

```

case (state)

// 1\. Read WHO_AM_I register (Addr 0x0F)
STATE_Whoami: begin
state &lt;= STATE_Whoami_Wait;

spi_request &lt;= 1'b1;
spi_nbits &lt;= 6'd15;
spi_mosi_data &lt;= 31'b10001111_00000000;
end

STATE_Whoami_Wait: begin
if (spi_ready) begin
state &lt;= STATE_Init;
led_out &lt;= spi_miso_data[7:0];
end
spi_request &lt;= 1'b0;
end

// 2\. Write ODR in CTRL_REG1 (Addr 0x20)
STATE_Init: begin
state &lt;= STATE_Init_Wait;

spi_request &lt;= 1'b1;
spi_nbits &lt;= 6'd15;
spi_mosi_data &lt;= 31'b00100000_01110111;
end

```

注意，led_out 是用于调试的，在最终代码中，输出没有连接到任何东西。每个状态的一般结构是要么执行某个操作并设置下一个状态，要么等待某个操作发生，然后设置下一个状态。很简单。当然，更复杂的状态机可能必须决定下一个状态，但在这种情况下不是这样。真正的工作是在 STATE_Compare 状态:

```

			// 6\. Compare X_OUT of the accelerometer to know the swipe direction
			// The acceleration is maximum at the edges of the swipe, detect that
			// and change direction accordingly.
			STATE_Compare: begin
				state &lt;= STATE_Read;

				if (saved_acc &lt; -8'Sb0010_0000) begin
					led_out &lt;= 8'b1110_0000;
					direction &lt;= 1'b0; end else if (saved_acc &gt;  8'Sb0010_0000) begin
					led_out &lt;= 8'b0000_0111;
					direction &lt;= 1'b1;
				end else begin
					led_out &lt;= 8'b0001_1000;
				end
			end
		endcase

```

不要忘记，led_out 在实际项目中并不使用——它只是用于调试。当加速度的符号变化超出死区时，方向位会发生变化。简单。

## 配置

您知道您想将消息改为其他内容，所以继续修改设置 foo 的代码。双击编译设计任务将生成一个 SOF 和 POF 文件。SOF 文件会将配置发送到板，但不会保存。如果您重置或重启，您将丢失主板上的配置。您必须对 POF 文件进行编程，以便电路板在启动时忠实地重新加载配置。

如果你双击任务列表中的程序设备条目，你将为程序员打开一个单独的窗口。您可以按照 [MAX1000 用户指南](https://shop.trenz-electronic.de/de/Download/?path=Trenz_Electronic/Modules_and_Module_Carriers/2.5x6.15/TEI0001/User_Guide)中的说明了解确切的细节，但想法是将 SOF 或 POF 文件与 JTAG 链上的 FPGA 相关联。如果你在编程器里看到这个设备，那很好，但是如果没有，你可以自动检测。只要确保你有 Arrow-USB-Blaster 的硬件设置和模式设置为 JTAG。您可能还需要特定设置的驱动程序，所以请查看用户指南。

[![](img/59e2cd96453e488e2e2cfb1c104161b9.png)](https://hackaday.com/wp-content/uploads/2018/08/prog.png)

唯一棘手的部分是当你编程一个 POF 文件时，你需要确保勾选程序配置复选框。然后按开始，你就上路了。

## 包裹

 [https://www.youtube.com/embed/cGGR0vB_LdU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/cGGR0vB_LdU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



学习 FPGAs 可能会令人望而生畏。毕竟，你需要学习一个复杂的软件，再加上你需要学习 Verilog(或者 VHDL)并习惯一种新的解决问题的思维方式。除此之外，你还需要学习一些常见的东西，比如器件如何连接，以及如何将“程序”下载到电路板上。但是，像这样摆弄已知的工作示例是获得一切工作方式的直观感觉的好方法。

有这么多东西需要学习，[vpecanins]教程可能不是您的第一步。但这是不错的第二步。如果你想要更温和的介绍，你可以看看我们的 [FPGA 训练营](https://hackaday.io/list/160076-fpga-tutorials)。前 3 个训练营与硬件无关，所以你所学到的将适用于 MAX1000。英特尔提供了大量培训来了解 Quartus。事实上，训练太多了，有时候[都不知道从哪里开始](https://www.intel.com/content/www/us/en/programmable/support/training/course/odswbecome.html)。

下一次，我将向您展示如何在项目中添加 UART，以便您可以通过 USB 端口动态更改显示。这听起来很难，但我会用一些小技巧让它变得相对简单。如果您想尝试一些简单的方法，可以考虑更改代码，使用像条形图一样的 led 来显示它读取的加速度。