# 这个电子管前置放大器有一个谢妮音量显示器

> 原文：<https://hackaday.com/2020/07/25/this-tube-preamp-has-a-nixie-volume-display/>

高保真音响发烧友的追求是一个用了许多最高级的东西，也许还花了太多钱的领域。但这也是一个领域，自建者可以生产自己的设备，这些设备与购买的设备一样好，甚至更好，因此它提供了大量有趣的项目。[【Justin Scott】的电子管前置放大器就是一个很好的例子](https://hackaday.io/project/173231-vacuum-tube-preamplifier-with-nixie-display)，它新颖地使用了一对谢妮电子管来指示音量。

前置放大器的音频端来自于来自 tubes 4 hi-fi 的四管套件[，其中我们注意到另一个管作为电源整流器。这个箱子是一个制作精美的木制东西，带有专业的前面板，但它是 Nixies，使它有点特别。高品质电动电位计用作音量控制，其多路输出之一用作简单的分压器来提供电压。它由 Arduino 读取，然后通过 BCD-to-decimal 解码器驱动 Nixies。在整个项目中，对细节的关注是非常高的，尽管他没有与我们分享任何音频测量，但我们希望它听起来和看起来一样好。](http://www.tubes4hifi.com/PH16.htm)

如果你对电子管放大器感兴趣，[我们过去曾深入研究过它们的设计](https://hackaday.com/2014/06/04/keep-those-filaments-lit-design-your-own-vacuum-tube-audio-equipment/)，也值得你去看看[贾斯汀的匹配放大器，](https://hackaday.io/project/168078-20-wpc-vacuum-tube-amplifier)。