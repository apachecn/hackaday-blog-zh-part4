# 知道天气的隐形眼镜发射器

> 原文：<https://hackaday.com/2019/04/07/a-contact-lens-launcher-that-knows-the-weather/>

他们说需要是“发明之母”，但多年来，我们开始怀疑她的表亲可能是一个未被充分利用的微控制器。你还能如何解释像[MNMakerMan]的最新项目，它采用了相对简单的隐形眼镜支架概念，并设法将其变成一个联网的电子设备？当然，我们不是在抱怨。

[![](img/cc8cf1c927e8365962a6a80ef61ce1eb.png)](https://hackaday.com/wp-content/uploads/2019/03/contact_detail.jpg) 他开始为他的墙壁设计了一个简单的 3D 打印支架，可以让他取出日常镜头，这个支架非常好用，并在 Thingiverse 上获得了一些人气。但他想知道是否有某种方法可以使用伺服系统来自动化这一过程。当他在做这件事的时候，他可能还会玩一些他一直想要获得一些实践经验的组件，比如所有酷孩子都在使用的那些小有机发光二极管显示器。

他修改了最初的设计，在底部加入了伺服系统，增加了一个中央隔间，可以容纳 ESP8266 和一个由红外 LED 和光电二极管制成的简单接近传感器。传感器往往会有点抖动，所以他在设备内部留了一个电位计，这样他就可以根据需要进行微调。

严格来说，这个项目实际上并不需要有机发光二极管显示器，但由于他有一个支持 WiFi 的微控制器，整天基本上什么也不做，他添加了一个显示天气预报的功能。可以毫不夸张地说，在恢复视觉后，你早上想看到的第一件事就是一天的天气预报，所以我们认为这是核心功能的合理扩展。如果他最终添加了一个通知，提醒他当分配器开始变低时，是时候订购更多的镜头了，这就是加分。

如果你没有需要配的隐形眼镜，不要害怕。类似的概念可以用于在黑客活动中发射定制的礼品。一点也没有吗？这样的话，你总是可以[为万圣节](https://hackaday.com/2018/08/15/arcade-inspired-halloween-candy-dispenser/)做一个糖果自动售货机。

 [https://www.youtube.com/embed/Lj-hJU5XPVM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Lj-hJU5XPVM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

