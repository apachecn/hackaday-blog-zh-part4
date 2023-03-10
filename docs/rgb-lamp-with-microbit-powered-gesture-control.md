# 具有微比特供电手势控制的 RGB 灯

> 原文：<https://hackaday.com/2019/09/20/rgb-lamp-with-microbit-powered-gesture-control/>

Micro:bit 是一个非常简洁的硬件，坦率地说，我们看得还不够多。当[【Manoj Nathwani】写信告诉我们他创造的华丽的 3D 打印 RGB LED 灯](https://manoj.ninja/articles/2019/09/19/2019-building-a-gesture-controlled-lamp)使用 BBC 认可的微控制器来执行基本的手势检测时，这让我们更加感兴趣。纯粹主义者可能会指出，Arduino Pro Mini 是用来处理与 led 接口的，但它仍然是一个很好的例子，说明在 Micro:bit 上使用 MicroPython 可以多快地启动并运行一个项目。

[![](img/9ff281db7495b584367f400d0455aa88.png)](https://hackaday.com/wp-content/uploads/2019/09/microlamp_detail.jpg)【Manoj】用八个尼奥像素的棍子，一个尼奥像素的环，和一些碎木板，构建了一个三维的“灯泡”来填充印刷扩散器内部的空隙。它们被链接在一起，所以所有的元素都显示为一个可寻址的条带，这使得项目的其余部分更容易实现。它可能并不漂亮，但它完成了任务，而且一旦安装到灯里，你就再也看不到它了。

Micro:bit 和 Arduino 副驾驶住在灯的底座上，提供电源(以及更新设备固件的能力)的单一 USB 电缆从底部伸出，使整个东西看起来干净专业。对于那些想知道为什么 Arduino 一直跟在后面的人，[Manoj]说他不能让 NeoPixel 库很好地与 Micro:bit 配合，所以他基本上使用 Arduino 作为中介。

目前，在 Micro:bit 上检测到的唯一手势是一个简单的摇动，它告诉 Arduino 打开和关闭灯光显示。但在未来，[Manoj]计划实现更复杂的手势，这将触发不同的动画。正如他在博客中解释的那样，使用 Micro:bit 进行手势识别非常简单，因此应该很容易找到一系列与灯交互的独特方式。

变色 LED 灯是黑客们最喜欢的项目，我们已经看到了用各种材料制作的例子[，从玻璃和铜](https://hackaday.com/2019/03/06/fueled-by-jealousy-this-smart-lamp-really-shines/)到[激光切割的木头和单板](https://hackaday.com/2019/03/05/cylindrical-led-display-comes-full-circle/)。虽然你可能更喜欢[跳过 ESP8266 和 UDP](https://hackaday.com/2019/05/27/esp8266-upgrade-gives-ikea-leds-udp-superpowers/) 的手势控制，但我们认为这个项目是进入这种流行风格的又一个强有力的入口。