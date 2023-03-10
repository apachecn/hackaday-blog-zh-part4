# 黄金电缆确实是最好的

> 原文：<https://hackaday.com/2020/04/01/gold-cables-really-do-work-the-best/>

作为一名作家，我长期以来一直梦想有一天，一位编辑会给我买一台顶级的音频分析仪，我可以建立一个音频测试实验室，并撰写文章，驳斥音响发烧友、高保真记者和高端音频行业对其产品质量的虚假断言。那个放大器真的能给更广阔的声场带来尖锐的咝咝声吗？我们能不能用一些可测量的数字而不是华丽的散文来支持它？

## 一个你不知道自己拥有的音频游乐场

[![An Audio Precision APx525 audio analyser.](img/93732d2c46eae52af1485e9cf4ef95db.png)](https://hackaday.com/wp-content/uploads/2020/03/APx525_Audio_Analyzer.jpg)

An Audio Precision APx525 audio analyser. Bradp723 ([CC-BY-SA 3.0](https://commons.wikimedia.org/wiki/File:APx525_Audio_Analyzer.jpg))

遗憾的是，Hackaday 不是一本音频杂志，如果 Mike 给我买了一台 Audio Precision，他也必须满足所有其他作者对测试设备的需求，谁知道这将会在哪里结束！所以暂时不会有黑客音频实验室。但这并不意味着我不能玩音频分析。

上个月，我们发表了一篇关于凯特·特姆金和迈克尔·奥斯曼的超级演讲的文章，他们在文章中提醒我们，我们的眼皮底下有一个开裂的通用 DSP 平台；GNU 电台不仅仅是用来广播的。一旦我看过这个演讲，我的音频分析视野就大大开阔了。也许那个音频分析器不是我的，但是我可以用 GNU Radio 做同样的工作。

在这一点上需要强调的是，我在工作台上所做的任何事情都无法达到专业音频分析仪的质量。但是，即使我不能测量非常高端的音频电路之间的微小差异，我仍然可以测量足以区分好的音频产品和坏的音频产品。

## 用软件无线电制作音频分析器

[![My single-frequency THD+N analayser flowgraph in GNU Radio](img/c191c1b1121608453ed9959c8ece37bc.png)](https://hackaday.com/wp-content/uploads/2020/03/gold-cables-thd-flowgraph.jpg)

My single-frequency THD+N analayser flowgraph in GNU Radio

对于我的替代音频分析仪，我决定保持简单，只测量总谐波失真，或 THD。严格来说，我测量的是总谐波失真加噪声，但在实验中，这与我无关。THD 用百分比表示，通常最好理解为受测器件中因器件失真而产生的信号的百分比。因此，理论上完美的器件总谐波失真为 0%。测量 THD 最简单的方法是在器件输入端注入一个单一频率，然后将输出端滤除该频率后剩余的频率除以输出端的频率成分。这需要一套非常好的滤波器，在模拟电路中是一项艰苦的工作，但在 GNU 无线电中却是一项简单的任务。

[我想出的流程图](https://github.com/JennyList/GnuRadioAudioAnalysers)非常简单:低通滤波器在注入频率以上截止，而高通滤波器在注入频率以上截止，产生谐波。然后，这是一个简单的数学案例，得出我的% THD 读数。

我使用立体声声卡的相反通道作为输入和输出，如果我将它们直接连接在一起，我会检索到 1kHz 输入为 0.0024%的 THD 数字。因此，我测量了一个戴尔声卡的总谐波失真，虽然它没有想象中那么糟糕，但作为比较，一个定位于音响发烧友的设备会有几个额外的前导零。但是当然，我不只是测量声卡的总谐波失真。

虽然理论上 GNU radio 的全数字信号路径是无失真的，但实际上它会引入自己的失真。存在量化失真，以及由滤波器中的缺陷引起的失真，当然还有来自运行多任务桌面操作系统的计算机正在做的任何事情的噪声。一个很好的例子是，当我拍摄流程图的截图时，THD 立即在短时间内增加了 10 倍。有一个很好的理由来解释为什么专业的音频分析器这么贵，以及为什么我们不用普通的声卡来代替它。

## 黄金线缆真的更好吗？

[![For 99 quid this had better be good!](img/59208d7b813252d786296a49ab5175db.png)](https://hackaday.com/wp-content/uploads/2020/03/gold-cables-grundlagen-audio.jpg)

For 99 quid this had better be good!

我有一个音频分析器可以玩，尽管不是很好，我四处寻找一个测试对象来尝试它。显而易见，要做的事情是尝试一个对比测试，因此，为此我投下了几笔电缆订单。高端电缆制造商的声明有任何真实性吗，或者仅仅是为了让消费者远离他们辛苦赚来的钱而设计的蛇油？

我拿起了一对 3 英尺的 USB 电缆，完全不同的市场两端。一种是 4 美元(5 美元)的亚马逊基础电缆，比如你可能正在用来给手机充电的那种，另一种是德国 Grundlagen Audio 的 99 美元(123 美元)的黄金参考系列电缆，其制造商声称，与传统电缆相比，它通过镀金的活性量子纳米粒子结构提供了非常低的数字音频传输总谐波失真。我能做什么，除了把每根电缆依次连接起来，试一试？

开箱后，两种电缆的长度和重量几乎相同，但 Grundlagen 明显比亚马逊电缆更硬。可能所有额外的黄金并不灵活或什么的。我使用了上面链接的流程图，但是用 USB 接收器和源代替了音频接收器和源。我希望 THD 的数字会大大低于这种安排，因为我当然已经从等式中删除了我的低质量声卡。首先是第一根电缆，从 USB 端口到 USB 端口的回环中的 Amazon Basics 电缆开始。很快我就能测量出相当不错的 THD，在 1 kHz 时为 0.00014%，考虑到没有声卡，这并不奇怪。非常好，但是花费二十倍的电缆怎么办？有了 Grundlagen，差异就很明显了，1 kHz 总谐波失真为 0.00007%，是基本电缆的一半。数字那么小，你能听出区别吗？可能不会，但它确实证明了金色电缆比灰色电缆更好，即使它们听起来一样。

Grundlagen 的员工非常友好地与我们分享了一段视频，展示了他们是如何制造电缆的。与此同时，如果你们中的任何人想在 GNU 电台中进一步发展音频分析器的想法，我们洗耳恭听。

 [https://www.youtube.com/embed/P55EWIww_Vs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/P55EWIww_Vs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

