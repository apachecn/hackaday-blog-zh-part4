# 褪色的美丽数字多媒体获得有机发光二极管改头换面

> 原文：<https://hackaday.com/2018/08/29/faded-beauty-dmm-gets-an-oled-makeover/>

当一件精美的实验室仪器出现在你的工作台上时，你必须尽最大努力让它发挥作用。但是，即使在最高质量的设备中，也没有哪一个部件能经久耐用，尤其是真空管。对于一些带有真空荧光显示屏的老式仪器来说，这意味着要忍受不太完美的数字，以获得那种甜美的精度。或者不是——你总是可以[逆向工程这个东西，并添加一个全新的有机发光二极管显示器](https://www.eevblog.com/forum/repair/hp-34401a-dmm-with-leaking-segments/125/)。

落入[qu1ck]手中的 Hewlett-Packard 34401A 数字万用表是一件漂亮的东西，但它显然曾经风光过。显示屏上满是虚假的发光点和线段，很难使用 6.5 位数字多用表。在徒劳地探索了一个相对简单的驱动程序是否会有所帮助之后，随着固体 unobtanium 显示屏的替换，[qu1ck]开始了对前面板协议进行逆向工程的漫长过程。幸运的是，惠普使用 SPI 协议与显示器对话，不久[qu1ck]就有了一个像样的原型。最终版本更加完美，显示屏大小适合 VFD 占据的原始空间。原来的数字和信号器图标被重新创建，他添加了一个 USB 端口和条形图显示显示在下面的剪辑。

我们认为它看起来很棒，如果你想拯救类似的仪表，Github 上有[固件](https://github.com/openscopeproject/HP34401a-OLED-FW)和[硬件](https://github.com/openscopeproject/HP34401a-OLED-HW)。不过，你可能想先看看[我们的购买旧测试装备指南](https://hackaday.com/2014/10/20/think-before-you-measure-old-test-gear-and-why-it-is-awesome/)，让你的钱发挥最大效用。

 [https://www.youtube.com/embed/LWxOfaXVN3I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/LWxOfaXVN3I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

