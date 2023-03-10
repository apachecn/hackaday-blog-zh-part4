# 切片您的下一个 FPGA 设计

> 原文：<https://hackaday.com/2021/06/28/slice-your-next-fpga-design/>

最近的趋势是将高级结构转换成类似 Verilog 或 VHDL 的 FPGA 代码。Silice 走的是另一条路:它将非常特定于硬件的概念转换成 Verilog，旨在成为一种更具表现力和更易于使用的语言。

为什么是 Silice？该项目的网页列举了它的设计目标:

*   一个清晰、简单的语法，清楚地揭示了操作流程和时钟周期的花费。
*   关于流量控制(循环、调用)及其时钟周期消耗的精确规则。
*   熟悉的硬件结构，如总是阻塞、实例化、表达式跟踪(连线)。
*   一种可选的面向流控制的设计风格(自动 FSM 生成)，它自然地集成在设计中:while、break、子程序。
*   容易描述管道的可能性。
*   通过自动修剪(如常量或绑定)，自动为变量创建触发器。
*   通用接口和分组 io 便于重复使用和模块化设计。
*   易于实例化和重复使用的通用电路。
*   显式时钟域和复位信号。
*   熟悉 C 和 Verilog 元素的语法。
*   与 Verilog 互操作，允许导入和重用现有模块。
*   基于 LUA 的强大预处理器。

有几个例子可以说明 Silice 支持的不同类型的编码，从强制闪烁的 LED 到 RISC-V CPU 和视频处理应用。下面是这个闪烁的例子的一部分，只是为了让你感受一下它的样子:

```

algorithm main(output uint5 leds)
{
intensity less_intense;
uint26 cnt = 0;
leds := cnt[21,5] &amp; {5{less_intense.pwm_bit}};
cnt := cnt + 1;
}

algorithm intensity(output uint1 pwm_bit)
{
uint16 ups_and_downs = 16b1110000000000000;
pwm_bit := ups_and_downs[0,1];
ups_and_downs := {ups_and_downs[0,1],ups_and_downs[1,15]};
}

```

当然，与直接 Verilog 相比，真正的优势只有在一些更复杂的例子中才显现出来。

用 Silice 做项目？给我们一个[提示](https://hackaday.com/submit-a-tip/)，这样我们就可以和大家分享了。如果你真的想接近硬件，你可以看到一个 [FPGA 拆卸](https://hackaday.com/2020/09/21/whats-inside-an-fpga-ken-shirriff-has-again-the-answer/)。如果你想比较 Slice 和另一种硬件描述语言，请查看 [SpinalHDL](https://hackaday.com/2018/12/08/vexrisc-v-exposed/) 。