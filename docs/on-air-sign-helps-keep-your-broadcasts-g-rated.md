# 广播信号有助于保持你的广播 G 级

> 原文：<https://hackaday.com/2021/01/18/on-air-sign-helps-keep-your-broadcasts-g-rated/>

像我们许多人一样，[迈克尔]需要一种方式让家人知道进入房间是否需要穿裤子——换句话说，就是在视频会议进行的任何时候。当然，他可以挂一个请勿打扰的牌子，但是这些很容易忘记。没有必要担心忘记改变状态，因为这个漂亮的壁挂标志可以用 Alexa 控制。

在这个由胡桃木、卷枫木和橡木制成的华丽盒子里，有一个 ESP32、一些 RGB LEDs 和三个 MOSFETs。[Michael]正在使用 fauxmoESP 库将 ESP32 与 Alexa 连接起来，为了使用她已经知道的协议，Alexa 模拟了 Phillips Hue 灯泡。[Michael]可以用语音命令改变颜色和亮度百分比。

该标志设置为四种不同的设备，一种默认，一种颜色。由于与 Alexa 交谈并不总是合适的，因此[Michael]还可以使用 ESP 提供的网站上的滑块来改变 led 的颜色。休息之后，请查看完整的构建视频。

需要又快又脏又好用的东西吗？我们自己的[Bob Baddeley]做了一个简单有效的状态指示器。

 [https://www.youtube.com/embed/_AaS32MWL8E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/_AaS32MWL8E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

