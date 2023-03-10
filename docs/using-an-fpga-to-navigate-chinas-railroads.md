# 使用 FPGA 导航中国铁路

> 原文：<https://hackaday.com/2018/09/23/using-an-fpga-to-navigate-chinas-railroads/>

如果你去 mainland China 旅游，你可以乘火车到达这个国家的大部分地区。然而，中国很大，大约和美国一样大，是欧盟的两倍多。穿越那么大的区域并不容易。中国有 300 多个火车站，在某个地方找到最快的路线一点也不容易。这是一个有待解决的工程挑战，幸运的是，康奈尔工程学院的一些学生已经尝试使用 FPGA 有效地导航中国的铁路系统。

FPGA 运行一种算法来寻找两点之间的最短路径，称为 [Dijkstra 算法](https://en.wikipedia.org/wiki/Dijkstra%27s_algorithm)。由于有如此多的节点，这对于计算机计算来说可能会很麻烦，但专用 FPGA 的并行处理大大加快了这一过程。FPGA 还包括一个叫做“[硬处理器系统](https://people.ece.cornell.edu/land/courses/ece5760/DE1_SOC/HPS_INTRO_54001.pdf)”或 HPS 的东西。这不是软核，而是 ARM Cortex-A9 形式的专用计算硬件。测试表明，与单独使用微控制器相比，同时使用 HPS 和 FPGA 可以将计算速度提高 10 倍。

这个项目非常详细地介绍了所涉及的方法、数学和编码背景，如果你对 FPGAs 或旅行推销员式的问题感兴趣，绝对值得一读。不过，FPGAs 并不是你可以用来解决这类问题的唯一专用硬件，如果你在中国旅行时有一个足够大的背包[，你还可以使用不同类型的计算机](https://hackaday.com/2018/01/22/quantum-computing-hardware-teardown/)。

 [https://www.youtube.com/embed/8EkWldmILow?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/8EkWldmILow?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

