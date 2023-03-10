# 自己实施真气感应充电

> 原文：<https://hackaday.com/2019/04/11/implementing-qi-inductive-charging-yourself/>

感应充电是一项承诺很多的技术，但还没有完全兑现不再需要插上手机的承诺。然而它背后的技术却出奇的简单。S]用一个基于 ATtiny13 的例子带我们了解这一切。

感应充电器的操作必须巧妙，因为如果它连续工作，它很快就会与感应炉架有更多的共同点，从而成为火灾风险，所以它必须确保在试图传输功率之前，有一个兼容的设备停在它上面。它通过周期性地发送功率脉冲来唤醒与之接触的任何设备来实现这一点，该设备通过修改接收器调谐电路的谐振，以编码到设备场的串行数据流来响应。这是由[Vinod]设备中的 ATtiny 控制下的一对 MOSFETs 完成的，结果是在一块原型板上构建了一个功能感应功率接收器，并配备了一个降压转换器，能够提供适合为手机充电的 5 伏电压。你可以[在 GitHub](https://github.com/vinodstanur/qi_wireless_receiver_attiny13) 上找到代码，并在 break 下面看到它的运行。

这项技术之前已经在这里出现过几次，例如当 Qi 充电器被集成到 Chromebook 中时。

 [https://www.youtube.com/embed/JiKEMybIFig?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/JiKEMybIFig?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

