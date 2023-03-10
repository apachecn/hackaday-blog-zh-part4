# 改良的微波固化树脂部件

> 原文：<https://hackaday.com/2021/05/05/modified-microwave-cures-resin-parts-with-style/>

一旦你跨越到基于树脂的 3D 打印，你会很快发现将零件放在阳光下固化并不总是可行的解决方案。获得一致结果的最佳方式是使用专用的固化室，它不仅可以旋转部件，使它们均匀地暴露在光线下，还可以让您调整具体的固化时间。当这个部分完成时，会有一个蜂鸣器响，这也很方便。等等，这听起来有点耳熟…

正如你所料，[Stynus]并不是第一个注意到理想的紫外线固化机器和简陋的微波炉之间的相似之处的人。但是他的转变无疑是我们见过的最巧妙的转变之一。最终产品*看起来*不像是一个被黑掉的微波炉，更像是一台特制的固化机器，这在很大程度上要归功于所有最初的控制仍然有效。

[![](img/9ecb4ffce6e0f0c82f27d2f0aa615d12.png)](https://hackaday.com/wp-content/uploads/2021/05/uvmicrowave_detail.jpg) 当【Stynus】注意到控制面板由一次性可编程 PIC16C65B 微控制器供电时，重大突破出现了。将它换成引脚兼容的 PIC16F877A 开辟了编写定制固件与所有微波炉原始硬件接口的可能性，他只需要逆向工程它是如何连接的。花了一些时间来弄清楚微控制器上有限的引脚如何运行 LED 显示器，同时读取按钮和开关，但我们要说最终的结果比工作更值得。

由于完全控制了微波炉的硬件，所有[Stynus]要做的就是去掉所有可怕的高压部分(这些部分从一开始就不再起作用)并安装一系列紫外发光二极管。现在，他只需将一个零件扔在盘子上，旋转刻度盘到所需的固化时间，然后按下按钮。在下面的视频中，你可以看到他甚至重新利用了控制面板上的一些按钮，让他可以为 EEPROM 设置新的默认“烹饪”时间。

与更传统的熔融沉积成型(FDM) 3D 打印机相比，[树脂打印需要大量额外的后处理和设备](https://hackaday.com/2019/10/02/when-does-moving-to-resin-3d-printing-make-sense/)。你[不一定非要清理你的微波炉](https://hackaday.com/2020/10/03/sunshine-in-a-bag/)只是为了修复你的打印，但是你最好在扣下闪亮的新打印机的扳机之前充分考虑你的工作流程。

 [https://www.youtube.com/embed/7Ee5pYmu-Ns?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/7Ee5pYmu-Ns?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

