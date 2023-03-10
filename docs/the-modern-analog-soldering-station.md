# 现代模拟焊接站

> 原文：<https://hackaday.com/2018/10/31/the-modern-analog-soldering-station/>

当构建自己的工具时，会有一种成就感。这就是亚历杭德罗·贝拉斯克斯建造自己的焊接站的目的。当然，你可以在亚马逊或易贝花很少的钱买到一个不错的站点。你甚至可以建立自己的微处理器控制站。[Alejandro]目前对模拟电子感兴趣，所以他走了这条路来建立自己的闭环站。

手柄是一个带有热电偶的 50 瓦 24 伏的东西。您可以在许多 Hakko 907 克隆焊台(通常称为 907A)上找到这种手柄。电台本身完全是模拟的。三端双向可控硅开关切换流向加热器的电流。三端双向可控硅开关由 PWM 信号控制。PWM 本身由 LM324 四路运算放大器产生和调节，它是该站的心脏。运算放大器将设定值与从焊接手柄热电偶读取的当前温度进行比较，然后调整 PWM 信号的占空比，以升高或降低温度。

这是一个经典的控制系统，如果你想了解如何利用运算放大器实现复杂的运算，原理图绝对值得一看。

你可以在 Hackaday 上找到更多关于模拟电子的信息，我们已经讨论了[热电偶放大器](https://hackaday.com/2015/04/06/how-to-build-a-thermocouple-amplifier/)，以及[仪表放大器](https://hackaday.com/2015/03/16/instrumentation-amplifiers-and-how-to-measure-miniscule-change/)。如果你是一个数字人，[看看这个 Arduino 控制的焊接站](https://hackaday.com/2018/09/22/diy-arduino-soldering-iron-hits-version-2-0/)！