# 探索运算放大器加载

> 原文：<https://hackaday.com/2021/04/18/exploring-op-amp-loading/>

运算放大器通常很容易应用，但有些实际的非理想行为你必须记住。[EEforEveryone]拿了一块测试板，上面有一些 2X 放大器，在摆弄了示波器探头之后，演示了运算放大器输出上容性负载的影响。(视频，嵌在下面。)

问题中的运算放大器是 OP07。事实上，单输入端有两个相同的运算放大器。一个运算放大器的输出直接馈入示波器探头。第二个通过由 NPN 和 PNP 晶体管组成的双极性晶体管缓冲器。两个输出都有可选的电容，可以跨接在电路中或电路外。

没有电容，一切如你所愿。信号进入，两个输出产生两倍幅度的完美复制。增加容性负载会使输出信号失真，正如你所料，输出端的电容越大，失真越严重。缓冲确实有所帮助，但仍然存在失真。

旁白提到，他可能应该使用更差的运算放大器来强调试图驱动高容性负载的问题，包括不稳定性。但是，即使使用高性能运算放大器，也可以看出增加缓冲器绝对是可取的。不过，天下没有免费的午餐，因为有了缓冲器，你确实会损失一些输出电压范围。最后，您还可以看到一个调整运算放大器的示例。

如果你喜欢虚拟地做实验，你可以这样做。如果你去了，别忘了试试[所有的模拟](https://hackaday.com/2021/01/15/circuit-vr-even-more-op-amps/)。

 [https://www.youtube.com/embed/LUk418xY9-U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/LUk418xY9-U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

