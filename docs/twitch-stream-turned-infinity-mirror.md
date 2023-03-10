# 抽搐流变成了无限镜

> 原文：<https://hackaday.com/2018/07/18/twitch-stream-turned-infinity-mirror/>

大多数 Hackaday 的读者可能都很熟悉 infinity mirror，这是一件非常棒的家居装饰，以至于在 2285 年斯波克仍然在墙上挂着一面镜子。这个想法很简单:两个平行的镜子来回反射和成像，这就产生了一个重复的反射，看起来好像消失在无穷远处。如果你将网络摄像头对准显示摄像头输出的屏幕，就可以观察到这种效果的数字版本。这个图像似乎将永远持续下去，在 20 世纪 90 年代末的那段时间里，这个技巧提供了数不清的乐趣，似乎每个人都有一个垒球形状的相机停在他们的 CRT 显示器上。

[![](img/f8b0f1568d4f3232bf62ebfc35b84ee3.png)](https://hackaday.com/wp-content/uploads/2018/07/infinity_detail.png)

Making use of that webcam in 2018.

虽然你可能认为你已经看到了这种经典视觉技巧的每一种可能的变化，但[马特·西山丽-拉奇]最近写信给我们，告诉我们他使用流行的流媒体平台 Twitch 创建的无限镜像效果。公众甚至被邀请通过一组可以在聊天窗口中使用的命令来摆弄视觉效果。

它的工作方式和你预想的一样:视频流被捕获，通过各种过滤器处理，然后通过 Twitch 重播。这导致了各种怪异的视觉效果，但总的来说，给人的印象是一切都是从远处的一个中心点辐射出来的。

虽然[Matt]承认可能没有很多人想要建立他们自己的 Twitch 反馈循环，但他仍然[向任何可能感兴趣的人提供他的 Python 代码](https://github.com/MattBroach/irc2osc)。在 Hacker Valhalla 中有一个特殊的位置给那些像开源一样发布利基软件的人。他们是*真正的*MVP。

如果你想从更实际的东西开始你的无限旅程，我们已经涵盖了传统的无限镜像构建[，从简单的](https://hackaday.com/2015/11/21/the-easiest-infinity-mirror-build/)到华丽过度设计的。