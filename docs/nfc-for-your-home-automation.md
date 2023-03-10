# 面向家庭自动化的 NFC

> 原文：<https://hackaday.com/2020/01/30/nfc-for-your-home-automation/>

如果物联网时代的家庭自动化教会了我们什么，那就是没有人愿意跑电线。我们中的许多人都租房住，所以新的布线甚至不是一个选项，即使我们想走这条路。如果你想要一个独特的传感器，你必须自己制造，而[tmkThings]希望在他的前门安装一个[NFC 扫描仪。就像上班一样，他扫描自己的证件，门就会自动打开。](https://www.tindie.com/products/thematthewknot/nfc-wifi-board/)

在一个白色的小盒子里，我们发现一个 ESP8266 语音 Wifi 连接到一个 PN532 语音 NFC，这两个名字在这些页面上都很熟悉。该代码可以在 GitHub 上获得，它连接了 IFTTT 和 MQTT。出于安全考虑，我们不会在你的前门上看到这个，但你可以触发你想象力的极限事件，从在一天结束时播放你最喜欢的果酱到在睡觉时关掉所有的电视。

NFC 黑客攻击很棒，因为它们很容易被识别，阅读器也不贵，但在我们的书中,[死栓黑客攻击](https://hackaday.com/2019/03/25/wifi-your-door-lock-with-an-esp/)很有趣。

 [https://www.youtube.com/embed/mKFkm8zK5ho?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/mKFkm8zK5ho?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



谢谢[c00p3r]的提示。