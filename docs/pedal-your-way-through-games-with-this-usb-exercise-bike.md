# 使用这款 USB 健身车，在游戏中尽情骑行

> 原文：<https://hackaday.com/2022/12/26/pedal-your-way-through-games-with-this-usb-exercise-bike/>

如果你喜欢骑自行车，没有什么比在开阔的道路上感受风吹过头发更好的了。不幸的是，气候条件使得这在一年中的某些时候不舒服或不可能，所以你可能会忍不住呆在家里玩电子游戏。幸运的是，多亏了[Patrick]的[健身车游戏控制器](https://twitter.com/KingwoodElectro/status/1551269866425815040)，你现在可以解决游戏问题并保持身材。

[![Two 3D-printed boxes with buttons and joysticks, to be attached to a bike's handlebar](img/9141f45d57e87a89538304dddd57ef3e.png)](https://hackaday.com/wp-content/uploads/2022/12/Exercise-bike-game-controller-pads.jpg)【Patrick】给自己弄了一辆二手健身车，发现里面的速度传感器是基于磁铁和簧片继电器，就像普通的自行车电脑一样。因此，读取传感器就像使用 Arduino Leonardo 计数脉冲一样简单，USB HID 协议可以轻松地将循环机制转变为一维游戏控制器。

然后，他添加了两个 3D 打印的车把安装游戏手柄，每侧都有几个按钮和一个拇指操纵杆，从而完成了设置。整个系统现在作为一个普通的游戏手柄工作，但可以选择使用自行车作为前进/后退控制。

我们可以想象，这个系统将比任何现成的互联网连接的健身车更有趣，因为你可以将它与基本上任何游戏相连接。[Patrick]使用第一人称射击游戏演示了他的装备，如 *Doom* 和 *Team Fortress 2* ，但可能性是无限的:将 *FIFA* 游戏变成自行车马球游戏怎么样？还是*镜之刃*变成自行车快递员冒险？毕竟，我们已经看到了类似的游戏控制器如何将*侠盗猎车手*变成[更像*侠盗自行车*](https://hackaday.com/2022/01/25/exercise-bike-hacked-as-input-for-xbox-360/) 的东西。

> 实现了蒸汽兼容性。现在我可以一边玩 TF2[@ TooftyTV](https://twitter.com/TooftyTV?ref_src=twsrc%5Etfw)[@ Dane ncle](https://twitter.com/DaneUncle?ref_src=twsrc%5Etfw)[@ valve software](https://twitter.com/valvesoftware?ref_src=twsrc%5Etfw)[@ steam](https://twitter.com/Steam?ref_src=twsrc%5Etfw)[@ peloton](https://twitter.com/peloton?ref_src=twsrc%5Etfw)[#游戏化](https://twitter.com/hashtag/gamification?src=hash&ref_src=twsrc%5Etfw)[#健身](https://twitter.com/hashtag/fitness?src=hash&ref_src=twsrc%5Etfw)[# teamfortress 2](https://twitter.com/hashtag/TeamFortress2?src=hash&ref_src=twsrc%5Etfw)[pic.twitter.com/z0raTSV2Hw](https://t.co/z0raTSV2Hw)
> 
> —金木科技(@金木电子)[2022 年 7 月 24 日](https://twitter.com/KingwoodElectro/status/1551269866425815040?ref_src=twsrc%5Etfw)