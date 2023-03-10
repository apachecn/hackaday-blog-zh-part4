# 了解音频:进入最佳状态

> 原文：<https://hackaday.com/2021/11/18/know-audio-get-into-the-groove/>

[![The legendary Technics SL1200 direct-drive turntable, as used by countless DJs. Dydric [CC BY-SA 2.5)], via Wikimedia Commons.](img/e2d3519901dc0d8d27928fd03384aa00.png)](https://hackaday.com/wp-content/uploads/2017/02/640px-technics_sl-1200mk2-2.jpg) 

传说中的工艺 SL1200 直驱转盘，为无数 DJ 所用。[照片由 Dydric 拍摄](https://commons.wikimedia.org/wiki/File:Technics_SL-1200MK2-2.jpg) CC-BY-SA 2.5

对我来说，黑胶唱机是我音频聆听体验的精神家园，可能是因为我是黑胶为王的时代长大的最后一代人。这张 12 英寸的专辑有着全尺寸的封套和丰富的封套音符，曾经是音乐享受不可或缺的一部分，在流媒体时代没有得到充分复制。

像任何成年人一样，当 CD 播放器还是昂贵的奢侈品时，我用一个听起来相当不错的转盘开始了我的高保真之旅。由于近年来新一代人重新发现了黑胶，它再次成为任何音频技术评论的一部分。

我本来会从一个好的转盘的组成部分的完整运行开始这篇文章，但由于[这是我在 2017 年](https://hackaday.com/2017/03/03/record-players-explained-for-the-streaming-generation/)写的一篇文章，是时候调查一些高保真音乐爱好者关于乙烯基录音的说法了。公平地说，在这个领域，很多完全的垃圾都是由应该更了解的人制造出来的，这是我觉得非常有趣的事情。系好安全带。

## 你能说它比 CD 好吗？

去年，[特伦斯·伊登]引起了我的注意，他表演了拆除一个非常便宜的 USB 转盘。他毫不讳言这是一个非常基本的设备，从我的角度来看，我敢肯定，它灵活的塑料结构，低质量的轴承，马达，拾音器和陶瓷墨盒不会提供最好的再现。然而，他的一句话确实吸引了我的目光。

> “任何说黑胶唱片比 CD 好的人都是提线木偶”

它指的是发烧友圈子里的一场长期讨论，即黑胶播放器是否能比 CD 播放器或任何类型的数字录音提供更高的质量。

有多种不同采样率的数字音频格式，包括有损压缩、无损压缩或根本不压缩，但最常见的可能仍是 16 位 44.1 kHz 立体声未压缩 PCM 数据流的 CD 衍生标准。我们都听过从这些溪流中衍生出来的音乐，听起来相当不错。然而，与所有数字化数据一样，它也有一个硬限制，即最大频率是采样率的一半。这被称为[奈奎斯特速率](https://en.wikipedia.org/wiki/Nyquist_rate)，以描述其特征的工程师命名，因此对于 CD 数据流，最大频率为 22.05 kHz。如果你读过[这个系列的第一部分](https://hackaday.com/2021/06/02/know-audio-start-at-the-very-beginning/)，你就会知道人类听觉的频率上限因人而异，但在年龄足够大、有闲钱购买高保真音响的人群中，频率上限很可能是 16 千赫或以下。因此，即使 DAC 安装了低通滤波器，CD 流中仍有足够的范围，足以轻松超越大多数人的范围。

## 也许如果你有十岁小孩的耳朵

[![This is the tympanic membrane of my left ear.](img/2b53fd7d46dd4b779badd3942890dfe4.png)](https://hackaday.com/wp-content/uploads/2021/05/2021-05-19-144604.jpg)

This is the tympanic membrane of my left ear. Can it really sense the presence or absence of ultrasonic frequencies it can’t hear directly?

然而，这并不是故事的结尾，因为一个经验丰富的音响发烧友会告诉你，虽然你不能直接听到 22 kHz 以上的频率，但你可以听到它们对较低频率的贡献的差异，大概是作为混合产品。换句话说，故事是这样的，你听不到他们，但是当他们不在的时候你可以听到。这个特殊兔子洞的问题当然是它变得主观，因此容易受到高保真音响爱好者的夸张。

在过去做了广泛的听力测试后，我知道我可以区分 96 kHz、24 位音频样本和仅具有适当 DAC 和耳机的 CD 质量样本，但在 Hackaday，我们需要*个数字*。可悲的是，像布吕尔&kjr 这样的公司并不出售经过校准的 10 岁儿童作为参考，来通过不受年龄影响的耳朵进行音频分析，所以我们处于推测而非事实的领域。我们知道超出我们听力范围的频率可以被复制，但是他们是否有任何不同还没有定论。

[![My trusty junk-shop record player](img/d317bcb42851fcd177eba6c9f807c9cc.png)](https://hackaday.com/wp-content/uploads/2017/02/record-player-intro-thumbnail.jpg)

My trusty junk-shop record player

黑胶没有采样率。这完全是模拟的，所以如果你用显微镜观察唱片，你看到的是一个波形，理论上它和录音室里歌手或吉他手的波形是一样的。有些描述对以每分钟 33 转的速度通过唱机唱针的乙烯基分子的数量设定了一个采样速率上限，但这可能会再次下降到高保真音响发烧友的疯狂状态。

毫无疑问，黑胶唱片没有 CD 的 22.05 kHz 奈奎斯特频率限制，因此可以录制和复制比这高得多的频率。记录和母带使用一个滤波器来降低低音频率，以阻止唱针跳出凹槽，转盘前置放大器将有一个所谓的“RIAA”滤波器来增强丢失的低音，但理论上就是这样。你可能会认为它解决了，乙烯基可以复制比 CD 更高的频率，并且自动更好，但不出所料，有一个进一步的障碍。即使这些频率存在于黑胶唱片中，它们在你听到的声音中的存在也取决于你的唱机拾取它们的能力。

## 黑胶版本有那些更高的频率吗？

[![Your copy of Sergeant Pepper Will amost certainly be a CD-quality remaster rather than direct from Abbey Road's tape recorders. Josephenus P. Riley, CC BY 2.0.](img/e96fb358a22babcdc27934027679705b.png)](https://hackaday.com/wp-content/uploads/2021/10/Studer_J37_4-track_tape_recorder_1964-1972_Abbey_Road_Studios.jpg)

Your copy of *Sergeant Pepper* will almost certainly be a CD-quality remaster rather than direct from Abbey Road’s tape recorders. Josephenus P. Riley, [CC BY 2.0](https://commons.wikimedia.org/wiki/File:Studer_J37_4-track_tape_recorder_(1964-1972),_Abbey_Road_Studios.jpg).

理论上，黑胶唱片能够比 CD 唱出更高的频率，假设你作为听众有一个足够好的唱机。但我们也发现，除非你是个孩子，否则你可能听不出有什么不同。

然而，黑胶唱片棺材上的最后一颗钉子是，虽然黑胶唱片可能比 CD 能容纳更多的信息，但现实是，这些天来，它是由与其数字对手相同的母带生成的，所以它很可能是从相同的 44.1 kHz、16 位数据流中截取的。也许老式录音可以避免这一点，但你需要考虑录音时录音室里的磁带的频率响应。你听不出你的黑胶唱片和 CD 之间的区别，可能是因为一开始就听不出区别。

可以肯定的是，一个高质量的盒式磁带、唱盘和功放将会带来顶级的听觉体验，相当于一个未压缩的数字流。糟糕的唱盘听起来会很糟糕。所以，如果你还在用你的黑胶唱片，就好好享受吧，毕竟 12 英寸的专辑和它的封面给人的感觉和外观都是一种享受。但是，如果没有一个经过校准的 10 岁儿童作为参考，也许不要做出任何无法证实的断言。

我现在怀疑写完这篇文章后，我的一个朋友会叫我布偶。

接下来，我们将看看磁带录音。到 2021 年，一台磁带走带设备可能不会像以前那样在高保真音响设备中占据同样重要的位置，但即使你从未享受过制作自己的混音带的乐趣，在磁性录音领域仍有数量惊人的技术诀窍等待着你去发现。