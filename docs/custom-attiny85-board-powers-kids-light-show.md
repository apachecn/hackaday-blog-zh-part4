# 定制 ATTiny85 板为儿童灯光秀提供动力

> 原文：<https://hackaday.com/2018/07/27/custom-attiny85-board-powers-kids-light-show/>

我们常说，父母是黑客和创造者的孩子一定是世界上最幸运的孩子。当所有其他的孩子不得不满足于亚马逊的一些大规模生产的胡说八道时，他们已经拥有了这个星球上一些最精心设计和制造的玩具和小玩意。毕竟，任何称职的黑客都不会为自己的孩子付出低于 110%的努力。

[![](img/4093de52e8eff92ee87c4535af38c774.png)](https://hackaday.com/wp-content/uploads/2018/07/kidstar_detail1.jpg) 一个很好的例子就是【意想不到的制造者】为他的孩子打造的这个 [RGB 星星小夜灯。星星本身足够简单，只是一个用透明 PLA 印在他 Prusa i3 上的基本形状。令人印象深刻的是他如何点燃它。他没有像我们以前多次看到的那样在那里贴上 Arduino 或 ESP8266，而是专门为控制 RGB LED 灯条而组装了自己的定制 ATTiny85 板。](https://github.com/UnexpectedMaker/KidsStarNightlight)

他称之为 TinyDev 的电路板的设计厚度与 NeoPixel 风格的 LED 灯条相同，因此可以安装在狭小的空间内。他将它焊接到 LED 灯条的末端，加上光敏电阻，这样星星就可以知道什么时候该点亮了，然后将整个装置蜿蜒穿过印在星星上的通道。中间有个电池组，不过也就这些了。它确实允许非常干净的 LED 灯条实施，当你可以将控制器塞进与灯本身相同的空间时，人们不禁开始思考有趣的可能性。

[意想不到的制造商]已经为任何想建造自己的 TinyDev 的人完全开源，但如果你想快速得到一个来玩的话，它也可以在 Tindie 上得到。如果你想用更主流的方法点亮小家伙的房间，[我们也能满足你的需求](https://hackaday.com/2018/06/07/ambient-lighting-for-baby-with-the-esp8266/)。

 [https://www.youtube.com/embed/u-KtG9Ui_h8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/u-KtG9Ui_h8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

