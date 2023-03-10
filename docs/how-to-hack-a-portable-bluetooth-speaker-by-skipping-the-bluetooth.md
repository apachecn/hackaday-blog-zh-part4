# 如何通过跳过蓝牙来破解便携式蓝牙音箱

> 原文：<https://hackaday.com/2020/02/04/how-to-hack-a-portable-bluetooth-speaker-by-skipping-the-bluetooth/>

便携式蓝牙扬声器已经加入了无处不在的个人电子产品俱乐部。由于制造商大量生产扬声器以满足各种口味和预算，曾经昂贵的奢侈品现在变得随处可见。有些甚至成为品牌促销赠品。因此，如今拥有一个小型的黑客收藏并不罕见，这是黑客攻击的沃土。

但许多多余的扬声器被放在架子上“以后用它做点什么”，只是为了收集灰尘。我们的主要障碍是市场多样性的一个副作用:有这么多不同的演讲者，针对一个演讲者的黑客攻击并不适用于另一个演讲者。一些扬声器适合定制固件，但只有一小部分吸引了软件开发社区。大多数蓝牙音频模块是不透明的，它们的开发工具链很难获得，这并没有帮助。

那么，如果我们只是利用这些扬声器的最佳部分:出色的音频保真度、便携性和消费品的精美外观，来充当我们自己的音频黑客的主机，会怎么样呢？让我们把蓝牙扔出船外，但拥抱所有其他的东西。现在破解这些盒子只需要改变思维方式和一点侦查工作。我将向您展示如何将 Arduino 放入一个便宜的扬声器中，作为您自己音频冒险的蓝图。

## 将黑客思维引向无数蓝牙音箱

[![](img/dac6bf138a8659f228ec6423d1397308.png)](https://hackaday.com/wp-content/uploads/2020/01/BSH050-open-case.jpg)

有太多不同的演讲者，一个黑客无法统治所有人。但通过将我们的蓝牙音箱思维模式从“这是一台可重新编程的计算机”转变为“这是一个有用的电子元件的集成集合”，我们将市场多样性变成了我们的盟友。

从蓝牙扬声器制造商的角度来看这个问题:他们希望他们的蓝牙扬声器从竞争对手中脱颖而出，最明显的方式是在他们对扬声器驱动器的选择上。用小盒子里的大声音给客户带来惊喜是成功的关键，因此每款产品都可以提供独特的音频驱动组合，所有这些都装在一个引人注目的外壳中，让消费者能够区分不同的便携式蓝牙扬声器。

定制扬声器选择对系统的其余部分具有级联效应。为了获得最佳声音，他们需要匹配的音频放大器模块，这些模块有自己的功率要求，决定电池性能等等。为了迎合这些欲望，组件被排除在紧密集成的神秘黑匣子之外。对硬件黑客来说幸运的是，这样的架构也使得组件易于重用:

1.  可充电电池。
2.  能够从 USB 给电池充电。
3.  一种低功耗待机模式，用于监控电源按钮的按下情况。
4.  保护电池免于过度放电。
5.  向设备提供电池电源的电压调节器。
6.  音频线路输入插孔。
7.  音量调高/调低控制。
8.  放大器和驱动器。

所有这些对项目都是有用的，已经整齐地包装在大规模生产的外壳中。

## 用一个例子把理论付诸实践

现在我们有了一个大致的背景，让我们将这个概念应用到一个具体的例子中。但在我们开始之前，有一个必须注意的事项，以防对任何阅读本文的初学者来说不明显:这个活动 ***非常肯定*** 会使保修失效(做吧，这是值得的！)，现代便携式电子产品使用[锂化学电池](https://hackaday.com/2020/01/07/choosing-the-right-battery-for-your-electric-vehicle-build/)，如果使用不当可能会有危险。

 [![Portable Bluetooth speaker with rubber surround.](img/3921992c845e9739657b80f4ab1c49c4.png "BSH00 Speaker")](https://hackaday.com/2020/02/04/how-to-hack-a-portable-bluetooth-speaker-by-skipping-the-bluetooth/bsh00-speaker/) Portable Bluetooth speaker with rubber surround. [![Peel back rubber surround.](img/dd8e703145050c702c9820633d84e153.png "BSH010 Pull back surround")](https://hackaday.com/2020/02/04/how-to-hack-a-portable-bluetooth-speaker-by-skipping-the-bluetooth/bsh010-pull-back-surround/) Peel back rubber surround. [![Pry off speaker grille.](img/61b7b3b03c6ba43753b1ae4ec29528c4.png "BSH020 remove grille")](https://hackaday.com/2020/02/04/how-to-hack-a-portable-bluetooth-speaker-by-skipping-the-bluetooth/bsh020-remove-grille/) Pry off speaker grille. [![Remove 5 screws holding halves together.](img/6ab54411e7f9c95f6fd54f771455e871.png "BSH030 remove fastener")](https://hackaday.com/2020/02/04/how-to-hack-a-portable-bluetooth-speaker-by-skipping-the-bluetooth/bsh030-remove-fastener/) Remove 5 screws holding halves together. [![Loosened halves allow rubber surround to be removed.](img/f44c1224b9e762ab2d4a0443db31ddd6.png "BSH040 remove surround")](https://hackaday.com/2020/02/04/how-to-hack-a-portable-bluetooth-speaker-by-skipping-the-bluetooth/bsh040-remove-surround/) Loosened halves allow rubber surround to be removed. [![Open two halves of enclosure.](img/738d061a81444e08110577d93484e67d.png "BSH050 open case")](https://hackaday.com/2020/02/04/how-to-hack-a-portable-bluetooth-speaker-by-skipping-the-bluetooth/bsh050-open-case/) Open two halves of enclosure. [![Remove main PCB for further investigation.](img/40ffab9cab1bea9de0ca1d26a3993115.png "BSH060 remove PCB")](https://hackaday.com/2020/02/04/how-to-hack-a-portable-bluetooth-speaker-by-skipping-the-bluetooth/bsh060-remove-pcb/) Remove main PCB for further investigation. [![Main PCB Closeup](img/8e635e1f25dc5860dd7ae3ea982b403d.png "BSH110 PCB closeup")](https://hackaday.com/2020/02/04/how-to-hack-a-portable-bluetooth-speaker-by-skipping-the-bluetooth/bsh110-pcb-closeup-2/) Main PCB Closeup

本例中使用的蓝牙扬声器是北美电子产品零售商 Best Buy 以其自有品牌之一销售的"[Rugged Portable Bluetooth Speaker](https://www.bestbuy.com/site/insignia-rugged-portable-bluetooth-speaker-black/5204300.p?skuId=5204300)"。搜索[的 FCC ID](https://fccid.io/XMF-CSPBTF1) ，发现制造商是 [Lightcomm 科技有限公司](http://www.light-comm.com/en/productinfo-173-190-186.html)。“坚固”的说法始于其外部包裹的一层软橡胶。此外，外壳内部的加固允许扬声器吸收一定程度的滥用。我想保留这种减震的外观，谢天谢地，它很容易无损地打开。如果是防水扬声器(这款不是)，就更需要小心了，还需要防潮。或者，如果计划将内部构件转移到另一个外壳中，那么原包装箱的状况就无关紧要了。

[![](img/cb68761f9d4ef72984c9ebc2afbf74f0.png)](https://hackaday.com/wp-content/uploads/2020/01/BSH120-ATS2823-bluetooth-module-e1580292179288.jpg) 一旦电路板被拔出，蓝牙接口模块将立即成为天线附近最复杂的组件。对 ATS2823 的搜索证实了它是一个为集成到蓝牙音频产品中而设计和销售的模块。它的 MIPS M4K 内核和相关的闪存可能是固件黑客攻击的一个有前途的开始，但这个例子的要点是演示如何利用现有的固件来攻击扬声器。因此，我们将保持该模块不变。

## 焊接到外部音频输入

[![](img/5bfa2fb701bf748e5660979517a93fa3.png)](https://hackaday.com/wp-content/uploads/2020/01/BSH150-audio-input-jack-e1580291822403.jpg) 将音频传输到该系统的最简单方法是伪装成外部音频源。我们希望系统*相信*我们是通过插入线路输入插孔的音频电缆连接的，但为了紧凑起见，我们更喜欢在没有使用实际线缆的情况下*这样做。这种方法简单、无损，并且保留了现有的音量控制机制。有许多不同的方法来实现音频插孔，所以需要使用万用表进行一些探索。我们需要找到标准化的触点:音频输入左声道、右声道和地。(维基百科参考资料:“[手机接口(音频)](https://en.wikipedia.org/wiki/Phone_connector_(audio)#Mono_and_stereo_compatibility)”)*

破译插头检测方案会有点棘手，因为它不是标准化的。在这个特殊的例子中，在没有音频插头的情况下，有第四个引脚悬空。当有音频插头时，针脚接地。将电线焊接到总是接地的检测引脚将使该扬声器始终处于“播放外部音频”模式。

## 或者直接连接到放大器

[![](img/1becad46530b0695a604251fcb6d0e2d.png)](https://hackaday.com/wp-content/uploads/2020/01/BSH130-MIX2052-6W-amplifier.jpg) 另一种方法是绕过现有的输入和音量控制，将音频直接发送到放大器芯片。为了找到这个芯片，我们从音圈线开始回溯。它可能是音圈线附近最大的元件。找到放大器芯片后，查阅数据手册，找到输入引脚，从电路中断开，并为绕过现有控制的音频输入重新布线。

但是即使我们希望保持现有的音量控制，定位音频放大器芯片仍然是有用的。它是电路板上最耗电的元件，系统的峰值功率要求由该放大器在大声播放时消耗的功率决定。因此，这是计算我们可用功率的一半难题。这个特殊的蓝牙设备使用了一个位于音圈线连接器附近的[mixino mix 2052](http://www.mixinno.com/userfiles/productfile/MIX2052.pdf)芯片，峰值功率为 6 瓦。

## 接入电源

难题的另一半是向放大器芯片输送功率的电压调节器。类似于我们在音圈线附近寻找放大器，我们也可以在电感、电容和二极管附近寻找调节器。找到电源模块后，阅读其数据表以确定峰值功率输出。

![](img/7a3ca6b07fb79206bb9f3012435e3641.png)

我们黑客的功率预算将受到这两个组件的功率数字的限制。大多数微控制器在启动时消耗最大功率。因此，只要音频源在此期间保持安静，我们就会有一点额外的功率来支持启动。调节器和放大器之间的某个地方也是获取功率的最佳位置。它允许我们利用现有的电源管理电路，在进入低功耗模式时关闭放大器，同时切断黑客的电源。

在该板的情况下，有一个突出的线圈，旁边有一个 [Techcode TD8208](http://techcodesemi.com/datasheet/TD8208.pdf) 升压调节器。配置为提供 5 伏，这个调节器可以提供 1A，并容忍短暂的尖峰不超过 2A。这不足以喂养一个树莓 Pi 4，但足以喂养一个 Arduino Nano。

## 改变用途控制按钮

[![](img/ad0ca32b099f9cc6594f149e73de7935.png)](https://hackaday.com/wp-content/uploads/2020/01/BSH160-cut-trace-for-SW4-e1580294267919.jpg) 到目前为止，这款音箱上四个按钮中的三个功能都被保留了下来:电源、调高音量和调低音量。第四个按钮启动蓝牙配对，或接听电话。我们将 BT 从等式中剔除，因此它不再有用，可以重新利用。

在这个扬声器上，SW4 通常是打开的，当按下时拉至地，使其可以重复使用。我切断了通向蓝牙接口模块的迹线，并焊接了一根电线，这样开关现在在按下时会将 Arduino 引脚拉到地。

## 把所有东西都塞回去

![](img/1a11445480e88b7ffc7faa1a1428d0c6.png)

一些内部塑料加固材料被切掉，为这个外壳内部的 Arduino Nano 创造了足够的空间。它不再那么坚固，但现在作为一个声音黑客的平台，它要有趣得多。为了结束这个概念验证，Arduino Nano 正在使用 [Mozzi 音频库](https://github.com/sensorium/Mozzi)来播放经典的 [Wilhelm scream](https://github.com/Roger-random/mozzi_wilhelm) 每当我们按下重新利用按钮时。

 <https://hackaday.com/wp-content/uploads/2020/01/Wilhelm-720p.mp4?_=1>

[https://hackaday.com/wp-content/uploads/2020/01/Wilhelm-720p.mp4](https://hackaday.com/wp-content/uploads/2020/01/Wilhelm-720p.mp4)

## 建立自己的 Bleepy Bloopy Buzzy 盒

Bluetooth used to be the novelty. With plenty of hacks [adding Bluetooth](https://hackaday.com/2019/04/20/vintage-radio-gets-a-modern-makeover/) to existing audio equipment, [playing Bluetooth audio](https://hackaday.com/2018/07/23/turn-a-cheap-bluetooth-speaker-into-an-audio-receiver/) out of one, or [building our own](https://hackaday.com/2019/10/07/pvc-pipe-turned-portable-bluetooth-speaker/) Bluetooth speakers from scratch. But now Bluetooth speakers are ubiquitous, we’re approaching the point where Bluetooth is not necessarily the center of attention. Skipping the Bluetooth in a portable Bluetooth speaker gives us a new platform for our noise maker hacks. Something small, fun, and easy to bring to our next hacker show-and-tell meetup!