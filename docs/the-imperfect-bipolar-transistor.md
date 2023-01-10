# 不完美的双极晶体管

> 原文：<https://hackaday.com/2021/04/16/the-imperfect-bipolar-transistor/>

我们喜欢假装我们的电路元件是完美的，因为老实说，这让生活更容易，而且在实践中往往没有多大关系。对于正常设计，一英尺导线的电阻很小，或者我们的电容值可能会下降 10%，这并没有太大的区别。然而，我们真正把头埋在沙子里的一个地方是当我们使用双极晶体管作为开关的时候。一个完美的开关在启动时应该有 0 伏的电压。一个真正的开关不会完全到达那里，但它将是非常接近的。但是饱和状态下的双极晶体管不会一直工作。[失调电压]着眼于双极晶体管如何开关，以及为什么饱和状态下晶体管两端的电压为零点几伏。你可以看下面的视频。

要理解它，你需要一点数学知识和对晶体管结构的一些理解。将晶体管用作开关的想法是，晶体管是饱和的——也就是说，增加基极电流不会对集电极电流产生太大影响。虽然它并不完美，但它足以切换继电器或执行其他常见的切换任务。

话说回来，你可以做得更好。[场效应晶体管可以更好地工作](https://hackaday.com/2018/08/17/circuit-vr-a-tale-of-two-transistors/)虽然曾经有一段时间你仍然必须使用双极器件来处理电流、低成本或由于开关频率，场效应晶体管现在可以处理几乎任何双极晶体管可以处理的工作。

尽管如此，理解这些设备背后的理论还是有好处的，它们仍然有自己的位置。毕竟，当你需要一个开关时，有相当多的[选项。](https://hackaday.com/2017/09/07/switching-from-relays-to-bipolar-junction-transistors/)

 [https://www.youtube.com/embed/KpoyFQxNORw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/KpoyFQxNORw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

