# 简单的 MP3 播放器隐藏了家庭自动化的辉煌

> 原文：<https://hackaday.com/2020/08/17/simple-mp3-player-hides-home-automation-brilliance/>

像气泡包装或开瓶器一样，许多日常用品已经失去了与它们最初用途的所有联系。可能是最初的产品没有市场，但是能够在一个意想不到的地方找到一个，或者仅仅是最初的用例消失了。我们认为，由于[Sebastian]最近的一个项目，这款儿童 MP3 播放器可能会遭遇与家庭自动化控制器相似的命运。

这种 MP3 播放器被称为 Jooki，通过使用小雕像(和几个按钮)来控制设备。例如，不同的小雕像使 MP3 播放器改变播放列表，但结果是该设备能够通过 [MQTT](https://en.wikipedia.org/wiki/MQTT) 进行通信。这意味着[Sebastian]能够使用来自 Jooki 的 MQTT 消息来做各种超出其与 openHAB、[一个开源家庭自动化系统](https://hackaday.com/2017/02/06/using-sdr-to-take-control-of-your-home-security-system/)的预期用途的事情，例如当他让儿子睡觉时调暗灯光和关闭百叶窗。

由于该平台在引擎盖下使用了轻量级通信系统，因此它具有相当大的黑客攻击潜力。Jooki 有点贵，但是如果你身边正好有一个，它是一个令人印象深刻的工具，可以远远超出其最初的预期用途。