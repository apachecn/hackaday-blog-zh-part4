# 好时字体:不是巧克力，矢量字体的起源

> 原文：<https://hackaday.com/2021/03/30/hershey-fonts-not-chocolate-the-origin-of-vector-lettering/>

在过去的几年里，我不断碰到一种叫做好时字体的东西。翻来翻去，我找到了一份 1967 年的政府报告，作者是艾伦·文森特·赫尔希博士。早在 20 世纪 60 年代，他是弗吉尼亚州达尔格伦海军武器实验室的物理学家，研究船体和水之间的相互作用。他的研究得到了[海军军械研究计算器(NORC)](https://en.wikipedia.org/wiki/IBM_Naval_Ordnance_Research_Calculator) 的帮助，该计算器由 IBM 制造，在 1954 年首次安装时是世界上最快的计算机之一。

NORC 的输入输出设备，如穿孔卡片、磁带和行式打印机，是那个时代的典型设备。但是 NORC 也有超高速光学打印机。这种设备最初是由斯特罗姆贝里-卡尔森电信公司为社会安全管理局开发的，目的是将大量数据直接快速打印在缩微胶片上。

[![](img/5701ec7371c7426511fbdee383a1e3e9.png)](https://hackaday.com/2021/03/30/hershey-fonts-not-chocolate-the-origin-of-vector-lettering/ibm-norc-dahlgren/)

IBM NORC at NWL Dahlgren

[![System Diagram of the SC4020 Optical Printer](img/700354996a0483f73ea3354ff78f344f.png)](https://hackaday.com/2021/03/30/hershey-fonts-not-chocolate-the-origin-of-vector-lettering/sc4020-flow-diagram-orange-themed/)

System flow diagram from: [SC4020 Computer Recorder Information Manual](http://www.chilton-computing.org.uk/acl/technology/sc4020/overview.htm) Stromberg-Carlson, August 1964

也许你听说过程序员不耐烦地等待大型机操作员的打印输出的故事？你可能会为你的光学图等更久。因为他们使用胶片，他们需要化学处理成为照片、幻灯片或缩微胶片。尽管有这样的等待时间，打印速度还是比当时的行式打印机快得多:每分钟 7000 行对 150 行。虽然这种打印速度确实令人印象深刻，但在几分之一秒内绘制整个图表的能力无疑受到了达尔格伦科学家的赞赏。

[![Charactron Tube Diagram](img/b2f9a287df03a9dcb1dbd87d75f184c7.png)](https://hackaday.com/wp-content/uploads/2021/03/charactron-patent-drawing-us2735956-orange-rethemed.png)

Charactron Tube Diagram (US Patent [2735956](https://patents.google.com/patent/US2735956A/en))

是什么让这个设备如此之快？这是我们在 2017 年报道过的[的](https://hackaday.com/2017/12/19/stromberg-carlson-charactron-tube/#more-286248)[电子管](https://en.wikipedia.org/wiki/Charactron)。这种特殊的阴极射线管有一个内部金属屏幕，屏幕上刻有字体。电子束在一次“闪光”中把一个完整的字母投射到显像管的荧光面上，从而使照相胶片曝光。没有光栅扫描或矢量绘图，所以这个过程很快。但是很快这个系统就会以最初设计者想象不到的方式被使用。

## 灵感

回到那个年代，在`roff`、LaTex 和 WYSIWYG 文字处理器出现之前，准备充满复杂数学方程和数据图的技术报告是相当耗时的。文本本身将使用普通打字机准备。但是像 Varityper 这样的专用打字机是用来排版数学方程式的。绘图和数字通常是手绘的或用绘图仪绘制的。赫尔希意识到 NORC 的光学打印机可以扮演一个新的角色，可以用作排字机。赫尔希博士不仅看到了这种可能性，而且对书法有着浓厚的兴趣，并不介意花上几个晚上来开发这种新能力。

![](img/44953dfeb2657ad3be535f0dee602d71.png)

Varityper used for report preparation

实现这一点的关键是定义一种绕过内部模板字体的新输出模式。相反，通过使用句号模板作为“点”来曝光胶片，并在程序控制下移动该点。当应用于文本时，这当然比使用模板慢，但它允许任意选择字体，或 Hershey 博士称之为“库”。此外，它打开了直接在胶片上绘制数据的能力，绕过了当时较慢的笔式绘图仪甚至更慢的手绘技术。

赫尔希博士了解到，新泽西州默里山贝尔实验室的工程师们已经用类似的技术为他们的光学打印机开发了一种字体，从光栅化的角度来看。赫尔希博士意识到，他可以扩展这一概念，以包含更多奇异的艺术符号。他专注于使用矢量来设计他的字体，并开始了研究和建立他的矢量字体集的漫长旅程。

## 适用于所有语言(运动中的龙除外)

事后看来，他不仅构建了一套工具来解决 Dahlgren 社区的需求，还将光学绘图仪的极限推向了极致。在他的报告中，他不仅展示了英语字体，还展示了其他语言的字体，如希腊语、俄语和日语。除了数学符号，他还展示了绘图仪如何绘制电子电路图、星系星图、普通地图、化学键等。在他 1967 年的报告[“计算机书法”](https://books.google.co.kr/books/about/Calligraphy_for_computers.html?id=qFFCAAAAIAAJ&redir_esc=y)中可以找到他彻底性的一个例子。尽管 Hershey 只实现了一部分日本字符作为示范，但他搜索了超过 5000 个日本字符，寻找可能超出他的方法限制的字形。他只能找到一个这样的情况，他合理地决定忽略:

> 在紧凑的空间中省略了一些细节，在复杂的情况下有一些溢出，这种大小[21 个光栅单位的高度]被认为足以容纳《纳尔逊字典》中除第 5444 号以外的所有字符。因为这个角色代表了运动中的龙，所以它的实用性值得怀疑。

[![](img/53a0d164c29c35b5ec2b6ac31764041b.png)](https://hackaday.com/wp-content/uploads/2021/03/hersey-font-sampler.png)

Composite of font charts created by [Paul Bourke](http://paulbourke.net/dataformats/hershey/)

总之，赫尔希博士绘制了大约 1400 个西文和 800 个日文符号，都是在图纸上手工绘制的。有五种不同的光学字体大小和三种不同的笔画类型，更不用说制图、科学、数学等领域使用的各种符号了。

## 好时字体在今天的重要性

好时公司试图利用当时的领先技术为打印报告生成令人满意的字体。到目前为止，最大数量的字形是复杂的——也就是说，它们由多条线或笔画构成，以增加和改变笔画宽度。当你在网上搜索他的字体时，这些笔画经常被描绘成细线，但当正确绘制时，考虑到 SC4020 光束的大小，就会产生实心字母。今天我们有太多的字体供我们使用，那么为什么好时字体还在使用呢？你可能会说，因为它们是公共领域。但最大的原因可能是单笔划字体系列，它在许多不同的应用中仍然非常有用。以下是我这些年遇到的一些例子。

### OpenSCAD(自 2015 年起不再需要)

![](img/91cdf00fec50748b976a0014cb6a9ad0.png)

Technical Lettering Style from 1865 Textbook

今天，如果你想在 OpenSCAD 中绘制文本，有内置的支持。但当我在 2015 年初第一次学习 OpenSCAD 时，这还不可用。我正在做的一个项目需要文本，所以我决定自己做一个。当我使用 OpenSCAD 的图形原语实现简单字体时，我发现这是一项历史悠久的技术。

正是在这个研究过程中，我第一次发现了好时字体。我后来了解到，这些经典的字体风格是好时博士的灵感来源，包括绘图员和一些漫画家使用的 Leroy 字体集。

当时我传了好时字体，因为他们只用线条，看起来真实的曲线会更好看。我基于这些简单的制图字体样式制作了自己的矢量字体，只使用了线条和圆弧——这是我知道如何用 OpenSCAD 制作的东西。现在回过头来看这个，我看到那个文本是在那年 3 月集成到 OpenSCAD 中的。如果我只等三个月，我会节省自己的时间和麻烦。

![](img/36ca04086a3e8c95fd5c942bdff073a2.png)

Leroy Lettering Set

### 前面板字母

![](img/07a7b58316f8d844900556dacdd6997a.png)

Example of Engraved Panel Lettering

作为一名年轻的工程师，我公司的一些项目需要耐用的前面板标记。我们用数控机器在面板上刻字和符号来制作这些。一个行之有效的方法是雕刻一个面板，然后用环氧树脂涂料填充凹槽。今天，我们甚至可以一起跳过机器雕刻的麻烦。低成本的直接激光蚀刻提供了一种更清洁且通常更廉价的技术。这两种方法都是通过沿着由 X-Y 对定义的路径移动头部、铣刀或激光束来工作的。这非常适合矢量字体。通过改变铣削工具的直径或激光束的大小，可以使它们变得更粗或更粗，并且可以根据需要使用基本的三角学很容易地缩放或旋转。试图用位图字体做到这一点，充其量也是笨拙的。

### PCB 插图文字

我们都在 PCB 的丝网印刷层和铜层上写了文字，但也许没有停下来想想细节。当您为制造生成文件时，您的电路板的走线和特征(本身就是向量)以熟悉的 Gerber 格式( [RS-274X](https://en.wikipedia.org/wiki/Gerber_format) )表示。字母也是这样表达的。

![](img/255f990d1f808e7519e652bc0ffdf9de.png)

Gerber 6241 Photoplotter from the early 1980s

20 世纪 60 年代， [Gerber Scentific company](https://en.wikipedia.org/wiki/Gerber_Scientific) 制造了第一台用于制作 PCB 胶片艺术品的光绘机。这个设备是由一系列大型计算机控制的 X-Y 工作台发展而来的。这些最初用于从织物上切割图案和制作处方眼镜镜片等任务。Gerber 光电绘图仪的基本操作与笔式绘图仪或 CNC 雕刻机没有什么不同，只是一束光线会穿过一个可选择的光圈来曝光摄影胶片。包含不同孔径大小的滚轮允许您改变线条宽度，也可用于“闪光”焊盘。矢量命令被用来控制光电绘图仪是很自然的。Gerber 没有重新发明轮子，而是定义了自 20 世纪 50 年代以来一直存在的 CNC 数字接口标准 RS-274D 的子集。经过一些扩展和修改，这仍然是我们今天用来向制造车间传达 PCB 作品的格式。

正如在许多领域一样，技术在不断进步。PCB 制造车间实际上不再使用 Gerber 风格的光绘机了。如今，制造商通常会转换您的 Gerber 文件，以便使用高分辨率、高速光栅打印机将作品转换为胶片。在某些情况下，艺术品直接投影到 PCB 上，完全绕过了胶片和中间转印步骤。

也就是说，我不认为我们会把光栅化的 PCB 作品发给制造商。我们送到商店的 PCB 的特征，走线和焊盘，本质上是固有的矢量。为了获得正确的结果，制造商需要识别这些特征，以便根据他们自己独特的制造工艺来调整它们。这就是制造说明的含义，如“线、焊盘和过孔尺寸规定为最终尺寸”和“受控阻抗走线 xxxx 应为 75 欧姆”。甚至丝网印刷字体的宽度也可能需要根据使用的工艺进行调整。在基于光栅的图像上调整这些参数，虽然不是不可能，但会复杂得多。

#### CAD 工具

![](img/4cb3a5b088e72ced01e06090f532b95f.png)

Hershey Format of the letter H

不久前，我需要为一个客户在 PCB 上放一些韩文。在 KiCad 论坛上讨论过这个问题之后，我了解到在 KiCad 中，PCB 字母以向量的形式存储在内部——使用原始的 Hershey 字体格式。我不会进入[血淋淋的细节](http://paulbourke.net/dataformats/hershey)，但原好时格式是奇特的，至少可以这样说。Hershey 只使用可打印的字母，我们今天可以称之为可打印的 ASCII，以非常紧凑的风格描述坐标。有一个基于字母的笛卡尔网格系统，字母`R`为零。字母`S`是 1，`P`是-2，等等。在这个符号中，字母`H`将显示为`508 9G]KFK[ RYFY[ RKPYP`。

#### TTGO

![](img/825c8365741e394ec2d5f29d70c37c21.png)

TurtlePlotBot Draws Using Hershey Fonts

我最近在基于 ESP32 的 TTGO 模块上玩 Micropython，以便在微小的 TFT 屏幕上试验文本。我发现 Hacakday.io 用户[Russ]在他的[海龟情节机器人](https://hackaday.io/project/174277-turtleplotbot-v3)中使用了[好时字体](https://github.com/russhughes/ttgo-hershey-fonts)。这给了我的一些实验一个很好的开端，也是在现代项目的引擎盖下找到好时字体的又一个例子。

#### 阴极射线管矢量绘图机

![](img/46b7c417aa2174c50f10bd244659c6b1.png)

Oscilloscope Clock Using Hershey Fonts

近年来，使用矢量图形的基于 CRT 的项目变得流行起来。有[时钟项目](https://hackaday.com/2012/11/07/more-crt-fun-with-the-scope-clock/)和[通用矢量显示](https://hackaday.io/project/176054-vdm3-vector-drawing-machine-3)。这是另一个用向量描述字体与显示的底层操作完美匹配的应用。当你得知好时字体在这些项目中很常见时，你不会感到惊讶。例如，[本教程](https://www.nycresistor.com/2012/09/03/vector-display/)由【Trammel Hudson】撰写，介绍矢量显示基础知识，展示如何在屏幕上绘制 Hershey 字体字母。

## 好时的遗产

Hershey 博士会怎么看待他的简单单笔画字体在 60 多年后仍在使用？考虑到他手工精心设计的多笔画字母和日本符号，他可能会有点惊讶，如果不是失望的话。如果您在项目中遇到或使用了好时的字体，请告诉我们。如果你想了解更多，这里有一个由 Frank Grieß hammer 做的关于 Hershey 博士本人及其字体发展的有趣演示。

[https://player.vimeo.com/video/178015110](https://player.vimeo.com/video/178015110)