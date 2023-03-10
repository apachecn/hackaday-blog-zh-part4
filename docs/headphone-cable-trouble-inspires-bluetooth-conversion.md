# 耳机线故障激发了蓝牙转换

> 原文：<https://hackaday.com/2022/07/06/headphone-cable-trouble-inspires-bluetooth-conversion/>

[adblu]在他们的 Sennheiser Urbanite 耳机上遇到了一直存在的耳机问题——电缆断了。这些耳机是体面的，尽管电缆的麻烦，值得给一个新的生活。更换线缆始终是一个选择，但[adblu]决定看看——如何才能让这些耳机无线化？当他们这样做的时候，他们的电池寿命能有多长？

配备了 CSR8635 蓝牙音频接收器分线模块和 TP4056 充电器，[adblu]继续为耳机内部重新布线。CSR8635 内部已经有一个扬声器放大器，所以连接耳机的扬声器并不需要太多的努力——除了一般的焊接困难，因为[adblu]的烙铁对于 BT 模块上的小焊盘来说太大了。他们还找到了一个 2400 毫安时的电池，并在大量的 dremel 工作后将其安装在耳机体内。

结果没有令人失望——不仅一切都适合耳机主体，耳机还以不同的音量提供了 165 小时的音乐播放。就电子产品而言，[给你的耳机加装蓝牙真的很容易，但是你可以更进一步，](https://hackaday.com/2018/10/30/a-bluetooth-upgrade-for-an-unusual-set-of-headphones/)[设计一套复杂的定制印刷电路板！](https://hackaday.com/2018/07/09/vintage-headphones-bluetooth-conversion-goes-the-extra-mile/)如果你更喜欢固件黑客，你可以使用 CSR8645 模块构建，然后[修改它的固件。](https://hackaday.com/2017/01/30/reprogramming-bluetooth-headphones-for-great-justice/)