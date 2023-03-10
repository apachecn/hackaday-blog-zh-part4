# 迷你游戏机革命，以及为什么黑客错过了他们

> 原文：<https://hackaday.com/2020/08/27/the-mini-console-revolution-and-why-hackers-passed-them-by/>

树莓派最初是作为一种教育工具开发的。凭借其低廉的价格和数字 IO，它很快成为黑客的最爱。它还配备了足够的电源，可以作为一个紧凑的仿真平台，供任何足够聪明的人在 SD 卡上加载一些 rom。

视频游戏巨头们并没有对此视而不见，他们意识到经典游戏仍有市场。再加上互联网对任何小巧可爱的东西的喜爱，市场已经为微型复古游戏机的发布做好了准备。

这些设备通常在发布后很快售罄，由于体验质量和盒子中包含的游戏，这些设备有时会受到不同的欢迎。随着如此多的人将 Pi 变成了一台复古游戏机，这些为同样目的而建造的迷你游戏机应该会立即受到硬件黑客的喜爱，对吗？发生了什么事？

## 模拟所有内容

![](img/a29d2d136dcc8e63d8c9951209dfd13a.png)

Nintendo fired the first salvo in the mini console wars in late 2016.

在市场上打响的第一炮是 2016 年底推出的 NES 经典版。它迅速占领了市场，在头六个月售出了 230 万台。出货量几乎立即售罄，许多设备在易贝以标价的倍数被倒卖，成功率各不相同。

该设备表明，低价的经典游戏机再版有着巨大的市场。这是通过使用仿真实现的，而不是重现 NES 定制的硬件或使用类似于芯片上的任天堂的东西。该系统的核心是一个四核 Allwinner R16 ARM Cortex-A7，配备了 256MB 内存和 512MB 闪存。这足以模仿经典的 NES 游戏，也有足够的空间玩很多游戏。除了玩模拟游戏的人之外，也不乏[人入侵 NES 经典游戏，看看是什么让它运行](https://hackaday.com/2016/11/13/linux-on-your-nes-classic-edition/)。

这种模式非常成功，任天堂将相同的硬件装在新的外壳中，并在一年后推出了超级 NES 经典版。其他制造商争相为他们自己的过期商品目录提供类似的机器。世嘉推出了 Genesis Mini，Konami 放弃了 TurboGrafx 16 Mini，这两款产品都基于 ZUIKI Z7213，与任天堂的产品规格相似。索尼的 Playstation Classic 在某种程度上加大了赌注，需要更多的功率和存储来处理 CD-ROM 时代的 3D 游戏。它配备了 16GB 的存储空间和 1GB 的内存，运行的是联发科 MT8167A。后来，同样的概念又有了新的发展，比如 64Mini，甚至是 NeoGeo Mini，它装在一个小小的拱廊橱柜里，配有一个 3.5 英寸的液晶显示屏。

## 能力

没过多久，大胆的黑客们就破解了这些机器；在 NES 迷你发布后的几个月内，向 NES 迷你添加更多游戏的指南就在网上发布了。迄今为止发布的大多数系统(如果不是全部的话)都有类似的方法。有些，像 64 Mini，甚至正式欢迎用户添加更多的软件，这些软件本应成为所有这些重新发行的系统的标准。

![](img/444fdd5fa6ecd651b544ccd4b84be57d.png)

Most hacks have focused on adding more games to the consoles, or running RetroArch to enable the emulation of many different consoles.

然而，除了运行一套不同的 rom 之外，还有更多的东西摆在桌面上。包装 ARM 处理器，闪存和 HDMI 输出，他们有一个小型单板计算机的气质。虽然有些只有有限的接口，但许多也有 USB 端口，使得连接外设理论上很容易。10 年前，这些可能是黑客们为各种项目开发的诱人机器。然而，在一个树莓 Pis 售价低于 50 美元的世界里，很难证明将这些机器转变为更成熟的平台所需的努力是合理的。

到目前为止，努力几乎完全集中在游戏上。不满足于从有问题的系统中加载更多的游戏，黑客们已经将 RetroArch 模拟器移植到这些微控制台上。这使得 ARM 系统能够模拟各种各样的系统，从家用游戏机时代的黎明一直到 Gamecube 和 Wii 等现代游戏机，只要系统有能力这样做。

在 NES 和 SNES mini 上使用一个名为 hacki 的工具来实现回溯，讽刺的是在某些情况下， [SNES 经典版模拟 Playstation 游戏比 PS 经典版更好](https://hackaday.com/2018/12/23/nintendo-does-sony-better-than-sony/)。由于缺乏 USB 端口，Wii Classic 控制器是那些寻求合适的模拟棒用于任天堂迷你游戏机的人的唯一可行的选择。

在 Playstation Classic 的情况下，运行 Retroarch 是通过 BleemSync 实现的，bleem sync 以最初的 Playstation 模拟器[或后来的厄里斯项目](https://www.youtube.com/watch?v=sSBsn4ZKzJg)命名。据报道，[它也比索尼的内部模拟器](https://hardforum.com/threads/playstation-classic-with-retroarch-runs-games-better-than-the-stock-emulator.1974353/)运行得更好，这可能部分是由于[决定在原型机上包括 PAL 端口。](https://www.eurogamer.net/articles/digitalfoundry-2018-playstation-classic-emulation-first-look)

## 结论

![](img/6818c6b72706976a858089b737b5112e.png)

What started as the Xbox Media Center was then ported to the Raspberry Pi and other platforms. Our own Mike Szczys [called in 2012](https://hackaday.com/2012/11/19/raspberry-pi-reaches-critical-mass-as-xbmc-hardware/) for “a streaming media device that could just be stuck to the back of a television.” These days, such devices are commonplace.

对于那些想要一个仿真系统的人来说，任天堂和索尼的产品可能很有吸引力。然而，对大多数人来说，使用黑客工具和控制器限制的大惊小怪可能会被证明过于繁琐，当替代方法是简单地在一个漂亮的塑料复制品中拍打树莓皮。虽然这些系统在很大程度上已经被黑客破解，但人们并不渴望在这些平台上运行完整的桌面操作系统或其他代码。单板计算机便宜且数量充足，所以没有什么动力去为一台哪怕是限制最少的计算机而烦恼。

这与这个网站诞生的时代截然不同。在 21 世纪初，torrents 占主导地位，很少有设备适合在电视屏幕上播放数字视频内容。[Xbox 是一个主要目标，](https://hackaday.com/2018/11/19/how-the-xbox-was-hacked/)以 USB、以太网和 x86 芯片为特色，所有这些都在一个适合电视的包装中。Xbox Media Centre 项目(今天仍然存在，但更名为 KODI)甚至完整的 Linux 发行版都迅速涌现出来，成为世界各地黑客的休息室。由于能够做一些现成产品无法轻易做到的事情，大量的时间被投入到平台开发中。

就这些微型游戏机而言，它们能做的事情很少，其他硬件不能做得更好。即使他们玩复古游戏的主要角色也可以在树莓 Pi 上得到更好的体验，即使是对技术缺乏经验的人来说。最终，制造商出售的是装在可爱塑料盒里的怀旧产品，我认为这种时尚不会持续太久。一如既往，时间会证明一切。