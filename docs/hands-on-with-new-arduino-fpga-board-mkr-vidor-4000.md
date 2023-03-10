# 新 Arduino FPGA 板实践:MKR Vidor 4000

> 原文：<https://hackaday.com/2018/07/30/hands-on-with-new-arduino-fpga-board-mkr-vidor-4000/>

当 Arduino MKR Vidor 4000 发布的时候，Hackaday 给你带来了第一眼。Arduino 送来了第一块电路板，所以现在我们终于有了一块！现在还为时过早，文档还有点少，但是我们已经让它运行起来，并通过一些 hello world 练习进行了指导。本文将回顾我们迄今为止对 FPGA 系统的了解，以帮助您使用新硬件。

提醒你一下，以下是 Vidor 板上的内容:

*   8 MB SRAM
*   2 MB QSPI 闪存芯片— 1 MB 分配给用户应用程序
*   微型 HDMI 连接器
*   MIPI 相机连接器
*   由 U-BLOX NINA W10 系列设备支持的 Wi-Fi 和 BLE
*   MKR 接口，所有引脚均由 SAMD21 (32 位 ARM CPU)和 FPGA 驱动
*   具有多达 25 个用户可编程引脚的迷你 PCI Express 连接器
*   FPGA(Intel/Altera Cyclone 10cl 016)包含 16K 逻辑元件、504 KB 嵌入式 RAM 和 56 个 18×18 位硬件乘法器

听起来不错。你可以在 Arduino 获得更多血淋淋的技术细节[，甚至还有一个](https://store.arduino.cc/usa/arduino-vidor-4000)[的示意图](https://content.arduino.cc/assets/vidor_c10_sch.zip)。zip)。

## 证明文件

到目前为止，文档很难获得，但是团队每天都在努力改变这种情况。以下是我们迄今为止使用的资源(除了原理图之外):

*   [入门指南](https://www.arduino.cc/en/Guide/MKRVidor4000)
*   一个有三个库的 [GitHub](https://github.com/vidor-libraries) 站点:一个 FPGA 中通用 I/O 的例子，一个视频的例子，以及一个加载未知——可能是默认——比特流的精简例子
*   [一个非常通用的关于 FPGA 编码的文档](https://www.arduino.cc/en/Tutorial/VidorHDL)
*   [MKR 4000 论坛](https://forum.arduino.cc/index.php?board=125.0)

此外，Arduino 刚刚发布了 Quartus 的示例 FPGA 项目[。我稍后会解释这是什么意思。](https://github.com/vidor-libraries/VidorFPGA)

## 启动并运行 Arduino 桌面 IDE

尽管有入门指南，但这些库似乎不能从基于云的 ide 中使用，因此我们按照说明将 MKR 4000 的测试版支持加载到我们的桌面 IDE 中。请注意，说明显示“正常”的 SAMD 板封装，但你实际上想要的是测试版，它说这是为 MKR 4000。如果你在“董事会管理器”对话框中搜索 SAMD，你会找到它(见下图中的第二个条目)。

我们从 GitHub 获取的 ZIP 文件库，使用从 ZIP 文件安装库选项没有任何问题。

[![](img/216ff88a2da5edab336c7e718f95f2d7.png)](https://hackaday.com/wp-content/uploads/2018/07/dialog.png)

## 代码是什么样子的？

该板最有趣的部分当然是 FPGA，这让我们想知道器件的代码会是什么样子。浏览代码时，我们对除了 JTAG 代码之外的所有代码都缺少注释感到有点沮丧。我们决定首先关注 VidorPeripherals 存储库，并深入到头文件中寻找一切如何工作的线索。

查看 [VidorPeripherals.h](https://github.com/vidor-libraries/VidorPeripherals/blob/master/src/VidorPeripherals.h) ，可以看到有一些有趣的 I/O 器件，包括 SPI、I2C、UART、读取正交编码器和 NeoPixel。还有一些头文件是不存在的(大概不会得到定义来打开它们)，所以在确定它们确实存在之前，不要对一些头文件的名称感到太兴奋。

然后我们决定尝试[示例测试代码](https://github.com/vidor-libraries/VidorPeripherals/blob/master/examples/VidorTestSketch/VidorTestSketch.ino)。该库提供了一个您需要设置的全局 FPGA 对象:

```
// Let's start by initializing the FPGA
if (!FPGA.begin()) {
    Serial.println(&quot;Initialization failed!&quot;);
    while (1) {}
}

// Let's discover which version we are running
int version = FPGA.version();
Serial.print(&quot;Vidor bitstream version: &quot;);
Serial.println(version, HEX);

// Let's also ask which IPs are included in this bitstream
FPGA.printConfig();
```

这段代码的输出如下所示:

```
Vidor bitstream version: 1020107
number of devices 9
1 01000000 MB_DEV_SF
1 02000000 MB_DEV_GPIO
4 04000000 MB_DEV_I2C
6 05000000 MB_DEV_SPI
8 06000000 MB_DEV_UART
1 08000000 MB_DEV_SDRAM
4 09000000 MB_DEV_NP
11 0A000000 MB_DEV_ENC
0 0B000000 MB_DEV_REG

```

在许多情况下，FPGA 提供的器件是非常透明的。例如，下面是示例代码中的另一个片段:

```
// Ok, so we know now that the FPGA contains the extended GPIO IP
// The GPIO pins controlled by the FPGA start from 100
// Please refer to the online documentation for the actual pin assignment
// Let's configure pin A0 to be an output, controlled by the FPGA
FPGA.pinMode(33, OUTPUT);
FPGA.digitalWrite(33, HIGH);

// The same pin can be read by the SAMD processor :)
pinMode(A0, INPUT);
Serial.print(&quot;Pin A0 is &quot;);
Serial.println(digitalRead(A0) == LOW ? &quot;LOW&quot; : &quot;HIGH&quot;);

FPGA.digitalWrite(33, LOW);
Serial.print(&quot;Pin A0 is &quot;);
Serial.println(digitalRead(A0) == LOW ? &quot;LOW&quot; : &quot;HIGH&quot;);
```

[![](img/3d204c3e02dce32fbb3120a798157b26.png)](https://hackaday.com/wp-content/uploads/2018/05/vidorheader.jpg)

这很简单，而且 CPU 和 FPGA 都可以使用这些引脚。我们找不到映射引脚的文档，但我们假设它即将到来。

比如说，使用额外的串行接口也很容易:

```
SerialFPGA1.begin(115200);
while (!SerialFPGA1);
SerialFPGA1.println(&quot;test&quot;);
```

## 比特流

那么 FPGA 代码在哪里呢？据你所知，这只是一个新的 Arduino，有很多额外的设备通过这个神秘的 FPGA 对象连接。诀窍是 FPGA 代码在库中。为了了解它的工作原理，我们先来谈谈 FPGA 的工作原理。

当你用 C 语言写程序时，这并不是计算机真正要看的，对吗？编译器把它转换成一串数字，告诉 CPU 去做事情。FPGA 与它既相同又不同。你写程序——通常用硬件设计语言，如 Verilog 或 VHDL。你把它编译成数字，但是这些数字不会像 CPU 那样被执行。

我能想到的最好的类比是，FPGA 就像那些老式的 Radio Shack 100 合 1 电子套件之一。电路板上有一堆部件，通过某种方式用电线将它们连接起来。把电线放在一边，你就有了一台收音机。换句话说，你就有了一个防盗警报器。重新布线，你就有了一个金属探测器。这些数字对应于电线。它们在 FPGA 电路中进行连接和配置选项。除非你已经建立了一个 CPU，否则没有任何东西可以像 CPU 那样检查和处理数字。

FPGA 工具产生的数字通常称为比特流。每次 Arduino 上电时，必须有人将比特流发送到 FPGA，就像 Arduino 上的 Cyclone 一样。那个人通常是板上的存储设备，虽然 CPU 也能做到。

这就引出了两个问题:比特流在哪里？它是如何到达 FPGA 的？

第一个问题的答案很简单。如果你在 Github 上看，你会看到在库中有一个名为 [VidorBase.cpp](https://github.com/vidor-libraries/VidorPeripherals/blob/master/src/VidorBase.cpp) 的文件。它有以下几行:

```
__attribute__ ((used, section(&quot;.fpga_bitstream&quot;)))
const unsigned char bitstream[] = {
    #include &quot;app.ttf&quot;
};
```

这意味着如果有一个名为 bitstream 的数组，链接器会把它放在内存中一个特别标记的区域。这个数组用 [app.ttf](https://github.com/vidor-libraries/VidorPeripherals/blob/master/src/app.ttf) 初始化，这只是一个充满数字的 ASCII 文件。尽管有这个名字，但它不是 TrueType 字体。这些数字是什么意思？很难说，尽管从理论上讲，你可以对它进行逆向工程，就像你可以对 CPU 的二进制代码进行反汇编一样。然而，这是我们刚刚谈到的所有库调用工作所需的配置。

关于 FPGA 配置的第二个问题有点神秘。据我们所知，引导装载程序理解该部分中的数据应该复制到 FPGA 配置存储器中，并为您进行复制。不清楚主闪存和配置闪存中是否有副本，但似乎在任何情况下都是透明的。

代码中定义了一个校验和，但是我们改变了它，一切仍然正常。据推测，在某些时候，如果你有错误的校验和，IDE 或引导装载程序会抱怨，但现在似乎不是这样。

顺便说一下，根据 Arduino 论坛，实际上有两个比特流。一个你很少(如果有的话)改变的上电加载。然后还有一个是包含在库中的。您可以双击 reset 按钮进入 bootloader 模式，我们怀疑这会使 FPGA 用第一个比特流初始化，但我们不能确定。不过，在引导模式下，板上的红色 LED 有一个呼吸效应，所以你可以告诉双击工作。

## 我的 FPGA 代码呢？

如果你希望用类似 Arduino 的简单方法用 Verilog 或 VHDL 进行自己的 FPGA 开发，这可不是什么好消息。英特尔会给你一份 Quartus Prime 的拷贝，它会全天为你生成比特流。我们认为——但我们不确定 ASCII 格式只是二进制比特流文件的原始转换。

最近，Arduino 提供了一个可以创建比特流的 Quartus 项目。这提供了拼图的几个关键部分，比如让 FPGA 编译器找到电路板上不同部分的约束文件。

然而，即使有了那个项目，如果你想开始的话，你仍然有一些逆向工程要做。为什么？以下是 Arduino 关于加载自己的 FPGA 代码的说法(我们添加了重点):

> Quartus 将在项目文件夹的 output_files 目录下生成一组文件。为了将 FPGA 整合到 Arduino 代码中，您需要创建一个库并预处理 Quartus 生成的 ttf 文件，以便它包含软件基础架构所需的适当标题。**流程稳定后，将立即披露该流程的详细信息**。
> 
> FPGA 编程有多种方式:
> 
> *   闪烁图像和 Arduino 代码创建一个包含 ttf 文件的库
> *   通过 USB Blaster 对 RAM 中的图像进行编程(这需要安装 FPGA JTAG 头)。只有当 SAM D21 处于引导加载模式时，才能安全地完成此操作**，因为在其他情况下，它可能会访问 JTAG 并导致争用**
> *   通过 SAM D21 通过仿真 USB Blaster 对 RAM 中的映像进行编程(**该组件正在等待发布**

此外，存储库本身表示，在他们能够解决许可问题或清理代码之前，一些关键部分会丢失。这使我们更接近了，但是你仍然需要从例子中逆向工程头部和/或弄清楚如何迫使处理器脱离 JTAG 总线。好消息是，听起来这些信息就要来了，只是现在还没有。

当然，要做任何有意义的事情，你需要了解更多。我们知道 FPGA 设置为 AS 配置模式。我们还向 Arduino 询问了电路板的时钟架构，他们告诉我们:

> [CPU]有自己的时钟，用来产生一个 48 MHz 的参考时钟，该时钟馈入 fpga(并且可以随时移除以“冻结”FPGA)。除了这个参考时钟，FPGA 还有一个内部 RC 振荡器，它不能用作容差问题的精确时序参考，但可以在您不希望[CPU]产生参考时钟的情况下使用。

当然，FPGA 片上有许多 PLL，可以接受任何有效时钟并产生其他频率。例如，在 Arduino 演示的视觉应用中，48 MHz 时钟通过 PLL 转换为 24 MHz、60 MHz、100 MHz 和 120 MHz 时钟。

## 混搭？

[![](img/fccfdb8c031a80667097519507937d67.png)](https://hackaday.com/wp-content/uploads/2018/05/arduino-vidor-4000-demo-bamf-2018-thumb.jpg) 令人失望的一点是——至少目前——你将无法混合搭配不同的 FPGA 库。只有一个比特流，你不能把它们混在一起。虽然 FPGAs 通常可以部分配置，但这是一项困难的技术。但是我们有点惊讶，IDE 不理解如何将库与，例如，EDIF 设计的 IP 文件一起编译。这样，我就可以选择 Arduino UART，并将其与 Hackaday PWM 输出模块以及我自己的 Verilog 或 VHDL 混合使用。

按照现在的构造方式，你将拥有一个由另一个工具(在可预见的将来可能是 Quartus)预编译的比特流。它将与特定的 C++库匹配。仅此而已。不管剩下多少 FPGA 或者实际使用了多少，都将全部用于一个库。

当然，你可以加载另一个库，但它将取代第一个库。所以你一次只能得到一组函数，其他人可以决定那组函数中有什么。如果你自己卷，你就必须自己卷到底。

## 下一步是什么？

对 Arduino Vidor 来说还为时过早。我们希望我们将获得必要的工具和程序来投入我们自己的 FPGA 配置。如果股票库可以以源代码格式获得，包括 Verilog HDL，那就太好了。最近的 GitHub 版本展示了很多，虽然不是所有的例子，但如果我们得到了其余的信息，可能就足够了。

至于更直观的界面，我们不知道这是不是可能的。我们没有看到太多的证据，尽管 Arduino 论坛上的帖子表明他们最终将提供一个“IP 汇编器”，让你将不同的模块组合成一个比特流。我们不知道这是否只适用于“官方”模块。然而，我们知道 Arduino 社区是非常足智多谋的，所以如果我们没有一个好的生态系统，如果有人让它发生，我们不会感到惊讶。最终。

目前，我们将继续利用现有的可用比特流。CPU 上也有一些很好的新特性。例如，您可以[映射两个未使用的串行模块。](https://www.arduino.cc/en/Tutorial/SamdSercom)有一种[基于硬件的协同多任务处理能力](https://www.arduino.cc/en/Reference/Scheduler)。随着更多关于 FPGA 的细节浮出水面，我们将随时通知您，如果您了解到一些情况，请务必在评论中留言，这样每个人都可以受益。