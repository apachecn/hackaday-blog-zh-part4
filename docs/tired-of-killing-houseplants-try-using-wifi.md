# 厌倦了杀死室内植物？试试用 WiFi。

> 原文：<https://hackaday.com/2018/12/17/tired-of-killing-houseplants-try-using-wifi/>

在 Hackaday，我们不得不承认在我们这个时代忽略了一些室内植物。让我们面对现实吧…一台冷酷、坚硬、会思考的机器能比你更好地照顾我们的绿色朋友。为什么不组队？【cabuu】的[支持 WiFi 的土壤湿度传感器](http://mangetout.net/cabuu/2018/12/16/wifi-enabled-soil-moisture-sensor/)将在你也想要快乐植物的情况下发挥作用。

这是那些即使在五年前也会困难得多的项目之一，并且真正地表明我们是多么幸运地拥有触手可及的技术。它由现成的电子模块方便地构建而成，坐落在[一个 3D 打印的盒子](https://www.thingiverse.com/thing:3289904)内。该设计既吸引人又实用，显示状态 LED，并允许访问 USB 充电端口。

大脑是一个 WeMos D1 迷你，而 D1 电池屏蔽和 14500 锂离子电池供电。这种构造的一个关键点是电容式湿度传感器的使用，它不会遭受相同的长期腐蚀问题，即[破坏更便宜的电阻探头](https://hackaday.com/2017/11/16/sensing-soil-moisture-youre-doing-it-wrong/)。没有 LED 就没有完整的项目，所以 WS2812 显示绿色代表好，红色代表干，蓝色代表太湿。为了延长电池寿命，传感器支持睡眠模式，定期测试土壤，并可能禁用 LED。

当然，如果你是一个习惯性忽视植物的人，简单地用一个湿度探头是没有用的；这些和植物本身一样容易被忽视。这就是 WiFi 的用武之地。[cabuu]写了一个 [Blynk](https://www.blynk.cc/) 应用程序来监控智能手机上的传感器。该应用程序显示当前的湿度水平，并允许您更改干湿警告阈值。当读数超过这些水平时，应用程序会通知你——这个功能可以让你的植物留在周围。

 [https://www.youtube.com/embed/fhIwSXpJTjg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/fhIwSXpJTjg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



在 T1 之前，我们已经看到了湿度传感器，我们自己的(Al Williams)甚至已经(T2)快速浏览了 Blynk(T3)，如果你想开始为你的项目编写智能手机界面，它会有所帮助。

感谢[Baldpower]的提示。