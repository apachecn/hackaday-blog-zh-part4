# 可定制的微编码控制器有助于在线调试

> 原文：<https://hackaday.com/2021/12/30/customisable-micro-coded-controller-helps-with-in-circuit-debugging/>

在 Hackaday.io 上，[Zoltan·佩基奇]一直在忙着构建一堆工具来帮助验证和调试复古计算应用程序。他介绍了他对使用英特尔 hex 文件进行定制在线测试的看法,该测试基于简单的微编码序列器，可根据高级描述自动生成。

其思想是，能够使用 FPGA 开发板来仿真 CPU 的存储器总线组件非常有用，允许直接存储器访问以用于设计验证目的。这种方法还允许生产测试设备来执行板级验证。[微码编译器(MCC)](https://hackaday.io/project/172073-microcoding-for-fpgas/log/179214-microcode-compiler-in-fpga-toolchain) 生成针对基于 Xilinx FPGA 的开发板所需的所有 VHDL 和支持文件，但足够通用，只需稍加修改即可针对其他平台。

另一个有趣的使用案例支持在线跟踪错误的存储器访问，微码序列器对访问进行解码，并将相关信息转储到串行端口，甚至直接转储到嵌入式 VGA 控制器，只要硬件允许。

这种自动生成可定制微编码硬件的方法是一个非常好的技巧，即使它只在某些情况下有所帮助，[Zoltan]指出，如果没有其他更多的东西，它至少是历史上计算机架构的一个有趣的例子。

示例 8085 项目的源码可以在[项目 GitHub](https://github.com/zpekic/sys_sbc8085) 上找到，工具链源码也可以在这里找到[。](https://github.com/zpekic/MicroCodeCompiler)

为了实现对历史硬件的模拟，微丁的一个有趣的实际应用，来看看这个整洁的[可切换复制计算器项目](https://hackaday.com/2019/11/13/two-vintage-calculators-in-one/)。