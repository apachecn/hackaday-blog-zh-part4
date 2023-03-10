# 人类看不懂时钟

> 原文：<https://hackaday.com/2020/10/06/clock-is-not-readable-by-humans/>

并不是每一个构建都需要立即可用或具有革命性。许多构建只是为了好玩，为了教育，甚至是有目的的无用但仍然具有挑战性。例如，这个时钟可能符合所有这三个类别。这是一个通过二维码显示时间的时钟，除非你有一个可能已经有可读时钟的设备，否则它完全不可理解。

QR 码时钟来自[Aaron]并基于现在无处不在的 ESP32 WiFi 芯片。ESP32 连接到一个 64×64 LED 矩阵，该矩阵每秒钟更新一次当前时间代码。凭借一秒钟的分辨率，这意味着即使有手动读取二维码的方法，就像你有时可以使用条形码一样，没有智能手机也无法读取，因为它变化如此之快。

当然，[亚伦]在他的视频中认识到了他设计中的缺陷，他半开玩笑地指出，有了这个时钟，你再也不用看智能手机了，因为时钟就在墙上。我们很欣赏这种幽默，而且[Aaron]已经公开了他所有的源代码，以防你想把它作为一个例子，把二维码用于更有用的目的。不过现在，我们会把你带到其他一些[无用的机器](https://hackaday.com/2020/09/20/finally-a-differently-useless-machine/)。

感谢[威尔莫]的提示！

 [https://www.youtube.com/embed/_Ku3ds-njfU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/_Ku3ds-njfU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

