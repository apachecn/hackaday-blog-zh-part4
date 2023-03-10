# 3D 打印的铝热剂带来了热量和安全

> 原文：<https://hackaday.com/2020/09/10/3d-printed-thermite-brings-the-heat-and-the-safety/>

铝热剂是一把双刃剑。铝热剂具有巨大的能量密度，并渴望在点燃时产生巨大的热量，非常适合焊接火车轨道。但有时你可能会寻找更多一点的技巧。一种 3D 打印铝热剂的新方法也许能够驯服这头野兽。

我们大多数人都是在舒适的室内安全地坐着进行焊接的。我们可能面临的最大危险是烧伤指尖、忘记热收缩或意外释放烟雾怪物。但是在我们的家庭和工作室之外，有很多极端的金属连接正在进行。无论在哪里进行，现场焊接和铜焊都需要大量的设备，其中一些设备很笨重，在恶劣的条件下甚至更难移动。

[![](img/d7569bea353615bad6ce6227ae0b75da.png)](https://hackaday.com/wp-content/uploads/2020/08/thermite-welcing-cropped.jpg)

Welding railroad tracks with thermite. Image via [YouTube](https://www.youtube.com/watch?v=5uxsFglz2ig)

铜焊的实用性受到支撑它所需的所有复杂硬件支架的限制。这个限制因素和[铝热剂](https://en.wikipedia.org/wiki/Thermite)的发现导致了[放热焊接](https://hackaday.com/2020/07/30/enjoying-some-exothermic-welding-with-thermite/)，它使用高能材料提供足够的热量来熔化填充金属并连接零件。含能材料可以储存大量化学能，并在短时间内强行释放出来。

铝热剂由金属氧化物和金属粉末制成，通常是氧化铁和铝。当被高热源点燃时，铝热剂化合物经历放热的还原-氧化(氧化还原)反应，因为铝减少了氧化铁原子中的电子数。更多的热量使反应进行得更快，产生更多的热量，等等。结果是铁水和氧化铝渣。

铝热剂最初的用途之一是连接铁路轨道，今天它仍被用于这一目的。这里有一个铝热剂焊接过程的视频。

 [https://www.youtube.com/embed/5uxsFglz2ig?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/5uxsFglz2ig?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



铝热剂很危险，因为它产生极高的热量，但它有很多好处。首先，它擅长连接不同的金属。虽然[压接连接非常可靠](https://hackaday.com/2020/04/27/grace-under-pressure-shelley-green-celebrates-crimped-connections/)，但铝热剂接头更坚固，可以承受更高的电压。它很容易用于制作搭接接头——只需用工件制作一个焊料三明治，将铝热剂放在上面，用镁带或每个人对烟火的介绍——火花点燃它。

铝热剂是可预测的可扩展的，因为产生的热输出与铝热剂的质量直接相关。传统上，铝热剂反应是通过改变化学成分来调节的——多一点铁锈，少一点铝粉，直到它达到你想要的效果。这一切都很好，尽管在常规环境下有点危险，比如铺设火车轨道。在像太空、海洋或战场这样的严酷环境中，使用高热的危险要明显得多。

## 可印刷、可编程的热源

[![](img/7d0f6b91a17c701bb2d784652eec450c.png)](https://hackaday.com/wp-content/uploads/2020/08/thermite-prints-cropped.jpg)

Printer and printed thermite paste.

最近，范德比尔特大学的一名机械工程博士生[创造了一种可印刷的 4D 铝热剂浆料](https://phys.org/news/2020-07-d-thermite-welding-space-combat.html)，这种浆料可以使放热焊接更加安全，尤其是在严峻的环境中。

这种糊状物由氧化铁、铝粉和石膏粉制成。当与水混合时，石膏粉将粉末粘结成可印刷的糊状物。即使酒石酸被加入水中，他们也只有不到 45 分钟的时间让它通过打印机——一台连接到 Ultimaker 2+ 的 Discov3ry 1.0 糊剂挤出机。在他们的实验中，[研究小组成功地用这种糊状物融合铝并制作了一个简单的铜搭接接头](https://sci-hub.tw/10.1016/j.mfglet.2020.02.002)。

通过将糊状物打印成精确的之字形和其他他们称为反应材料架构(RMA)的几何形状，该团队能够对铝热反应进行更多的控制。当分布在这些图案中时，铝热剂表现为可编程的热源，燃烧起来更像保险丝，储存、运输和使用起来更安全。

[![](img/469b99a0159250357c9348f4dd6c5746.png)](https://hackaday.com/wp-content/uploads/2020/08/thermite-reactions.jpg)

Arrows indicate direction of initial reaction, and the red circles highlight new ignition points.

选择这些 RMA 的形状是为了研究它们对铝热反应的影响。第一种是简化的之字形，一种拉长的 S 形图案，带有坚硬的直角，用来测量一端点燃时的传播速度。

上面复杂的锯齿形图案旨在研究点燃铝热剂的影响，以弥合间隙并点燃垂直于初始反应燃烧的新部分。第三种架构是一对简单的锯齿形平行放置，但角度很小，用于测试铝热剂反应平行于起始反应的传播。这三个建筑都是在强制通风烘箱中打印和固化的，然后点燃并用配备有焊接灯罩的高速摄像机拍摄。

有许多接合应用将受益于这种可控热源。水下或空间焊接的铝热剂结构可以提前设计和打印，然后远程点燃，从而节省资金、设备费用和潜在的几条生命。

我们已经看到了一些铝热剂黑客在我们的日子里，其中许多是破坏性的，而不是建设性的。因为铝热剂不是你能在商店买到的东西，所以[从阅读食谱](https://hackaday.com/2016/09/21/copper-thermite-explodes-and-smolders-successfully/)开始。