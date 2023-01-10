# 这个敏捷的 8 位微型计算机加快了逆向计算的速度

> 原文：<https://hackaday.com/2022/10/21/this-snappy-8-bit-microcomputer-brings-the-speed-to-retrocomputing/>

当对速度的需求战胜了你，思想一般不会转向 8 位计算机。当然，8 位机器对于复古游戏和重温辉煌时代来说很有趣，当然也有一些旧机器明显比其他机器快。但是原始计算能力并不是逆向计算的重点。

或者是？在*的【贝尔纳多·卡斯特鲁普】字节阁楼*推出了一种有趣的机器，叫做[Agon Light](https://www.thebyteattic.com/p/agon.html)，一种 8 位 SBC，有点像微控制器。这台机器有一个 PCB，看起来大约有 Arduino Uno 的一半大，在其外围有一些相同的连接器和端子。Agon Light 的核心是 eZ80 8 位、18.432 MHz 3 级流水线 CPU，与 Z80 二进制兼容。它还具有一个音频视频协处理器，采用 ESP32-Pico-D4 的形式，支持 640×480 64 色显示器和两个单声道音频通道。我们找不到关于 ESP32 的射频系统是否可用的信息；这将是很好的，但也许没有必要，因为有两个 USB 端口和一个 PS/2 键盘插孔。还有一个用于 20 GPIOs 的引脚接头，以及用于串行通信的 I2C、SPI 和 UART。

下面的冗长视频深入到 Agon Light 的所有细节，包括基准测试的结果，所有这些都彻底击败了通常的 8 位嫌疑人。该项目是开源的，所有的设计文件都是可用的，或者你可以得到一个印刷电路板与所有的 SMD 元件，只是把通孔部分。[Bernardo]也鼓励人们制造和销售他们自己的 Agon 灯，这看起来也很酷。老实说，它看起来很有趣，我们很期待看到人们用它做什么。

 [https://www.youtube.com/embed/R2dYZmlu1D4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/R2dYZmlu1D4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

