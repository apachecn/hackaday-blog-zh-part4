# 用焊料固定一个昂贵的频谱分析仪

> 原文：<https://hackaday.com/2018/11/08/fixing-a-crazy-expensive-spectrum-analyser-with-solder/>

它曾经是一个频谱分析仪，是一个奇特的装置。然而，如今示波器具有某种能力来完成这项工作是很常见的，也就是说，绘制振幅与频率的关系。然而，一个专用的商业产品通常会有更多的带宽和其他功能。【信号路径】拿起一个 [Anrtitsu 7.1 GHz 便携式频谱分析仪](https://www.youtube.com/watch?v=1_M-Wccn2w8)。一套昂贵的装备——在易贝大约 4000 到 8000 美元——如果它能工作的话，但这一套不行。它需要电源，但也缺少设备用来启动的内部闪存卡。

由于是便携式的，所以在一个非常小的空间里塞进了许多数字和射频电子设备。最初的拆除看起来不是很有趣，因为它主要是一个射频屏蔽。然而，许多微小的螺丝之后，你终于可以看到实际的电子。

第一块电路板是跟踪发生器，它利用 ADI 公司的专用芯片产生四种不同的数字传输流，并将其转换为模拟信号。过滤器在印刷电路板上非常明显，还有一些未安装在本装置中的附加选项。

输入板使用继电器进行输入切换，有正负之分。该仪器不是最新产品，而且[Signal Path]提到，与您在较新设备中看到的相比，许多组件似乎都很大。

看起来它可能工作，但 LO(本地振荡器)解锁错误需要更多的努力。这也给了他一个借口，向我们展示更多的董事会。电路板上的一点压力导致本地振荡器解锁，这表明焊点不良或其他类型的布线问题。

一点侦查工作将问题缩小到一个小的屏蔽电路。屏蔽罩内有一个变容二极管和一些相关部件。返工焊点似乎可以解决这个问题。

我们大多数人都不会撕毁一个价值 10，000 美元的仪器，但多亏了像这样的视频，我们可以在别人看的时候看。鼓起勇气打开一个 3 美元的万用表要容易得多。另一方面，至少这个频谱分析仪没有[花费超过一百万](https://hackaday.com/2018/09/24/tearing-into-a-1-3-million-oscilloscope/)。

 [https://www.youtube.com/embed/1_M-Wccn2w8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/1_M-Wccn2w8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

