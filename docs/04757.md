# 借助 PowerCore 和 FluxLamp，回流成为可能

> 原文：<https://hackaday.com/2019/12/10/with-powercore-and-fluxlamp-reflow-is-possible/>

[nathan]提交了这个项目组合，这些项目组合在一起构成了一个非常有趣的回流焊炉。

首先是 [PowerCore](https://nathan.vertile.com/blog/2019/04/07/vertile-powercore/) ，它有两个微控制器，一个 ATmega 和一个 ESP8366 协同工作，以设定的时间间隔打开和关闭交流电。GLCD 显示当前配置文件，WiFi 也允许远程控制。输入由瞬时开关旋转控制器处理。在阅读了商业控制器的论坛后，他决定走这条路，并认为它们需要太多的摆弄，而且对黑客不够友好。

PowerCore 然后连接到一个[卤素工作灯](https://nathan.vertile.com/blog/2019/04/24/fluxlamp-the-soldering-reflow-over-for-hackers/#2d08533af)。他从卤素灯上取下前玻璃，用铝箔盖住。这成为了[烤箱](https://hackaday.com/2019/03/10/diy-reflow-oven-is-heavily-documented/)的底座。PowerCore 和传感器安装在背面。使用照明元件作为加热元件是有意义的，正如我们从曲线中看到的，似乎提供了非常准确的响应。

最重要的是[内森]已经很好地记录了这个项目。小尺寸和良好的控制使它在我们推荐的回流焊版本列表中名列前茅。

The [HackadayPrize2019](https://prize.supplyframe.com) is Sponsored by: [![Supplyframe](img/79a7db035b8a2b6c2b7b0895c45b7de8.png)](https://supplyframe.com/)  [![Digi-Key](img/ba094a14c430ab81591a2abdc54a5363.png)](https://hackaday.io/digikey)  [![Microchip](img/5023ef0b7ff1aee311cba9b54a3ac9fe.png)](https://hackaday.io/microchip)