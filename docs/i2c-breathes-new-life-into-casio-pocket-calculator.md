# I2C 为卡西欧袖珍计算器注入新的活力

> 原文：<https://hackaday.com/2022/02/21/i2c-breathes-new-life-into-casio-pocket-calculator/>

什么时候袖珍计算器不仅仅是一个计算器？[Andrew Menadue]一直在通过计算器的扩展端口添加各种现代功能[来推动他的 70 年代卡西欧 FX-502P 的极限。](https://www.youtube.com/watch?v=JpELJASPR_0)

几个旧的卡西欧计算器包括一个扩展端口，用于连接盒式磁带存储和打印功能。FX-502P 上的数据可以使用众所周知的堪萨斯城标准保存在盒式磁带上，但是这个信号是由卡西欧的 FA-1 计算器支架产生的，而不是 FX-502P 本身。要与计算器本身进行交互，需要理解卡西欧为这一特定型号设计的任何协议。

事实证明，该协议与其同时代的协议相比有点古怪，具有可变长度的数据包和反转的数据逻辑，(零伏是‘1’，三伏是‘0’)。一旦协议被解开，只需将计算器连接到 STM32 上的 GPIO 接口，并使用一些软件魔法开始来回发送数据包。

这种技术可以用来发送和接收来自 SD 卡的数据(通过 RAM 缓冲区)，然而它的其他扩展功能真的让我们很好奇。[Andrew]展示了添加实时时钟或热敏打印机是多么简单。使用 STM32 的 I ² C 功能，很可能所有种类的小工具和传感器都可以与这个老式计算器以及许多其他类似的计算器相结合。

你可以在这里找到更多关于这次黑客攻击的细节，包括一些最初黑客攻击的后续视频。我们对老式计算器并不陌生，在[为一台旧卡西欧](https://hackaday.com/2020/03/08/bus-sniffing-leads-to-new-display-for-vintage-casio/)改装了现代液晶显示器之后，我们上一次特别报道了【安德鲁】。看到这些计算器远未过时，真是令人着迷。

 [https://www.youtube.com/embed/JpELJASPR_0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/JpELJASPR_0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

