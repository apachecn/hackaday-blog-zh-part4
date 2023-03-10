# 有趣的是，猎鹰 9 号的遥测技术已经加密

> 原文：<https://hackaday.com/2021/04/07/fun-while-it-lasted-falcon-9-telemetry-now-encrypted/>

几周前，我们带来消息称，Reddit 用户[derekcz]和[Xerbot]已经成功接收到猎鹰 9 号上面级的 2232.5 MHz 遥测下行链路，并拉出了一些有趣的纯文本字符串。随着软件的进一步摆弄，飞行器的视频流被解码，产生了一些从低地球轨道拍摄的火箭及其有效载荷的绝对惊人的照片。

不幸的是，看起来那些令人兴奋的日子现在已经结束了，因为[【derekcz】报告说，最新的猎鹰 9 号任务的下行链路只是清晰的噪音](https://www.reddit.com/r/amateursatellites/comments/mm8fcz/spacex_vehicle_decoding_and_encryption_part_2_its/)。由于他这边的硬件和软件没有改变，唯一合乎逻辑的结论是 SpaceX 对业余无线电爱好者监听他们的火箭不太满意，并决定采用某种形式的加密。

由于这些数据显然在地面上的任何人注意到之前已经被清楚地广播了近十年，所以很容易认为这是一种过度反应。毕竟，几个组装天线的极客偷看一堆 Starlink 卫星有什么坏处呢？[derekcz]甚至沉思道，允许业余爱好者捕捉这些太空景观可能会为公司赢得一些积极的宣传，这是埃隆·马斯克似乎永远不会满足的。

[![](img/f5b2047eacee908dbe02379f37d2ef18.png)](https://hackaday.com/wp-content/uploads/2021/04/falconradio_detail.jpg)

Some of the images [derekcz] was able to capture from the Falcon 9

另一方面，我们知道 SpaceX 正在积极寻求更有利可图的猎鹰 9 号和猎鹰重型的国家安全发射合同。对于这些敏感的政府有效载荷，正常的屏幕遥测数据和空间视图从公司的官方直播流中被省略。五角大楼似乎非常有兴趣了解平民是如何获得这些信息的，SpaceX 保证未来所有航班的链接都将加密，这可能有助于平息事态。

在帖子的最后，[derekcz]呼应了我们最近从其他业余无线电运营商那里听到的一种情绪，即很快太空可能会成为我们平民的禁区。随着旧的气象卫星开始失效，并被更新的、不可避免的更复杂的模型所取代，T2 用 RTL-SDR 和几行 Python 代码获取卫星图像的日子可能屈指可数了。