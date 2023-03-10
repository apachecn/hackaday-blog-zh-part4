# 用于受保护存储器访问的指令集破解

> 原文：<https://hackaday.com/2020/04/27/instruction-set-hack-for-protected-memory-access/>

nRF51 系列 SOC 是 Nordic Semiconductor 基于 ARM Cortex 内核的低功耗蓝牙芯片系列。nRF51822 具有皮质 M0 内核，用于许多产品。[Loren]写了一篇博文，他声称能够[绕过芯片上的回读保护，从而获得对 ROM、RAM 和寄存器的访问，并允许交互式调试会话](https://www.optiv.com/blog/automated-unlocking-nrf51-series-socs-nrfsec)。

这种攻击源于这样一个事实，即串行线调试或 SWD 接口不能在这些芯片上完全禁用，即使存储器保护单元阻止直接访问任何存储器区域。第二个关键点是，CPU 可以从代码存储器中获取数据。结合社署更改登记册本身的超能力，这是一个强大的工具。

ARM 指令集包含许多间接寻址加载指令，并且[Loren]指向 LDR R2[R0]的伪指令，该伪指令允许从由 R0 指定的 rom 中的位置复制数据。这个想法是在 ROM 中已经存在的代码中搜索指令，因为我们自己不能写入内存。那么我们该怎么做呢？很简单，只要使用程序计数器循环遍历所有代码空间，保持 R0 和 R2 为零。当你命中一条指令，使 R2 与 0x00000 中的东西值相同时(因为 R0 是 0x00000)，我们就找到了这条指令。SWD 最初会将 0x00000 处的值识别为堆栈指针中的值。

一旦你有了可以从 rom 中复制信息的指令的地址(在 PC 中),只需将 R0 设置为不同的值，将 PC 设置为 LDR 指令的位置，单步执行它就可以看到它复制到 R2。循环，你可以转储整个 ROM。[Loren]已经将整个事情打包在一个 Python 脚本( [Github](https://github.com/buildxyz-git/nrfsec) )中，你可以在家里用 ST-Link 试用。

nRF51 被用在很多地方，包括 [BBC microbit 以及其他可以使用廉价 SDR 进行监听的设备](https://hackaday.com/2019/03/28/wopr-security-loses-some-of-its-obscurity/)。游戏正在进行中。

![](img/5c7be9ea848e8f1369dddfc872643268.png)