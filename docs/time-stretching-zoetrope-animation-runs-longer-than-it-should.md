# 时间拉伸 Zoetrope 动画运行时间过长

> 原文：<https://hackaday.com/2018/08/27/time-stretching-zoetrope-animation-runs-longer-than-it-should/>

3D 打印机早就让任何人都可以轻松制作三维的佐伊特罗佩斯，但是你知道你可以通过拉伸时间来利用第四维空间吗？以前，zoetrope 动画的持续时间是平台旋转一周的时间。为了让长时间观看更有趣，您通过创建动画的同心环来填充场景。[凯文·霍尔姆斯]、[查理·轮特纳]和[张克帆·史酷比]想出了一种方法来使他们的动画持续多次旋转，在一个例子中超过三次。如果你对这些 3D 立体雕塑一点都不熟悉，你可能想先看看[这个更简单的版本](https://hackaday.com/2015/03/25/before-film-there-were-zoetropes-now-we-have-3d-printed-zoetropes/)。

[![4-Mation Fish eats Fish zoetrope](img/b5f276d3afe55298a6d68ec255818fae.png)](https://hackaday.com/wp-content/uploads/2018/08/4-mation-fish-eats-fish-zoetrope1.jpg) 他们的项目名称是 4-Mation，但他们称之为时间拉伸技术，动画复用。实现它的一种方法是使用一个长螺旋，从中心开始，在平台的外围结束。这是螺旋路径，使动画持续更长时间。

在他们的*鱼吃鱼*动画中，螺旋是一条小鱼，它从中心的一只蛤蜊中出来，随着它向外螺旋逐渐变大，直到它吞下位于外围一圈的另一条鱼。当然，当你用一个适当定时的闪光灯观察它时，没有螺旋。相反，看起来好像一群鱼或多或少地从中心放射状地向外移动。下面嵌入的第二个视频一步一步地演示了动画，使人们更容易理解正在发生的事情的复杂性。

其他功能包括内置闪光灯和手动及手机应用程序控制。这个项目是 kickstarter 活动的产品，所以通常情况下，电子产品的细节会缺席。但显然[Kevin]熟悉 Hackaday，并发送了一些附加信息，您可以在下面找到这些信息和视频。

控制板使用运行 Arduino 内核的 ESP8266 和 WebSockets API 在 ESP8266 和应用程序之间进行通信。具体来说，他们在 ESP8266 上使用了 Markus Sattler 的 arduinoWebSockets API，在 Android 上使用了 T2 川崎孝彦的 nv-websocket 客户端。他们不确定这些是否是最好的 API，所以如果你有意见，请在下面留下评论。

对于频闪灯，他们使用 9 瓦的 RGB 发光二极管，每个通道有适当的 45 密耳芯片(测量)。他们通过每个通道上的 6 个 led 用 24 V 稍微过压。如果有一个完整的占空比，他们会烧坏它们，但他们使用的占空比只有 1.5%左右。这是因为他们发现，为了让动画清晰，发光二极管需要打开大约 0.5 毫秒。蜗轮的最大速度是 100 转/分，他们使用 2860 计数/旋转编码器。

对于电源，他们有 DC 电源开关供电电路，该电路将 24 V 电压分为 12 V 用于电机，3.3 V 用于 ESP8266。四个“巨型”680 μF、35 V 松下电容缓冲每个选通脉冲之间的电流。

但是动画在这里是新奇的东西，他们已经在 Thingiverse 上发布了他们的 [3D 模型。他们没有包括平台，但复制起来不会太难。对于鱼的动画，他们建议使用树脂打印机，但我们认为，有了支持材料和一些调整，它应该可以用细丝打印机打印。或者更好的是，想出你自己的动画！](https://www.thingiverse.com/n0f8r/designs)

Zoetropes 不仅仅可以用来娱乐和教育。它们是艺术品。看看这幅[把四维挤压成三维](https://hackaday.com/2016/06/29/3d-printed-zoetrope-sculpture-squashes-4-dimensions-into-3/)还有这幅[一个人走在旋转轮子的外缘](https://hackaday.com/2012/01/11/3d-printed-zoetrope/)。

 [https://www.youtube.com/embed/_Tg6O8DoRAY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/_Tg6O8DoRAY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/U8ZHJwjGL5s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/U8ZHJwjGL5s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/xl_b5ynKApQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/xl_b5ynKApQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

