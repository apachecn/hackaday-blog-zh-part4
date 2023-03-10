# Logic Meter 旨在使业余爱好电子故障诊断更容易

> 原文：<https://hackaday.com/2021/01/28/logic-meter-aims-to-make-hobby-electronics-troubleshooting-easier/>

基本的测试仪器套件——一个台式电源、一个好的万用表，也许还有一个示波器——非常灵活，但在诊断一些常见硬件设置的问题时，并不完全是“即插即用”的。例如，伺服驱动器的问题可能很容易用示波器解决，但设置好一切以查看 PWM 信号发生了什么需要一些时间。

一定有更好的方法来诊断业余爱好电子产品的困境，如果[鲍勃·亚历山大]有他的方法，[他的“逻辑仪表”](https://www.galacticstudios.org/the-logic-meter/)，或非常接近它的东西，将是下一个必备的工作台工具。逻辑表将示波器和逻辑分析仪的一些功能结合到一个方便的仪器中，就像万用表一样容易使用。逻辑仪表的探头连接到电路中的逻辑电平信号，可以设置为直接从 UART 或通过 SPI 总线连接捕捉或发送串行数据。还有测试伺服系统和具有可配置 PWM 输出的类似设备的功能。[Bob]用一个 GPS 模拟器和一个简单的逻辑分析仪，加上一些实用功能完善了功能。

逻辑表的美妙之处在于[Bob]已经将它的下一步主要留给了社区。他得到了一份关于基于 PIC32 的硬件的详细信息的 GitHub repo，下面的视频清楚地表明这只是进一步工作的起点，他希望这能产生一个商业版本的 Logic Meter。这是一种令人耳目一新的态度，我们希望它有所回报；从一些[【鲍勃】的逆向计算改造](https://hackaday.com/2019/08/25/vintage-console-becomes-the-calculator-it-appears-to-be/)来看，类似逻辑表的东西可能会非常方便。

 [https://www.youtube.com/embed/55UjsmX5F90?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/55UjsmX5F90?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

