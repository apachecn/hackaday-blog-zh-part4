# CMOS 环形调制器踏板

> 原文：<https://hackaday.com/2021/12/24/a-cmos-ring-modulator-pedal/>

今年早些时候，我们推出了一款不同寻常的无线电接收机，它采用非常传统的超极本设计，并以一种意想不到的方式实现，没有任何电感，而是使用 74HC 逻辑芯片和运算放大器的组合。它的设计者[acidbourbon]评论说，该电路与环形调制器有着惊人的相似之处，因此通过生产基于 74HC 的环形调制器吉他踏板来沿着这条道路前进。

在这两个电路中，74HC4046 锁相环芯片用作振荡器，驱动执行混频器任务的 74HC4051 模拟开关芯片。无线电中的额外运算放大器滤波器和解调器电路被省略，振荡器频率下移至音频范围。结果可以在视频中听到，我们可能同意他的观点，即它与经典环形调制器不太一样。这取决于混频器的类型，传统电路中使用的二极管在开始或结束导通之前需要克服正向电压，而 CMOS 开关芯片则根据命令立即开始或结束导通。

4000 系列 CMOS 及其后代是一个迷人的家族，拥有许多意想不到的特性，我们的同事埃利奥特·威廉姆斯在他的[逻辑噪声](https://hackaday.com/2015/08/07/logic-noise-4046-voltage-controlled-oscillator-part-one/)系列中详细介绍了这些特性。与此同时[看看我们对原电台](https://hackaday.com/2021/04/19/a-superheterodyne-receiver-with-a-74xx-twist/)的报道。

 [https://www.youtube.com/embed/58PG2kCZipk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/58PG2kCZipk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

