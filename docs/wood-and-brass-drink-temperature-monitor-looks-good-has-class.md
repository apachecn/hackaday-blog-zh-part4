# 木头和黄铜饮料温度监测器看起来不错，有档次

> 原文：<https://hackaday.com/2021/06/16/wood-and-brass-drink-temperature-monitor-looks-good-has-class/>

我们都经历过。你目前的项目碰壁了，或者下一步需要几天才能完成，这期间你需要做点事情。所以你开始了一个项目，你想象它会很好地适应这个空白，然后，不可避免地，它没有。也许它甚至需要很长时间，以至于最初的项目先完成了。那又怎样？这没有什么错，尤其是当灌装机项目的结果和[这个伪装成电路雕塑的饮料温度监控器](https://www.youtube.com/watch?v=4gJ1Rk6mqHM)(视频，嵌入下方)一样好的时候。只要把你的杯子放在杯垫上，它的重量就会启动一个隐藏的开关，使雕塑显示出它秘密的发光二极管。

[MakeFunStuff]想要做一些看起来不像电路而更像艺术的东西，同时建立一个可以确定饮料相对热度的工具。这样一个有用的电路雕塑对我们来说听起来是一个高要求，但[MakeFunStuff]用技巧和风格完成了它。

[![](img/4fd04f625c961a7a1ecde0459314c1e7.png)](https://hackaday.com/wp-content/uploads/2021/06/arduino-drink-temp-monitor-inner.jpeg) 这个电路是基于这个看起来像人造卫星的独立红外温度传感器，正如[MakeFunStuff]恰当地描述的那样，它是“一个单像素红外摄像机，可以拍摄从传感器开始的 90°圆锥内的一切。”

[MakeFunStuff]将这款易于使用的传感器与 Arduino Nano 和五个 led 配对，这些 led 可以从 1 到 5 显示饮料的热度。传感器隐藏在显眼的地方，悬挂在黄铜杆雕塑的顶部，完美地融入其中。我们喜欢 led 隐藏在一层精心钻孔的木材后面，并同意钻床会容易得多。

该代码几乎适用于从摄氏温度到摄氏温度的所有温度范围，因此解决了这个问题。使用开尔文温标是因为科学。我们最喜欢这个视频的一点是，[MakeFunStuff]分享了他们的失败和修复，因为他们在回答如何将传感器悬挂在饮料上，以及如何在隐藏电子设备的同时最好地显示热量水平的问题。休息之后，去拿一杯热咖啡，看看有什么东西，让它以正常的方式冷却下来。

我们承认，在等待 led 消失时，我们可能会晕过去。[这是一个智能杯垫，当你的饮料达到最佳饮用温度时，它会使用 ESP8266 向 Discord 发送信息](https://hackaday.com/2018/08/14/internet-of-tea-coaster-watches-for-optimum-drinking-temperature/)。

 [https://www.youtube.com/embed/4gJ1Rk6mqHM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/4gJ1Rk6mqHM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



谢谢你的热点提示，[佩里]！