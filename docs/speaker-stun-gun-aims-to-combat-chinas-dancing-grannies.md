# 演讲者“眩晕枪”旨在打击中国的跳舞老奶奶

> 原文：<https://hackaday.com/2021/10/28/speaker-stun-gun-aims-to-combat-chinas-dancing-grannies/>

在中国比较流行的社交活动之一是在公共广场跳集体舞。参与者通常是许多中老年妇女的消遣，他们被通俗地称为“跳舞的老奶奶”虽然这种活动相对有益健康，但一些跳舞者已经开始用他们响亮的音乐引起邻居的愤怒，并试图控制公园和娱乐场所的使用。

自然地，一个有希望解决这个问题的技术解决方案出现了。《南华早报》报道了[的一个“眩晕枪”装置](https://www.scmp.com/news/people-culture/trending-china/article/3151243/chinas-dancing-grannies-viral-stun-gun-claims)，该装置声称可以在远处中和扬声器，试图关闭舞会。该设备在社交媒体上引起了巨大的轰动，以及许多关于它如何工作的问题。这比你想象的要简单，也没那么酷。

## 《消失的电视》的续集

![](img/f9160a7a893c1f0284af7fb3a5914541.png)

Image sourced from a Taobao listing for a anti-square dance device. Note the device is reported as capable of interfering with common outdoor PA systems but not other types of speakers.

很难找到这些设备的具体细节，尤其是在英语世界。易贝和速卖通等面向西方的网站上的商品被删除的速度惊人。这只是增加了一个可以远程关闭音频设备的设备的神秘色彩。

然而，足够深入地挖掘，用一些翻译应用程序武装自己，并与中国的几个朋友交谈，你就会了解真相。这些设备不是什么万能的眩晕枪，不能让说话者屈服。相反，它们只是简单的红外遥控器，内置在一个熟悉的手电筒样式的外壳中。将一个强大的红外 LED 和一个透镜结合起来聚焦光束，意味着这些设备在理想条件下可以发射 50 米以上的红外信号。然后，用正确的信号调制红外 LED 就很简单了。让 LED 与跳舞的老奶奶们使用的普通便携式 PA 扬声器的遥控器所使用的“关闭电源”命令相匹配，您就成功了。

和著名的 [TV-B-Gone 是一个概念。](https://www.tvbgone.com/)TV-B-Gone 本质上是一个十多年前推出的一键通用遥控器，它有一个红外发射器，当你按住按钮时，它可以简单地发出各种流行电视的“关闭”命令。这些扬声器关断装置使用完全相同的方法。唯一的区别是，它们触发代码来关闭便携式扬声器，而不是电视，而且它们内置在一个设计用于更远距离工作的包中。

有趣的是，Hackaday 在年前[推出了一款非常相似的设备。它将一个简单的 TV-B-Gone 红外代码发送器和一个 1 W 的红外 LED 封装在一个紧凑的手电筒外壳中。它是为电视设计的，不是为 PA 系统设计的，但概念是一样的。](https://hackaday.com/2009/10/07/tv-b-gone-zilla-rar/)

![](img/345f64254c4e034b976a22fd714f6194.png)

这些设备在淘宝上很容易找到，比如前几天我们找到的[这些](https://item.taobao.com/item.htm?ut_sk=1.XEVZ/kg0UZwDAAiSVxMzICwN_21380790_1634275636320.Copy.ShareGlobalNavigation_1&id=656351105895&sourceType=item&suid=D666E721-C56E-4AA9-AF5D-A77EA8422262&un=bd75e29b7b09ac7603c6109e527695c7&share_crt_v=1&spm=a2159r.13376460.0.0&sp_tk=VXNqS1hIa2lNdHk=&cpp=1&shareurl=true&short_name=h.feINsZH&bxsign=scdvYF892kemaEDsQCwwXsyfEurrG3aYc-ZMMl8cukZ4a5Cnc6Vzvm1zm5dKCmfZ7fc9arL1T73mMH-3zQt24WztxDbOzUXSGmAD7wsIHzplCA&sm=a7ba28&fbclid=IwAR0CWhG4rnjZ7tkhLK_CXsInE0pGQymnKP-xfi3vq-f153MNV9FWVWFuqZU&app=chrome) [列表](https://item.taobao.com/item.htm?spm=a230r.7195193.1997079397.10.7ded5471nlf4JI&id=644625400919&abbucket=19)。然而，被删除的速卖通列表最诚实地说明了这些设备的工作方式，指出它们只适用于使用红外遥控器的户外 pa。

![](img/5d429ede433b94b8c890904578acce04.png)

Spinning the lens fitting can throw a narrow beam a long way or a wider beam a shorter distance.

一旦人们知道这些装置是如何工作的，对策就显而易见了。一条简单的不透明胶带覆盖在 PA 的红外接收器上就足以使设备失效，代价是失去自己遥控器的功能。

这些设备在西方可能仍然很难找到。政府当局模糊地看待任何作为“干扰器”或“干扰”设备销售的东西，即使这些实际上只是奇怪的遥控器。不清楚他们是否参与了，还是易贝和全球速卖通只是积极主动地删除列表。无论如何，这些设备在中国以外的市场可能很小。

然而，在中国国内，社交媒体上有很多关于最终从定期接管社区的跳舞老奶奶联盟手中夺回控制权的谈论。这些设备是否能有效地给社区带来和平尚不清楚；相反，它们很可能会加剧紧张局势。

无论如何，如果你有一个更好的想法，可以关闭更宽范围的放大器，请在下面分享。或者，给我们你解决老奶奶和邻居之间冲突的最佳方案。中国的和平就靠它了！

*【感谢戴斯勒·邓恩协助研究本文。]*