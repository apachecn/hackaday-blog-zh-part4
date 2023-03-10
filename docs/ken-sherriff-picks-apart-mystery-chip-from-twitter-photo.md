# [Ken Shirriff]从推特照片中挑出神秘芯片

> 原文：<https://hackaday.com/2021/04/25/ken-sherriff-picks-apart-mystery-chip-from-twitter-photo/>

众所周知,[Ken Shirriff]的作品经常出现在 Hackaday 的头版。他又回来了，这次[从推特](http://www.righto.com/2021/04/reverse-engineering-vintage-comparator.html)上的一张照片逆向工程出一个比较器芯片。神秘的芯片被打开盖子，在显微镜下拍照，随后[在互联网上公开呼吁弄清楚它做了什么。](https://twitter.com/EvilMnkyzDsignz/status/1381991092929761284)

[![](img/23296dc7742cfe270c37eed7a08c6527.png)](https://hackaday.com/wp-content/uploads/2021/04/ken-sherrif-circuit-labeled.jpg) 【肯】加紧了，一眼看去，很明显大部分芯片都没用，同样的电路好像有四份。在识别电阻和不同的晶体管类型后，[Ken]找到了差分对。

差分对构成了大多数运算放大器的核心，通过将它们链接在一起，可以获得足够强的信号，将其视为逻辑信号。根据设计和材料，[Ken]估计该芯片来自 20 世纪 70 年代。鉴于它似乎是 ECL(发射极耦合逻辑)，它可能只是四个比较器。但是，由于两个比较器具有额外的反相输出，仍有一些事情不合理。搜索零件号几乎没有提供任何线索，所以这仍然是一个谜。

我们之前已经报道过[肯]令人难以置信的芯片侦查，比如 1969 年的[夏普 EL-8。](https://hackaday.com/2020/12/29/reverse-engineering-silicon-from-the-first-pocket-calculator/)