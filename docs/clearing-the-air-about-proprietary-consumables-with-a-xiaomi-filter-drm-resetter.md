# 用小米滤镜 DRM 重置器消除专有耗材的疑虑

> 原文：<https://hackaday.com/2021/08/28/clearing-the-air-about-proprietary-consumables-with-a-xiaomi-filter-drm-resetter/>

“剃刀和刀片模型”可能让许多年轻黑客走上了他们当前的轨道。如果我们买了一个小工具，我们想选择我们的小工具笔芯，而不是回到制造商的名牌选项。当[Flamingo-Tech]的小米空气净化器需要一个新的过滤器时，他们什么都没有，所以他们开始[欺骗它，让它认为有一个真正的替代品](https://flamingo-tech.nl/2021/06/20/xiaomi-air-purifier-3h-modchip-is-here/)刚从盒子里拿出来。与剃须刀手柄不同，空气净化器如果不满意可以拒绝工作，所以最好的选择是制作一个“mod-chip”

制造商的滤波器有一个近场通信(NFC)芯片和天线，可以与基站通信。控制器通过 I [2] C 接收滤波器数据，但 mod-chip 替换了该发射器，并向控制器保证滤波器镇一切正常。最重要的是，[Flamingo-Tech]向我们展示了如何用廉价的包装来延长过滤器的寿命，这样就一举两得了。你可以从[开源文件](https://flamingo-tech.nl/2021/07/10/xiaomi-modchip-open-source/)中创建自己的 mod-chip，或者从[火烈鸟科技的 Tindie 商店](https://www.tindie.com/products/theflamingo/xiaomi-air-purifier-3hcpro-mod-no-nfc-mod/)中抓取一个。

我们通常听说 [mod-chips 与游戏](https://hackaday.com/2021/03/04/arduboy-fx-mod-chip-now-youre-playing-with-power/)有关，但我们很高兴将这一荣誉扩展到 [3D 打印机](https://hackaday.com/2016/01/12/hacking-chipped-3d-printer-filament-on-the-da-vinci-printer/)。你骗过“剃刀”吗？

 [https://www.youtube.com/embed/YJmcQXRz9bo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/YJmcQXRz9bo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



谢谢你的提示。