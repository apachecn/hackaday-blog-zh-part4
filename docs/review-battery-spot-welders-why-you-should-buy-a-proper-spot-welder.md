# 回顾:电池点焊机，为什么你应该买一个适当的点焊机

> 原文：<https://hackaday.com/2021/06/16/review-battery-spot-welders-why-you-should-buy-a-proper-spot-welder/>

制作电池组是我们社区的共同追求，包括将镍条点焊到单个电池的端子上。许多电池包就是用这种方式制造的，使用的是从废弃的笔记本电脑中回收的 18650 个电池。商业电池点焊机做得很好，但有巨大的涌入电流，而且不便宜，所以看到临时解决方案并不罕见，如从微波炉中取出的重绕变压器。不过，还有另一种可能性，廉价模块的形式，承诺使用电池组作为电源也能达到同样的效果。

我无法抗拒让全球电子市场的廉价终端接受娱乐的诱惑，所以我花了 15 英镑(约 20 美元)买了一个“迷你点焊机”，坐下来等邮递员给我送来通常的匿名灰色包裹。

## 这台焊机很有前途…

[![The mini spot welder set up to use, with electrodes held in a vice.](img/2e5a72c4817f92fc0a2bd3a856617e88.png)](https://hackaday.com/wp-content/uploads/2021/05/spot-welder-setup.jpg)

The mini spot welder set up to use, with electrodes held in a vice.

到达的东西似乎很有希望，一个“便携式晶体管微型点焊机”以及一对电池电缆和一些以点焊电极为终端的电缆。

该模块本身是金属支架上的 PCB 夹层，主板上有电力电子设备，子板上有零件号打磨的微控制器和小型有机发光二极管显示器。板上有一些控制按钮和一个电源开关，以及一个脚踏板插座，主板上有螺丝端子，一排笨重的 MOSFETs 和一个大型电解电容器。

与该单元一起的是一组导线，焊接导线端接在一组绝缘导线中，除了它们的尖端铜探针和未端接的电池导线。我安装了一对卷曲眼连接器，以适应我的电池端子。盒子里还有一张纸，上面建议使用哪种电池适合这项任务，这种电池可以归结为一种类似汽车电池的东西。我手头有一个合适的密封铅酸电池，以及几个可疑的 18650 电池，这种电池非常轻便，明显是假的，所以我拿了一小段镍条，开始将电池和镍条焊接在一起。

[![The tips of the electrodes, with a bit of discharge damage visible.](img/fa6af2b3e8272abf7d1eb80c200ccb05.png)](https://hackaday.com/wp-content/uploads/2021/05/spot-weld-electrodes.jpg)

The tips of the electrodes, with a bit of discharge damage visible.

给设备加电并试验按钮，很明显有两种模式:一种是自动模式，当它检测到要焊接的东西时会操作它，另一种是手动模式，通过脚踏开关操作它。我碰巧有另一个设备的脚踏开关，所以选择了那个。

否则会有一个用“E”校准的功率设置，没有解释“E”是什么。事实上，它是根据器件提供的功率脉冲长度来衡量能量的，上电时，它被设置为 5E 范围的低端。

我第一次试着用一只手拿着两个探针，用另一只手将它们用于试纸条和细胞，但我发现自己不够灵巧，无法完成这项工作。伸手拿起一个小台钳，我可以把它们放在合适的位置，这样我就可以靠着它们的尖端握住电池和铝带，并通过脚踏开关操作焊机。

## …但收效甚微

![This was the best the device could do to my test subjects.](img/4f92a82c220785b4e3dc6df1bfb4d8cc.png)

This was the best the device could do to my test subjects.

从 5E 开始，并开始寻找设备可以成功点焊的点，我在 5E 的步骤中增加功率，并尝试在每个级别进行焊接。较低的水平使这两个粘在一起，但只有一点，我可以很容易地把他们分开，所以我继续。可悲的是，我从来没有找到它工作的水平，因为在 25E 时，那些 MOSFETs 中的一个没有短路，带有通常的魔法烟雾气味，我无法继续。

审查这种类型的非常便宜的电子产品的过程有点像玩独臂土匪。有时你赢得了头奖，但在其他时候，该设备被证明是未经雕琢的钻石。虽然通常情况下，它至少能完成工作，尽管是以一种令人愉快的糟糕方式，所以在我设法让它执行之前，它就失败了，这种情况特别令人失望。

很明显，[电池 MOSFET 点焊机](https://hackaday.com/2017/09/16/a-battery-tab-welder-with-real-control-issues/)的想法有些道理，但这些廉价的设备似乎并没有实现。如果你需要焊接电池端子，找一个更传统的点焊机，同时关于这些电池:我买了一个，所以你不必。