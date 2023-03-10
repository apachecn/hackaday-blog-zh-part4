# 一个雷达模块拆卸和测量风扇速度的艰难方式

> 原文：<https://hackaday.com/2018/08/14/a-radar-module-teardown-and-measuring-fan-speed-the-hard-way/>

如果你对微波电子学和雷达有哪怕一丁点的兴趣，那你一定会大开眼界。信号路径通过另一个视频回来了，这个视频涵盖了一个简单的 24 GHz 雷达模块的内部结构，以及一些我们觉得很有趣的实验。

[Shahriar]在下面的视频中使用的雷达模块是一个 CDM324，可以从通常的来源花几块钱买到。因此，它包含了价值工程和价格点设计方面的许多经验，而拆卸后发现它只包含一个有源设备。[Shahriar]向我们展示了电路的布局，指出了一些有趣的地方，如没有电介质的电容器、充当[偏置三通](http://hackaday.com/2018/06/26/everything-you-didnt-know-you-were-missing-about-bias-tees/)的蝶形短截线，以及用作混频器的 rat-race 耦合器。PCB 的另一面有两个波束形成贴片天线阵列，一个用于发射，一个用于接收。经过几个简单的测试，显示模块的中心频率是高度可变的，他做了一个简单的测试，使用伺服系统制成的万向节来扫描方位角和仰角的信号，同时指向接收喇叭天线。这显示了波束形成阵列的不对称特性。最后，他使用该模块测量了计算机风扇的速度，这在数据安全和一些实际应用中有一些有趣的可能性。

尽管[Shahriar]的视频倾向于长一点的那一面，但他通过包装大量的材料来使每一秒都有价值。他还让复杂的话题变得非常平易近人，比如[价值百万美元的示波器里面有什么](https://hackaday.com/2015/02/10/the-one-million-dollar-scope-teardown/)或者[诊断一台不稳定的 14 GHz 频谱分析仪](https://hackaday.com/2017/01/29/2700-ebay-bet-pays-off-for-this-14-ghz-spectrum-analyzer-repair/)。

 [https://www.youtube.com/embed/5vqSX40seqA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/5vqSX40seqA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

