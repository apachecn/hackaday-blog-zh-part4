# 8087 协处理器如何产生偏差

> 原文：<https://hackaday.com/2018/08/18/how-the-8087-coprocessor-got-its-bias/>

我们大多数人都去过那里。您构建了一个器件，但意识到需要两个或更多电压。你可以连接多个电源，但这可能不方便，也不优雅。或者，你可以在器件本身做些事情，从一个电压开始产生额外的电压。当[Ken Shirriff] [打开一个 8087 协处理器的盖子开始探索它](http://www.righto.com/2018/08/inside-die-of-intels-8087-coprocessor.html)时，他发现它也有同样的问题。它需要:+5 V，一个地，和一个附加的-5 V。

他的探索从确凿的证据开始。在打开芯片的盖子，数出所有连接到不同焊盘的焊线后，他发现多了一根。不难看出，额外的电线连到了芯片的基板上。这是为了给衬底提供负偏压，在一些高性能芯片中这样做是为了获得更高的速度，更可预测的晶体管阈值电压，并减少漏电流。在检查焊线在电路中的位置时，他发现了横幅图像中显示的两个电荷泵电路。它们以交替的方式向衬底提供-5 V 的偏置电压，如果考虑到电压降，则大约为-3 V。当然，他也解释了电路并深入研究，包括展示如何提供振荡来使电荷泵工作。

如果这和[Ken]以前的探索有任何相似之处，这将是探索 8087 系列文章的第一篇。至少这是我们所希望的，因为他之前曾让我们高兴地对《太空入侵者》中使用的 76477 音效芯片进行了[逆向工程，然后](https://hackaday.com/2017/05/06/reverse-engineering-space-invaders-sound-chip/)[更深入地谈论了芯片部件中使用的集成注入逻辑(I ² L)](https://hackaday.com/2018/06/08/space-invaders-sound-chip-went-old-school-with-i2l/) 。