# 恢复 5 美元的合成器变得容易，感谢热

> 原文：<https://hackaday.com/2022/07/16/restoring-5-busted-synthesizer-made-easy-thanks-to-thermal/>

在一次车库拍卖中，斯科特·威廉姆森花了 5 美元买了一台罗兰 JV-30 合成器。得分！只有一个问题:它不工作，而且不包括电源。幸运的是，通过使用热感相机，修复变得更加容易。

如上所述，键盘缺少一个 9 VDC 电源(额定 800 mA ),带有一个中心负极桶形连接器。有点奇怪，但没有什么是一个有事业心的黑客不能对付的。用板凳电源供电后，不仅键盘没活过来，电源还把电流消耗钳位在了 1.5 A！肯定有什么不对劲。

[![](img/8720451a883b8d94931e686f8faea3d5.png)](https://hackaday.com/wp-content/uploads/2022/07/090-FLIR_20220517_102703-768x1024-1.jpg)

This shorted glass-bodied diode might look normal to the naked eye, but thermal imaging makes it clear something’s amiss.

在内部，没有可见(或嗅觉)的损坏迹象，但仔细观察发现，电源连接器旁边的一个小 SMT 电容器裂成了两半。解决这个问题并没有给键盘带来活力，所以是时候打开热像仪了。有什么东西吸收了所有的电流，很有可能在这个过程中有什么东西变热了。

罪魁祸首？反极性保护二极管短路，可能是由于不适当的电源或某种电涌造成的损坏。更换后，键盘可以正常工作了！对于 5 美元、一个二极管、一个 SMT 电容和一点点工作台时间来说，一点也不差。点睛之笔是更换一个丢失的滑动旋钮，这需要一些 OpenSCAD 和 3D 打印机的工作。总体来说还不错！

热成像曾经是价格惊人的东西，但是[现在完全可以使用](https://hackaday.com/2021/07/27/hand-on-review-tcam-mini-wifi-thermal-imager/)，并且很容易发现不该热的东西。如果热感相机的镜头不是你想象的那样呢？[一个有足够动机和知识的黑客甚至有可能修改那些](https://hackaday.com/2018/03/08/adding-optics-to-a-consumer-thermal-camera/)。