# 波兰复古硅带来了这台电脑的生活

> 原文：<https://hackaday.com/2019/01/28/polish-retro-silicon-brings-this-computer-to-life/>

对于我们来说，在报道一个主题时，只写我们所知道的东西是一个很容易的陷阱，因此错过了我们主题的整个方面。以逆向计算为例；我们可能会写美国或西欧的机器，因为我们是伴随着它们长大的，而完全忽略了铁幕另一边正在生产的硬件。因此，看到[Marek wi cek]的项目[采用英特尔 8080](https://hackaday.io/project/161333-polon-7880) 的波兰克隆的单板逆向计算机是很有趣的。

在波兰语论坛 ( [谷歌翻译](https://translate.google.com/translate?sl=auto&tl=en&u=https%3A%2F%2Fforbot.pl%2Fforum%2Ftopic%2F13083-polon-7880-jednoplytkowy-komputer-w-stylu-retro%2F))上，他讲述了一个故事，他收到了一个 MCY7880 CPU 作为他的收藏，只是想知道它是否可以单独制成一台机器。作为 8080 的克隆，这也需要相当于英特尔总线控制器和时钟发生器芯片，我们猜测必须是 UCY74S405 和 UCY7404，他也是该项目的来源。

构建以真正的复古风格完成，在原型板的背面有一个点对点布线的迷宫，他在板上放置了一个 TinyBASIC 解释器端口和 8251 UART，以及一个用于一些 GPIO 操作的 8255 三并行 I/O 端口。我们热爱这台电脑，欣赏它照亮微处理器历史上一个不为人知的角落。

如果东欧逆向计算是你的事情，在 Hackaday，我们很幸运地在我们的同事中找到了这个问题的权威。[Voja Antonic]向我们讲述了他如何设计南斯拉夫第一台家用电脑 Galaksija 的故事。遗憾的是，他在设计中没有使用波兰 8080。