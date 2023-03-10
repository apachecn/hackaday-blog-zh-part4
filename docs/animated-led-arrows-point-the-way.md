# 动画 LED 箭头指示方向

> 原文：<https://hackaday.com/2022/09/24/animated-led-arrows-point-the-way/>

华盛顿贝尔维尤花园的游客遇到了一个问题。在参观节日灯展时，他们不断偏离道路。活动组织者尝试了一些简单的 LED 箭头，但它们只是充斥着它们的海洋中更多的亮点。这就是[埃里克·甘纳森]被要求帮忙的时候。他显然有一些 LED 动画的经验，甚至[编写了一个简单的描述语言](https://github.com/ericgu/Fade)来编写由 ESP32 驱动的动画。为了使预期的路径显而易见，他转向一个嵌有 50 个 WS2812 像素的 PVC 板——RGB 可控 led。控制盒是一个 USB 电源适配器和一个 ESP8266，非常小心地防水并连接到像素串。背板涂成黑色，以完成硬件。在不可避免的休息之后，留下来看看决赛

构建过程的描述很详细，包含了一些很棒的技巧，但是如果没有一个聪明的 led 动画，它的实用性仍然值得怀疑。选择的图案很棒，led 大部分时间都是蓝色的，每隔几秒钟就有火焰般的梯度穿过箭头。和节目的灯光明显不一样，似乎是真正的赢家。[Eric] [发表了他的代码](https://github.com/ericgu/LedArrow)，羞怯地警告说，他不得不再次重新发明轮子，并且不能在这一个上重用他以前的任何 LED 动画作品。这是一个简单的技巧，但是一个很棒的构建日志，并且是一个微妙问题的有效解决方案。如果可寻址 led 是你的东西，[看看我们的其他黑客](https://hackaday.com/2020/10/02/voice-controlled-rgb-leds-go-big/)！

 [https://www.youtube.com/embed/9ViJaHS8k9U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/9ViJaHS8k9U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

