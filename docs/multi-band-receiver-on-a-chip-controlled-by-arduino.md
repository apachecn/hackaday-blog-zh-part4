# Arduino 控制的片上多频段接收机

> 原文：<https://hackaday.com/2020/03/02/multi-band-receiver-on-a-chip-controlled-by-arduino/>

Silicon Labs Si4735 是一款用于接收 AM、FM 和短波广播的单芯片解决方案。稍加黑客攻击，它甚至支持单边带(SSB)。你所要做的就是给它提供一个合适的控制界面，里卡多·利马·卡拉蒂在他最近的项目中已经做到了。

[![](img/99fce5be62fbba498e5f4115aa0846c2.png)](https://hackaday.com/wp-content/uploads/2020/02/arduradio_detail.jpg) 使用一个 Arduino Pro Mini、几个按钮和一个标准的 TFT 显示屏，【Ricardo】组装了一个可维护的小接收器，具有相当令人印象深刻的用户界面。我们特别喜欢指示信噪比和接收信号强度的水平条。下一步的发展是将整个装置放入某种外壳中，但目前他似乎满足于通过一块 perfboard 上的几个无标签按钮来控制行动。

当然，这个接收器的展示并不是重点；这更多的是一个概念的证明。你看，[Ricardo]实际上是开发库的人，该库允许你从你选择的微控制器通过 I2C 控制 Si4735。他目前已经用 Arduino 家族的几个成员(不那么官方)和 ESP32 测试过了。

[Ricardo]为他的 MIT 授权 Arduino Si4735 库收集的文档简直是惊人的。说真的，如果所有开源项目都有这个项目一半的文档记录，我们就离世界和平更近了一步。即使你对在你的下一个项目中加入短波无线电接收不是特别感兴趣，你也必须浏览他的文档，看看高潮在哪里。

事实上，我们第一次听说这个库是在几天前[，当时我们报道了另一个使用 Si4735](https://hackaday.com/2020/02/12/all-band-radio-uses-arduino-and-si4730/) 的接收器，而【Ricardo】突然加入评论，分享他为[推动这种有前途的芯片](https://hackaday.com/2018/04/22/an-fm-transceiver-from-an-unexpected-chip/)的最先进水平所做的一些工作。

 [https://www.youtube.com/embed/oL8qyRglZ8I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/oL8qyRglZ8I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

