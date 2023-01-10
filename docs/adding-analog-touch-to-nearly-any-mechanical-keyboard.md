# 为(几乎)任何机械键盘添加模拟触摸

> 原文：<https://hackaday.com/2018/09/26/adding-analog-touch-to-nearly-any-mechanical-keyboard/>

DIY 电子产品的新热点是机械键盘，在过去的几年里，我们已经看到了一些惊人的创新。这一个是不同的。它为几乎所有的机械按键开关添加了一个模拟传感器，只需要最少的部件，并且不需要对开关本身进行任何修改。[这是一个 reddit 帖子](https://www.reddit.com/r/MechanicalKeyboards/comments/9ii6gw/this_is_my_first_unmodified_analog_cherry_mx/)和 [imgur 帖子](https://imgur.com/gallery/ImrH7nO)，但这个想法是*太好了*我们可以忽略关于这个的文档。

这种传感器背后的关键发展是认识到几乎每个机械按键开关(Cherry MX、Kalth、Gateron)的底部都有一个弹簧。弹簧只是一卷电线，电感器也只是一卷电线。通过在按键开关下方的机械键盘的 PCB 上放置一条螺旋轨迹，您可以感应到该弹簧的电感。这确实需要一点额外的硬件，在这种情况下是一个 [LDC1614 电感数字转换器](http://www.ti.com/product/LDC1614)，但这是一个 I2C 可读器件，理论上可以很容易地与任何机械键盘 PCB 和固件集成。

使用 LDC1614 的缺点是采样有一定的时间限制，四个通道或单个按键以 500 Hz 进行轮询。如果用例是给你的 WASD 键添加模拟，这不是问题，但是对于整个键盘来说，这可能会成为一个问题。此外，LDC1614 有点贵，千片订量约为 2 美元。使用这种技术的全模拟键盘将会非常昂贵。

目前，这种模拟机械按键开关的概念验证只是一个 0.1 毫米的柔性 PCB，插在樱桃 MX 红色和(普通)机械键盘 PCB 之间。开发的下一步将是带有模拟传感器的 2×4 键盘，并在 GPL 许可下开放硬件和固件示例。