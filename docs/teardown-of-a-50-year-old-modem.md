# 拆除 50 年历史的调制解调器

> 原文：<https://hackaday.com/2019/03/29/teardown-of-a-50-year-old-modem/>

几年前，我在加利福尼亚州雷东多海滩诺斯罗普·格鲁曼公司的停车场参加了 W6TRW 交易会。一个小木箱藏在形似北极熊的电视机、种类繁多的手机充电器和壁瘤之间。有一个门闩，一个木柄，旁边还有一个 DB-25 接口。有一个半双工和全双工的开关。我知道这是什么。这是一个调制解调器。木制调制解调器。具体来说，1965 年左右的利弗莫尔数据系统声学耦合调制解调器。

[![](img/84819a8f911acd0646d8707a963ce500.png)](https://hackaday.com/wp-content/uploads/2019/03/16231454431657034.png)

The Livermore Data Systems Modem, where I found it. It cost me $20

知道声学耦合调制解调器是什么样子的概率与知道堡垒之夜是什么成反比，所以对于任何阅读这篇文章但不知道我在说什么的人，我将详细说明。在 WiFi、以太网、电缆调制解调器和光纤无处不在之前，你通过电话线连接互联网和宽带。调制解调器将数字数据(在这种情况下是串行连接)转换为模拟数据或声音。哦，对了，我们也有电话线。你房子里的电话线*和电话*都属于 AT & T。是的，你从电话公司租了一部电话。

90 年代的孩子可能记得将美国机器人调制解调器插入你的电脑，然后将 RJ-11 插孔插入调制解调器。当这个木制调制解调器建成时，那是违法的。从 1934 年的通信法案开始，在你家里的电话上附加任何东西都是非法的。这种情况在 1956 年的“嘘电话公司诉美国案”中得到改变，该案裁定你可以机械地给手机的耳机附加一些东西。(在 Hush-A-Phone 的例子中，它是一个小盒子，可以放在烛台电话上，给你更多的隐私。)

1968 年，给美国电话电报公司的设备附加东西的权利再次改变，卡特尔局决定允许任何人通过电子方式将 T2 的东西连接到 T4 电信的网络。这为将 RJ-11 电话插孔直接插入你的计算机打开了大门，但直到 1978 年关税、规格和认证才制定出来。从 1956 年到 1978 年，声学耦合调制解调器是通过电话线发送数据的解决方案。这是对法律体系的破坏。

这使得像我桌子上的这个古老的调制解调器在历史上处于一个奇怪的位置。它的设计、营销和销售都发生在卡特尔局的决定之前，因此不能直接连接到美国电话电报公司的网络。它是在许多我们认为理所当然的集成芯片出现在硅片上之前就被设计出来的。这种调制解调器的第一个版本是在第一个商用调制解调器 Bell 103 调制解调器之后一年左右推出的，是用 13 个左右的晶体管就能实现的一个很好的例子。拆卸的时间到了，我们开始吧。

## 以前的作品和参考文献

这种调制解调器的现代历史可以追溯到近十年前,[phreakmonkey]的一个视频，IBM 工程师的遗孀给了他一个 Livermore Data Systems Model 调制解调器。这最终成为 YouTube 上非常受欢迎的视频，并成为 Defcon 17 上的演讲。

从[preakmonkey]的调制解调器演示中可以看出，他的调制解调器是非常早期的型号，序列号为 200 多。据我所知，他的木箱是胡桃木做的，有燕尾榫接头。根据【preakmonkey】的说法，木盒上的接头类型会告诉你有多老；燕尾榫是劳动密集型的，第一个生产单元并没有针对生产进行优化。后来的单位，大约序列号 850，使用柚木盒接头，比燕尾榫更适合大规模生产。还有后来的单位，比如我的单位，在所有的关节上都用了榫头。这是生产过程中的一个明显的优化，允许利弗莫尔数据系统更快地生产更多的调制解调器。

[![](img/255254728d23a1052242ea28523c73b2.png)](https://hackaday.com/wp-content/uploads/2019/03/modemtransistors.png) 这个调制解调器之前已经解剖过了；2007 年，[Brent Hilpert]发现这些调制解调器中有一个是多余的，[记录了内部情况](http://madrona.ca/e/LDSA/index.html)。这个示意图特别有趣。这个调制解调器中有 13 个独立的晶体管，都是相对标准的现代 PNP 和 NPN 通用晶体管的混合。有一个锗 PNP 晶体管，我不知道是什么原因，但大多数情况下，这些组件是标准的，现成的项目，仍然可以作为新的老股票。今天你可以用不到 20 美元买到制造这个调制解调器的所有晶体管。如果你想建造自己的声学调制解调器，你会在微型变压器上花更多的钱。

## 真正的拆卸

除了缺少声学耦合器之外，这个调制解调器或多或少与文档和参考资料告诉我的完全一样。有一个各种各样的背板，容纳三张卡。一张卡支持电源(无变压器)，另一张卡支持调制器，另一张卡支持解调器。晶体管日期代码，特别是 2n5138 晶体管的日期代码，是 1969 年第 37 周的。很好。这表明晶体管的生产日期是 1969 年 9 月，以及之后的某个时间。不幸的是，没有办法进一步缩小这个调制解调器的年份，但它完全有可能是在 1970 年之前建造和运输的。

[![](img/dd314a6bb50171b13d2c1db97dc06b3a.png)](https://hackaday.com/wp-content/uploads/2019/03/modemgif.gif)

 [![ModemHeader](img/2cbde42c105c29305cdbc5d3a8123a73.png "ModemHeader")](https://i0.wp.com/hackaday.com/wp-content/uploads/2019/03/modemheader.png?ssl=1)  [![ModemThmb](img/ca864f1c4e530dae2866615cfd7cbf89.png "ModemThmb")](https://i0.wp.com/hackaday.com/wp-content/uploads/2019/03/modemthmb.jpg?ssl=1)  [![Detail of joinery. Notice the rabbet joint](img/c28307ff2325313fed30eb76fd665399.png "RabbetDetail")](https://i0.wp.com/hackaday.com/wp-content/uploads/2019/03/rabbetdetail.jpg?ssl=1) Detail of joinery. Notice the rabbet joint [![ModemFront](img/16fbff277443c44bf1ec67e8fb9726e2.png "ModemFront")](https://i0.wp.com/hackaday.com/wp-content/uploads/2019/03/modemfront.jpg?ssl=1)  [![ModemPanel](img/2f1097abb3bb83964e36aba5b9467057.png "ModemPanel")](https://i0.wp.com/hackaday.com/wp-content/uploads/2019/03/modempanel.jpg?ssl=1)  [![ModemPanelWide](img/d7a1e7ad5837ba0722c7dd88e84d557b.png "ModemPanelWide")](https://i0.wp.com/hackaday.com/wp-content/uploads/2019/03/modempanelwide.jpg?ssl=1)  [![ModemUnderside](img/aad15f4658cce1050c9e7f60c63291e7.png "ModemUnderside")](https://i0.wp.com/hackaday.com/wp-content/uploads/2019/03/modemunderside.jpg?ssl=1)  [![Rabbet](img/af3f4da8affcd8722d74bc25b2a77d6a.png "Rabbet")](https://i0.wp.com/hackaday.com/wp-content/uploads/2019/03/rabbet.png?ssl=1)  [![pwr2](img/fcd9c69fc518b6260d5b7e955c9688e2.png "pwr2")](https://i0.wp.com/hackaday.com/wp-content/uploads/2019/03/pwr2.jpg?ssl=1)  [![backplane](img/9971c5a6b0cc632405ba9b79046cc97d.png "backplane")](https://i0.wp.com/hackaday.com/wp-content/uploads/2019/03/backplane.jpg?ssl=1)  [![demod1](img/422b29ba52234769e80089db6bf233a1.png "demod1")](https://i0.wp.com/hackaday.com/wp-content/uploads/2019/03/demod1.jpg?ssl=1)  [![demod2](img/7e4f5aa4c4ff690a0cd3f9d7c7fe73d4.png "demod2")](https://i0.wp.com/hackaday.com/wp-content/uploads/2019/03/demod2.jpg?ssl=1)  [![mod1](img/98b592e1df7c42a24fc143c2c833dd1c.png "mod1")](https://i0.wp.com/hackaday.com/wp-content/uploads/2019/03/mod1.jpg?ssl=1)  [![mod2](img/cdca8a5d6f45bd736d06142e165f9e6e.png "mod2")](https://i0.wp.com/hackaday.com/wp-content/uploads/2019/03/mod2.jpg?ssl=1)  [![mod3](img/7d5b7783ac983938c11d2bf46954fe36.png "mod3")](https://i0.wp.com/hackaday.com/wp-content/uploads/2019/03/mod3.jpg?ssl=1)  [![mod4](img/a16dfed5338f046a329097eb96f2a24c.png "mod4")](https://i0.wp.com/hackaday.com/wp-content/uploads/2019/03/mod4.jpg?ssl=1)  [![Power1](img/e9bc3ce177e9d329e3cb0042745358f7.png "Power1")](https://i0.wp.com/hackaday.com/wp-content/uploads/2019/03/power1.jpg?ssl=1)  [![pwr1](img/f7cf36eed6b0ccb88cad9c759b3a3c4c.png "pwr1")](https://i0.wp.com/hackaday.com/wp-content/uploads/2019/03/pwr1.jpg?ssl=1) 

## 这东西值得修吗？

我最初对这个调制解调器感兴趣是在一次业余旧货交易会上找到它，只是想拥有它。这是一个木制的调制解调器，我不认为我认识的任何人会尊重它到底有多酷。在 objet d'art 上，存放各种杂物很有用。我考虑过修理或翻新这个调制解调器，但是有一些事情使它不切实际。

第一，没有声学耦合器。我相信，这就是为什么在旧物交换会上没有人意识到它是什么的原因。利弗莫尔数据系统的标志和序列号也贴在声学耦合器上，如果没有这些，你真的不知道你在看什么，除非你对老式计算机博物馆仓库的垃圾堆有深入的了解。但是我可以很容易地 3D 打印一个声学耦合器，这可能很诱人。

其次，这个调制解调器完全没有经过测试，已经有半个世纪的历史了。我保证瓶盖需要更换，碳成分瓶盖不符合规格。我需要重新设计整个设备来修复它，如果我想制作自己的调制解调器，我可以做更好的事情。

最后，如果我想设计自己的调制解调器，我可以[建造一个数据厕所](https://de.wikipedia.org/wiki/Datenklo)。这是 1985 年德国/混沌计算机俱乐部的一个项目，是为了应对德国联邦邮政高度管制的调制解调器而建造的。从设计的角度来看，数据厕所要简单得多，功能也强大得多。它是围绕一个支持高达 1200 波特的 AM7910 芯片构建的，这些芯片仍然可以从通常的在线零售商那里买到。如果我想从头开始构建一个调制解调器，我会这样做，而不是用分立晶体管。

不幸的是，不值得花时间去修复这个古老的木制调制解调器，但一次好的拆卸确实能让我们深入了解在所有东西都有集成电路之前，东西是如何建造的。这是一个好奇的对象，或者至少是，直到我可以为它找到一个声学耦合器。