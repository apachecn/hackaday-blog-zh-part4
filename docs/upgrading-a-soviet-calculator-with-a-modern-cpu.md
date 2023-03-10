# 用现代中央处理器升级苏联计算器

> 原文：<https://hackaday.com/2022/01/27/upgrading-a-soviet-calculator-with-a-modern-cpu/>

今天的供应链问题可能会使购买微控制器或任何种类的半导体变得困难。但对于那些让复古计算机存活下来的人来说，这个问题一直存在:古老的组件可能已经停产几十年了，二手零件或“新老库存”的供应日益减少是唯一的选择。如果一个罕见的 CPU 坏了，你可能别无选择，只能更换整个电脑。

[Piotr Patek]在获得一台中央处理器损坏的 Elektronika MK-85 可编程计算器时遇到了这个问题。由于找不到替代品，他决定基于 STM32 微控制器制造一个引脚兼容的 CPU 单元[。当然，没有一个现代的 CPU 与 20 世纪 80 年代的苏联设计引脚兼容，所以[Piotr]不得不设计一个小的内插器 PCB 来匹配原来的引脚排列。这也给他足够的空间来添加一个高效的 DC/DC 转换器芯片，为 STM32 产生 2.5 V 电源。](http://pisi.com.pl/piotr433/stmk85_e.htm)

至于软件，[Piotr]设法将最初用 PDP-11 汇编语言编写的 BASIC 解释程序移植到用 c 语言编写的现代版解释程序中。在他从事这项工作的同时，他修复了一些已经存在了大约 35 年的错误。更新的 CPU 还允许 MK-85 绕着它同时代的兄弟运行:[Piotr]计时比原始芯片快大约 30 倍，同时使用相当数量的能量。

如果你碰巧也有一台中央处理器不可靠的 MK-85，你会很高兴地发现[Piotr]的修改原理图和源代码都在他的博客上。这可能是我们看到的第一次计算器 CPU 更新，尽管我们已经展示了其他古老的计算器[用新固件](https://hackaday.com/2017/07/11/cosmac-elf-calculator-gets-new-firmware/)更新，以及一些[基于经典硬件](https://hackaday.com/2020/11/17/another-kind-of-bare-metal-6502-computer-powers-rpn-calculator/)的全新计算器设计。

感谢提示，[cmholm]！