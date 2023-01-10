# 你对灯光的选择有多稳定？

> 原文：<https://hackaday.com/2020/03/21/how-constant-is-your-choice-of-lights/>

在过去的几十年里，从白炽灯到荧光灯，再到 LED 照明，在节能方面带来了巨大的好处，但也给那些对闪烁或过多特定波长敏感的人带来了问题。量化特定光线闪烁的倾向并不总是容易的。所以[kk99] [已经生产出一种仪器，它返回一个质量的视觉指示](https://hackaday.io/project/170394-the-simple-light-flicker-meter)。

它的核心是一个 M5Stick ESP32 开发平台，以及一个连接到 ESP 内部 ADC 的 [TSL250R](https://www.digikey.co.uk/product-detail/en/ams/TSL250R-LF/TSL250-R-LF-ND/3095043) 光传感器。闪烁波形在屏幕上显示为一个简单的示波器，并执行傅立叶变换以提取其频率。其结果是一个非常方便和紧凑的仪器，显示了 M5Stick 外形适合此类设计。到目前为止，我们只给你带来了[一个 M5 棒的密码保持器](https://hackaday.com/2020/02/19/password-keeper-uses-off-the-shelf-formfactor/)，但我们期待看到更多的项目采用它。

您可以在休息时间下方的视频中看到灯光闪烁仪在工作。

 [https://www.youtube.com/embed/-aoaFfzkxDI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/-aoaFfzkxDI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

