# 自由空间基金会评论软件无线电

> 原文：<https://hackaday.com/2020/04/08/the-esa-reviews-software-defined-radios/>

如果您想通过软件定义无线电(SDR)更上一层楼，有很多选择。RTL-SDR 加密狗很好，但如果你认真对待，你可能会想要别的东西。你如何选择？嗯，你在欧洲航天局的朋友们已经发表了一篇论文[比较了许多常见的选择](https://gitlab.com/librespacefoundation/sdrmakerspace/sdreval/-/raw/master/Report/pdf/Evaluation_of_SDR_Boards-1.0.pdf)。诚然，他们主要是在研究接收器如何与立方体卫星配合工作，但这仍然是一个很好的比较。

他们检查的设备有:

*   RTS-SDR v3
*   迷你飞机
*   SDRPlay RSPduo
*   LimeSDR Mini
*   刀片式服务器 2.0 微米
*   埃图斯·USRP B210
*   冥王星 SDR

他们研究了几个感兴趣的波段，但没有研究高频波段——考虑到一些设备甚至不能在高频下工作，这并不奇怪。他们确实检查了 VHF、UHF、L 波段、S 波段和 C 波段的性能。一些 SDR 具有传输功能，对于这些设备，他们测试了传输功能和接收功能。

这篇评论不仅仅是主观的。他们计算噪声系数和动态范围，以及其他技术参数。它们还包括用于测试设置的 GNURadio 流程图，如果您想自己进行这些类型的测量，这将是一个很好的起点。

在这份 134 页的报告的末尾，是对 SDR 软件以及如何支持主板的评估。我们将让您阅读该论文的结论，但没有明确的赢家或输家，尽管他们确实提到了 SDRPlay 的封闭源代码如何限制了某些应用程序的软件支持。

即使报告提出了建议，你也需要根据自己的需要调整他们的建议。例如，如果您想使用 HF 频率，许多电路板需要一个上变频器，但并非所有电路板都需要。每个人的需求都有点不一样。

如果你对 GNURadio 感兴趣，试试[我们的教程](https://hackaday.com/2015/11/11/getting-started-with-gnu-radio/)。我们很快会谈论更多关于 PlutoSDR 的内容，但在那之前，你可能会[喜欢这本免费的书](https://hackaday.com/2018/06/29/free-e-book-software-defined-radio-for-engineers/)。

很高兴看到自由太空基金会蓬勃发展。在[SatNOGs 项目早在 2014 年就赢得了最初的 Hackaday 奖](https://hackaday.com/2015/02/19/ground-stations-are-just-the-beginning-the-satnogs-story/)之后，他们用赢得的奖金成立了自由空间基金会，这是一个非营利组织，专注于让开放源代码空间技术广泛可用。这是那项任务的完美延续！