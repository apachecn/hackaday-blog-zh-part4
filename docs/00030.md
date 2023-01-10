# 黑客日链接:2018 年 7 月 15 日

> 原文：<https://hackaday.com/2018/07/15/hackaday-links-july-15-2018/>

你试过 Altium CircuitMaker 吗？呃，你可能不应该。EEVBlog fame 的[Dave]通过可靠消息来源告诉我们，电路制造商[通过在高焊盘数电路板上添加随机睡眠](http://www.eevblog.com/forum/altium/busted-altium-deliberately-crippling-circuit-maker/?PHPSESSID=m5vcjio0rcp970tf5hdqindl84)而被故意削弱。论坛上建议的爆笑伪代码是`if ((time.secs % 3) == 0) delayMicroseconds(padCount * ((rand() % 20) + 1));`。现在，这是一个谣言，但是，我想[戴夫]有一些到 Altium 的秘密渠道。此外，这种说法得到了 CircuitStudio 的[文档的支持，其中提到，*“虽然本质上没有‘硬限制’，但该软件已经被设计成不适合用于大型设计。为此，当编辑包含 5000 个焊盘的设计时，PCB 编辑器将开始显示[sic]性能下降。把这记为另一次油炸胜利；Fritzing 不会故意拖慢你的电脑。*](http://documentation.circuitstudio.com/display/CSTU/CircuitStudio+-+((System+Requirements)))

这是对每个人的公开挑战。[据【SexyCyborg】](https://twitter.com/RealSexyCyborg/status/1016509621941387264)报道，XYZPrinting(达芬奇打印机的制造商)正在专利钓鱼。[这项美国专利](https://patents.google.com/patent/US9987802B2/en)被用于将 3D 打印机从亚马逊市场上撤下。问题来了:没人能搞清楚这个专利到底在主张什么。有一些关于多喷嘴，它*可能*是关于减少喷嘴行程，但我得到了一个'快速上床'的感觉。3D 打印专家不知道这项专利要求什么。问题中的打印机是 [Ender 3](https://www.amazon.com/dp/B07BR3F9N6) ，第一个(实际上是第三个……)基于中国的开源硬件认证产品之一，它实际上是目前亚马逊上最畅销的打印机。我正在和 Comgrow(亚马逊上《安德 3》的卖家)谈话，整个情况一团糟。期待不久的更新。

厌倦:国会不应该制定法律…剥夺言论自由。连线:[但是如果那个演讲是一把枪呢？](https://www.wired.com/story/a-landmark-legal-shift-opens-pandoras-box-for-diy-guns/) *《连线》*的安迪·格林伯格提出了计算机代码不是语言的论点，这与过去 30 年的许多法院裁决相反(见伯恩斯坦诉美国)。[这是](https://www.eff.org/document/amicus-brief-34)案件的法庭之友简报。读一下。了解一下。这里有一篇 Stephen Levy 在 1994 年发表的关于出口管制的 PGP 的文章供参考。

比如集成电路和微处理器？你当然知道。喜欢戏剧？哦，男孩，我们有东西给你。大约一周前，ARM 推出了一个名为 RISC-V Basics 的网站(现在不可用，甚至可以从互联网档案中获得，但[你可以在这里尝试一下](https://web.archive.org/web/20180710112443/https://riscv-basics.com/))。它声称要打破基于 capital-O Open RISC-V 指令集的新芯片的记录。事实上，它充满了恐惧、不确定和怀疑。这是 ARM 控股公司试图击倒 RISC-V 架构新贵[的一次尝试，但许多 ARM 工程师不喜欢它](https://gizmodo.com/arm-takes-down-boneheaded-website-attacking-open-source-1827513230)。