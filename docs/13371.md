# 锂电池升级使枪支保险箱更加安全

> 原文：<https://hackaday.com/2022/04/18/gun-safe-made-safer-with-lithium-battery-upgrade/>

一个合适的枪支保险箱应该很难打开，但关键是，允许授权方立即进入。[【Gerg 博士】得到了一个 SnapSafe](https://www.drgerg.com/a-gun-safe-safer.html) 并发现，虽然它很容易使用，但它也可以在电池耗尽时轻松地将主人锁在外面。这意味着使用四节 AAA 电池，没有办法从外部给它们充电，这可能会让你在你需要枪安全打开的确切情况下皇家拧。这当然意味着 AAA 电池不得不被淘汰。

Gerg 博士]以前拆过几块笔记本电脑电池，现在手上有一小堆锂离子电池——圆柱形和袋状电池。将 AAA 电池座换成其中一个电池座在电压方面没有任何问题，测试表明它工作顺利！然而，用另一个不可充电的电池替换另一个不可充电的电池并不是一种可行的方法，所以他还增加了使用 Adafruit LiPo 充电器板充电。一个 3D 打印的 OpenSCAD 设计的支架之后，他将电路板安装在保险箱的框架内，然后拔出 USB 电缆进行充电，将电池变成备用选项，本质上为这个保险箱创建了一个 UPS。如今，保险箱一直插在墙上的插座上，而且[格尔博士]估计，即使在 USB 断电的情况下，它也应该能持续几周。

当你读到黑客攻击枪支保险箱时，[通常是因为它们的安全性差](https://hackaday.com/2017/12/13/bluetooth-gun-safe-cracked-by-researchers/)，甚至连生物识别模型[也偶尔成为窥探手指的受害者](https://hackaday.com/2019/10/03/pistol-safes-poor-design-means-biometric-sensor-bypassed-in-seconds/)。有人说要将锁定功能植入枪支本身，但[我们对此仍持怀疑态度](https://hackaday.com/2016/08/01/firearm-tech-are-smart-guns-even-realistic/)。“用内部电池给电子锁箱供电”是一个有趣的问题，最近，我们看到这个复杂的声控锁箱以不同的方式得到了解决。