# node-红色激光射击馆无处不在

> 原文：<https://hackaday.com/2020/01/14/node-red-laser-shooting-gallery-goes-anywhere/>

当你想到一个射击场时，你可能会想象一排锡罐沿着分离式围栏排列，或者几排鸭子或瓶子在嘉年华上排列。但是这些有什么共同点呢？你，站在一个地方，朝同一个方向射击。你暴露了！如果那些目标可以还击，你会在几秒钟内死亡。如果目标 360°都在你身边不是更好玩吗？我们也这么认为。

所以你怎么可能以这种方式建立一个射击场？[【另一个制造者】已经用 ESP32s 和 Node-RED](https://www.youtube.com/watch?v=cY0ELz11IpI) (YouTube)为你解决了那个问题。每个目标都有一个 ESP32，一个激光传感器和一个 LED，当目标准备好时，它就会亮起，一旦被击中，它就会熄灭。它们都发出诱人的“开枪吧”的声音，与它们的图形相匹配，直接点击时会播放第二个 mp3。

PVC 枪装有一个 ESP8266，这是一个位于枪管末端的激光模块，依靠滑入第二手柄的圆柱形 USB 电池运行。[另一个制造者]可以将目标分散到很远很广的地方，只要它们都在本地 WiFi 接入点的范围内。

最棒的是，Node-RED 系统是目标不可知的——它不关心你有多少或它们是如何制造的，它可以处理多达 250 个。由于目标对象的编程方式，很容易添加致动器，使它们在被击中时落下或向后倒下。你也可以实现[另一个制作者]的绝妙建议，用 NERF 飞镖击中街机按钮。给这些激光充电，按下中断按钮，观看演示和演练视频。

如果您计划在实现中推翻或推翻目标，您将需要一种简单的方法来重置它们。[这是一个废弃的射击场，它使用一个挡风玻璃刮水器马达来备份它们](https://hackaday.com/2012/01/03/laser-shooting-gallery-made-from-scrap/)。

 [https://www.youtube.com/embed/cY0ELz11IpI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/cY0ELz11IpI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



通过 [r/duino](http://reddit.com/r/arduino/comments/emvniv/laser_shooting_galley_that_handles_up_to_250/)