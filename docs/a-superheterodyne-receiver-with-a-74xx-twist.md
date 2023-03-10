# 一个 74xx 扭曲的超外差接收机

> 原文：<https://hackaday.com/2021/04/19/a-superheterodyne-receiver-with-a-74xx-twist/>

在一个软件定义无线电和单芯片接收机的世界里，超外差短波无线电可能不会在潇洒尺度上获得很高的分数。毕竟，人们混频、滤波和解调 RF 信号已经有一个多世纪的历史了，而且表现最佳的电路已经有了很好的特征。但是不使用传统的超级热装置来建造同样的接收器呢？这是新的东西。

在[Micha]半开玩笑地称之为[的“74xx 定义的无线电”](https://acidbourbon.wordpress.com/2021/04/11/a-74xx-defined-radio/)中，容易获得的分立逻辑芯片，加上一些运算放大器和一些简单的元件，取代了调谐 LC 电路和成组的可变电容器，使典型的超热接收器更加优雅。[Micha]从利用 74HC4051 模拟多路复用器构建一个 RF 混频器开始，借助 2N3904 分相器形成一个开关混频器。本地振荡器依赖于 74HC4046 PLL 中的压控振荡器(VCO)，这是一种我们之前在[埃利奥特·威廉姆斯]的中见过的[出色的“逻辑噪声”系列芯片。中频滤波器是一个简单的运算放大器带通滤波器；解调器还具有一个运算放大器，设置为有源半波整流器。没有线圈要缠绕，没有电容器要调谐，没有具有神秘属性的二极管——从下面的视频来看，它工作得相当好。](https://hackaday.com/2015/08/07/logic-noise-4046-voltage-controlled-oscillator-part-one/)

这可能不是最传统的短波波段调谐方式，但我们总是喜欢像这样人为限制的项目结果。向[Micha]脱帽致敬，沿着设计之路进行有趣的旅行。

 [https://www.youtube.com/embed/XsFSDM1pgMA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/XsFSDM1pgMA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

