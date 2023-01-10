# ice blaster:ice 40 的拖放式比特流加载器

> 原文：<https://hackaday.com/2022/07/11/iceblaster-a-dragndrop-bitstream-loader-for-ice40/>

iCE40 系列 FPGAs 在这些页面上得到了相当多的报道，这主要是因为它的可访问性(由于逆向工程和开放工具链方面的巨大努力)，也可能是因为 Lattice Semiconductors 对开源的态度。虽然这些设备很小，而且相当有限，但对于首次涉足这个主题来说，你真的无法打败它们。对于许多简单的 FPGA 应用来说，它们已经足够强大了。在 Hackaday 那边。IO 拥有丰富的设备经验，并为我们的集体 iCE40 武器库增加了另一个工具，即 iCEBlaster，这是一个 [USB 大容量存储设备(MSC)风格的引导加载器](https://hackaday.io/project/185263-iceblaster)，用于拖放比特流加载。需要专门的程序员的日子开始屈指可数了，许多芯片现在向主机提供 USB 大容量存储设备，以便上传固件映像。

FPGAs 往往不会以这种方式工作，启动时需要加载特定于器件的比特流，这通常是外部配置存储器的工作(除非它们有 OTP 存储器)。iCEBlaster(可能是 Xilinx ByteBlaster 程序员的一个游戏？)至少可以在 STM32F4xx 系列设备上运行，但应该可以方便地移植到其他设备上。这个想法非常简单——将新的比特流文件拖到存储设备上会启动 FPGA 目标复位，进而允许 STM32 通过 SPI 接口将比特流发送到 iCE40。仅此而已。

如果你一直在寻找进入 iCE40 的机会，[这个指南可能是一个很好的起点](https://hackaday.com/2018/09/27/three-part-deep-dive-explains-lattice-ice40-fpga-details/)，并且每一次学习经历都需要一个好的项目来驱动它，[在软核 RISC-V](https://hackaday.com/2021/02/07/ice40-runs-doom/) 上运行 Doom 怎么样？