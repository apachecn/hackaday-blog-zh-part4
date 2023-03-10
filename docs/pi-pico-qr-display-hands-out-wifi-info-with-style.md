# Pi Pico QR 显示屏以时尚的方式分发 WiFi 信息

> 原文：<https://hackaday.com/2022/12/08/pi-pico-qr-display-hands-out-wifi-info-with-style/>

在这一点上，你可能意识到你可以将你的无线网络凭证存储在一个二维码中，这样任何想用智能手机连接的人只需要扫描 2D 的条形码。不管你是把它打印在纸上，还是用塑料挤出来，或者把它画在墙上，它都是一样的。当你邀请朋友和家人过来时，这是一个巧妙的技巧，省去了你解释冗长的 WPA 键的麻烦。

但是，如果您想经常更改加密密钥，该怎么办呢？重新粉刷墙壁肯定会很麻烦。[进入来自【Predrag Mijatovic】](https://github.com/predmijat/qr_wifi)的这个有趣的项目，它使用几个脚本来自动建立一个新的加密的客人 WiFi 网络，并在连接到树莓派 Pico 的有机发光二极管显示器上显示适当的二维码。这有点复杂，如果不进行重大调整，几乎肯定不会在您的网络上运行，但我们对这个想法很感兴趣。

正如[Predrag]解释的那样，整个事情是基于一个可以通过 SSH 配置的拉脱维亚 MikroTik 路由器。Bash 脚本通过对输出`/dev/urandom`进行 base64 编码生成一个新的加密密钥，登录路由器使用它建立一个新的网络，然后生成匹配的 ASCII QR 码。通过一些`sed`诡计，代码被嵌入到一个 MicroPython 程序中，该程序被上传到连接的 Pi Pico。

在休息后的视频中，[Predrag]带我们手动完成这个过程，这样更容易看到发生了什么。在正常情况下，这一切都会自动发生，只需几秒钟就能完成。如果脚本有一些纠错功能，允许它们在出错时优雅地退出，我们会感觉更舒服，但作为概念的证明，它肯定是有效的。

我们希望看到这一概念得到进一步的探索，也许可以使用我们多年来看到的一种[物理二维码显示器](https://hackaday.com/2022/08/28/led-clock-uses-micro-qr-codes-to-show-the-time/)。一个[可编程电子纸显示器](https://hackaday.com/2022/12/07/review-inkplate-2-shrinks-down-adds-color/)也将是展示动态二维码的一种合乎逻辑的方式。

 [https://www.youtube.com/embed/APTqu29ApRc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/APTqu29ApRc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

