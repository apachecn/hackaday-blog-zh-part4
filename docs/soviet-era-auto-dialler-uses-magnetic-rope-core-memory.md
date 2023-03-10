# 苏联时代的自动拨号器使用磁绳芯存储器

> 原文：<https://hackaday.com/2022/01/13/soviet-era-auto-dialler-uses-magnetic-rope-core-memory/>

这些年来，我们在这些精美的页面上看到了一些有趣的磁芯存储器，但我们不记得看到过太多的*用户* *可编程*磁芯存储器设备。这个有趣的俄罗斯电话自动拨号器在当时是一个非常有用的设备，能够存储和拨打 40 个用户可编程的 7 位数。[【mikeselectricsuff】撕成一个](https://www.youtube.com/watch?v=tPT6nIRFI_I&amp;list=RDCMUCcs0ZkP_as4PpHDhFcmCHyA&amp;start_radio=1&amp;rv=tPT6nIRFI_I&amp;t=2)(视频，下面嵌入)，发现了一些很有意思的科技。在那个时代，这是高科技的东西。不可否认的是，俄罗斯的老技术在使用老部件方面有着令人难以置信的独创性。毕竟，如果它有效，那么就没有必要改变它。但无论如何，这里有趣的是设计者如何决定解决编程和回忆数字的问题，而不使用微处理器，通过使用离散逻辑和[核心绳存储器](https://en.wikipedia.org/wiki/Core_rope_memory)。

这与阿波罗制导计算机使用的技术相同，但采用了用户可配置的形式，显然存储容量要小得多。核心数组由七个四位字组成，每个电话号码一个字，从下到上依次读出。您对数字进行编程的方式是，将编程线插入适当的孔中(一行与数字 1-20 相关，另一行与第二排的数字 1-20 相关)，并沿编织型图案的芯线穿过。在这一过程中，导线会穿过或绕过特定的核心，这取决于您要编码的数字。这种编码的密钥写在设备的盖子上。最后，您需要在匹配的顶部连接器中终止导线，以完成回路。

据我们所知，编码是一个二进制序列，用一个特殊的“停止”代码来表示少于七位数的电话号码。我们将把进一步的分析留给感兴趣的人，只给你指出[原始制造商原理图](http://electricstuff.co.uk/trill2.pdf)。尽情享受吧！

当然，我们不会只提到 rope core memory 和 AGC 而不链接到[一篇关于相同的](https://hackaday.com/2016/09/02/decoding-rediscovered-rope-memory-from-the-apollo-guidance-computer/)的精彩文章，如果这满足了你制作 rope core memory 的胃口，这里还有[一件关于它的小事](https://hackaday.com/2013/10/09/making-a-core-rope-read-only-memory/)！

 [https://www.youtube.com/embed/tPT6nIRFI_I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=2&wmode=transparent&listType=playlist&list=RDCMUCcs0ZkP_as4PpHDhFcmCHyA](https://www.youtube.com/embed/tPT6nIRFI_I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=2&wmode=transparent&listType=playlist&list=RDCMUCcs0ZkP_as4PpHDhFcmCHyA)

