# 隐私踏板

> 原文：<https://hackaday.com/2020/09/29/push-pedal-for-privacy/>

我们中的许多人在秘密 Hackaday 老巢的办公桌上使用游戏硬件，因为它可靠且性能良好。我们并不孤独，也许你正通过一个 20 键鼠标在喝咖啡休息时阅读这篇文章。我们打赌[蒂亚戈·里贝罗·德·阿泽雷多]有这种心态，因为他把一些旧的模拟游戏踏板改造成了他家庭办公室的电话会议工具。现在，他不用急着去办公室了，他不得不接很多电脑电话，而且当他嚎叫的儿子试图上台时，他必须迅速而秘密地将麦克风静音。

当他开始在家工作时，踏板上积满了灰尘，但为了升级，它们还没有恢复。在内部，没有什么神秘之处，只有几个弹簧加载的可变电阻，所以他添加了一个 Arduino Nano 几个 4.7kω的电阻来创建一个分压器。Nano 没有本机人机接口设备(HID)功能，因此 Python 脚本接收串行端口信号并切换应用程序栏通知，以便他可以看到麦克风状态。有了两个踏板，他可以按下通话或锁定麦克风的开关。我们不得不怀疑，他是在开会的时候写的软件吗？

我们喜欢用脚控制我们的战斗位置的想法，或者看到一堆被用作低分辨率显示器的 T2 RGB 键盘。

The [HackadayPrize2020](https://prize.supplyframe.com) is Sponsored by:[![Supplyframe](img/193ca31946d20fcfa39296cb816a4c50.png)](https://supplyframe.com/)[![Digi-Key](img/4fc24a8a6b4498aecfe987b00009d192.png)](https://www.digikey.com/)[![Microchip](img/8dd361210bbb0e5592c24f87e4e2267e.png)](https://www.microchip.com/)[![Arm](img/7d728b281b85469ef9013d45001f14b4.png)](https://www.arm.com/)