# LTSpice 中的光伏电池

> 原文：<https://hackaday.com/2022/07/04/photovoltaic-cells-in-ltspice/>

我们喜欢用真实的零件来建造东西。但是我们确实认为使用 LTSpice 这样的工具建模越多，进入死胡同的时间就越少。如果你需要模拟一个普通的元件，比如一个电阻，甚至一个有源器件，大多数模拟器都有很好的模型，你可以调整它们以产生真实的寄生效应。但是，如果您想要的组件不在库中或者没有您想要的保真度，该怎么办呢？【FesZ】想要[制作光伏电池](https://www.youtube.com/watch?v=uV_z1ptufa4&t=0s)的模型，必须自己搭建模型。由此产生的两个视频非常值得一看。

在 Spice 中构建自己的模型并不一定非常困难。然而，准确地知道添加什么来模拟不同的真实世界效果可能是具有挑战性的。这些视频很好地展示了如何将一个简单的二极管突变成一个暴露在光线下产生电流的二极管。

在我们看来，关键是不要掉进兔子洞太深。例如，默认模型在模拟主要效果方面做得很好，但不会陷入没有多大实际差别的微妙细节中。您通常希望捕捉正常操作状态下的主要影响。事实上，如果你抽取 30 安培的电流，你的电阻将会熔断，这对于大多数仿真来说并不重要。

在之前，我们已经看过在 [Spice 中建造变形金刚。我们也喜欢用 LTSpice](https://hackaday.com/2016/03/02/transforming-spice/) 建模[测试设置。](https://hackaday.com/2019/06/05/circuit-vr-resistance-measurement-with-four-wires/)

 [https://www.youtube.com/embed/uV_z1ptufa4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/uV_z1ptufa4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/ox0UtYe4owI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ox0UtYe4owI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

