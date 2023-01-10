# 捡起球，带着它跑

> 原文：<https://hackaday.com/2021/09/11/pick-up-the-ball-and-run-with-it/>

偶尔，我们会看到人们是如何以意想不到的有趣的方式在彼此的工作基础上发展的。GateBoy 项目也是如此，这是一个从原始 Game Boy 处理器的芯片构建的门级仿真器。问题是，[奥斯汀·艾波]不需要从芯片的拆封和拍照开始。他甚至不需要通过逆向工程来制作自己的结构图。其他人已经完成了这项工作，并提供给其他人使用。几年前，[furtek]开始手动追踪 DMG 芯片，[发布了 DMG CPU 内部回购](https://github.com/furrtek/DMG-CPU-Inside/)的示意图，友好地授权它为 CC-BY-SA 4.0，让人们知道他们可以如何使用这些信息。

但是玩游戏机实际上并不是[奥斯汀]一丝不苟的关卡娱乐的最终目的。他用它来构建“一套编程工具，可以在软件使用的 C/C++世界和硬件使用的 Verilog/VHDL 世界之间架起桥梁。”一种新的工具已经诞生，不是为了游戏，而是为了转换一种元语言，这种元语言将四个字母的代码分配给门结构(有点让人想起 DNA 序列)，并最终将它们转换为您选择的 C++或用于 FPGAs 的硬件描述语言。

开源社区在踢四维足球。每个项目都将球向前推进，但其中一些项目在另一个硬件世界中增加了一个额外的目标——推进两者的目标(比如找到并修复[furtek]原始示意图中的一些错误)。

当然，真正的挑战是让人们知道这些项目的存在，并且对你正在做的事情有用。例如，[【Neumi 的】深度探测划艇](https://hackaday.com/2021/09/06/homebrew-sounder-maps-the-depths-in-depth/)允许个人制作湖泊、河流等的详细深度图。在评论中,[提到了 OpenSeaMap 项目](http://www.openseamap.org/index.php?id=openseamap&L=1)——一个致力于创建众包航道图的网站。这是[Neumi]获得灵感并帮助将球推向一系列目标的完美地方。

我们如何把这个消息传出去，让更多这样的联系发生？我们会在 Hackaday 尽我们的一份力。但是，首先是那些文档完善、经过深思熟虑许可的项目建立了竞争环境。

This article is part of the Hackaday.com newsletter, delivered every seven days for each of the last 200+ weeks. It also includes our favorite articles from the last seven days that you can see on [the web version of the newsletter](https://mailchi.mp/hackaday.com/hackaday-newsletter-649368). Want this type of article to hit your inbox every Friday morning? [You should sign up](http://eepurl.com/gTMxQf)!