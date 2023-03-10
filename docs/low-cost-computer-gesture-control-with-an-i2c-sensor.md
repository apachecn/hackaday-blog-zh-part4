# 具有 I2C 传感器的低成本计算机手势控制

> 原文：<https://hackaday.com/2021/11/12/low-cost-computer-gesture-control-with-an-i2c-sensor/>

用手一挥来控制你的电脑看起来像是科幻小说里的东西，而且理由很充分。从《少数派报告》到《T2》和《钢铁侠》，我们已经看到很多著名演员通过在空中疯狂地比划来控制他们的高科技电脑系统。与此同时，我们都像一群傻瓜一样使用键盘和鼠标。

但不一定非要这样。正如[【诺伯特·扎雷亚】在他的最新项目](https://hackaday.io/project/182542-control-your-computer-with-hand-gestures)中展示的，你实际上可以使用一个 10 美元的 PAJ7620U2 传感器在你的计算机上实现一些相当令人印象深刻的手势控制。当然不是*而是*传感器。你需要某种方法将 I2C 传感器的输出转换成你的计算机能够理解的东西，这就是微控制器的用武之地。

[![](img/4084fed55523e3237963a07682104d52.png)](https://hackaday.com/wp-content/uploads/2021/11/i2cgesture_detail.jpg) 通过查看提供的源代码，您可以看到与 PAJ7620U2 对话是多么容易。没有什么比`switch case`陈述更奇特的了，【Norbert】能够从传感器中获得手势标志。从那以后，只需要使用 Arduino 键盘库来发出适当的键码。如果你想重现这一点，我们会选择支持原生 USB 的微控制器，但从技术上来说，这可以在几乎任何 Arduino 上完成。事实上，在这种情况下，他实际上使用的是基于 ATtiny85 的 Digispark[。](https://hackaday.com/2021/09/08/spooky-usb-baby-types-out-messages-from-beyond/)

这实际上并不是我们第一次看到有人[使用类似的传感器来实现低成本的手势控制](https://hackaday.com/2017/12/03/gesture-control-for-lunch-money/)，但是到目前为止，这些项目都没有真正成功。在休息后的视频中，它似乎工作得足够好，但外表可能具有欺骗性。有没有任何 Hackaday 读者真正尝试过将这些模块之一用于他们的日常未来计算？

 [https://www.youtube.com/embed/BoA5tAtZOtc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/BoA5tAtZOtc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

