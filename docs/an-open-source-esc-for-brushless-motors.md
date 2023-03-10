# 一种用于无刷电机的开源 ESC

> 原文：<https://hackaday.com/2019/05/15/an-open-source-esc-for-brushless-motors/>

对于像有刷 DC 电机这样的基本设备来说，速度控制可能非常简单，给电机加电只是施加电压的简单事情。然而，无刷电机的要求更加苛刻，除非驱动*恰到好处*，否则不会旋转。【Electronoobs】一直在探索无刷速度控制器的设计，[刚刚发布了他的开源 ESC 设计的 1.0 版本。](https://www.electronoobs.com/eng_arduino_tut91.php)

基本设计紧凑，非常类似于低功率范围内的许多现成的无刷 ESC。有一个小 PCB 封装了一组 MOSFETs 来处理电机线圈的开关电源，还有一个大电容来帮助处理电流尖峰。黑客主食 ATMEGA328 是运行该节目的微控制器。这是一种无传感器设计，它测量电机的反电动势，以确定何时启动 MOSFETs。这使得低扭矩、低功耗应用变得简单。

这是一个整洁的构建，与早期的原型相比，最新的修订版显示了很多改进。如果你有兴趣了解更多，试着自己建造它，[或者考虑在家里为你的工作台建造一个推力测试台](https://hackaday.com/2018/12/16/brushless-motor-thrust-stand-provides-useful-data/)。休息后的视频。

 [https://www.youtube.com/embed/VdkloigaxZo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/VdkloigaxZo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

