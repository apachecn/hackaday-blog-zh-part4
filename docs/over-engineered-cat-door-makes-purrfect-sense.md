# 过度设计的猫门非常有意义

> 原文：<https://hackaday.com/2019/09/16/over-engineered-cat-door-makes-purrfect-sense/>

理论上，宠物门是很棒的。不用一直让猫进进出出，整体上门上的划痕应该会少一些。不幸的是，你的普通宠物门是不分青红皂白的，会让任何老动物华尔兹的权利。嗯，[耶利米]厌倦了不请自来的小动物，[所以他建造了一扇内置弹跳器的电动门](https://www.hackster.io/fwrawx/rpi-3-ble-cat-door-f3bfc8)。现在，只有带有预先批准的 BLE 标签的动物才能进入。

保镖是一个运行 Node-RED 的 Raspi 3，它不断扫描猫项圈上的 BLE 广告。[Jeremiah]选择瓷砖标签是因为它们可靠且防猫。第一个版本为猫使用了 Arduino 和 RFID 标签，但它们必须离门太近才能触发它。

我们喜欢[Jeremiah]选择的门致动器，一个 12V 可伸缩的汽车天线。[Jeremiah]使用天线本身来提升和降低门附带的可移动锁定面板。他拆除了断电时收回天线的电路，这样停电就不会成为寻求庇护的动物们的混战。

对于慢动作动物来说也有一个很好的功能——在最后一个 BLE 广告后 15 秒钟，门才会关闭，所以它们的猫永远不会有印第安纳琼斯那样的开场。磁性开关目前限制门在顶部和底部的移动，尽管[Jeremiah]最终会用标准开关取代它们。暂停一下，直到你看到一段视频。

猫就是猫，出去玩的猫可能会被清点人数。这是一扇猫门，它寻找被猫咬住的受害者，并开始 15 分钟的锁定期。

 [https://www.youtube.com/embed/6Cnj6fomOQg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/6Cnj6fomOQg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



谢谢你的提示，[baldpower]。