# (相对)便宜的热感相机的拆卸

> 原文：<https://hackaday.com/2018/11/07/teardown-of-a-relatively-cheap-thermal-camera/>

工具和测试设备的成本多年来一直呈下降趋势，这使得进入黑客和制作领域比以往任何时候都更加实惠。这一点在古老的示波器上尤其明显:十年前，这种设备对家庭黑客来说几乎是不可及的，现在你只需花 20 美元就能买到数字袖珍示波器。但仍有一些产品没有达到我们希望看到的价格。

[![](img/3ab5caee04bb17c5f1cab91e2776a36c.png)](https://hackaday.com/wp-content/uploads/2018/10/hta1_detail.jpg) 热成像相机就是一个完美的例子。廉价的温度计通常分辨率很低，就像温度计一样，但分辨率较高的温度计可能要花费数千美元。[Rob Scott]最近写信给[告诉我们一个非常有前途的中间地带，HTI HT-A1](https://www.youtube.com/watch?v=owc-vJKEi1c) 。但他不只是给我们指出来，他还把它拆了，把它的内部暴露出来供我们娱乐。这就是我们的介绍。

[Rob]向我们介绍了设备的拆卸过程，由于一半的螺钉隐藏在粘合的屏幕边框下，拆卸变得不必要的困难。这意味着如果你想进入设备内部，需要一个热风枪，一个薄的工具和耐心。他们在现代智能手机上使用这种构造技术已经够糟糕了，但至少它们很薄，我们可以理解其中的原因。为什么这个矮胖的东西需要采取这样的措施超出了我们的理解。

最后，他打开 HT-A1，迎接他的是一块双面印刷电路板。除了按钮和 LCD 显示屏，顶部几乎是光秃秃的，而反面很大程度上只是一个四核 Allwinner A33 子板的突破。[Rob]认为这是为了通过允许在其他设备上重用模块化 A33 板来降低成本。鉴于 A33 在如此多的廉价平板电脑中的使用，HTI 也有可能只是购买这些子板作为嵌入式组件，并围绕它设计自己的主板。

除了可充电电池组和热感相机外，HT-A1 内部没有太多其他东西，两者都连接到设备的后面板。[Rob]注意到热感相机 PCB 上的日期比主 PCB 上的日期早了整整两年，这让人怀疑 HTI 是否在这些稍微过时的传感器上做了一笔好交易，并围绕它们旋转了整个设备。

HT-A1 的分辨率足够高，你实际上可以挑出 PCB 上的单个元件，400 美元对个人黑客来说是一个合理的价位。这并不是说它便宜，但至少你的钱得到了一个有用的工具。我们不建议你心血来潮买这个设备，但是如果你做了大量的诊断工作，[在几次维修后它可能会收回成本](https://hackaday.com/2018/03/03/thermal-camera-diagnoses-thermal-issue-on-a-sonoff-switch/)。

如果这对你来说还是有点太贵，我们已经介绍了一些 DIY 选项，这些选项可能会更符合你的预算。

 [https://www.youtube.com/embed/owc-vJKEi1c?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/owc-vJKEi1c?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

