# 神经网络识别鸟叫，甚至在你的 Pi 上

> 原文：<https://hackaday.com/2022/06/25/neural-network-identifies-bird-calls-even-on-your-pi/>

最近，我们偶然发现了鸟网研究平台的广泛努力。 BirdNET 利用神经网络通过鸟类发出的声音来识别鸟类，是康奈尔鸟类学实验室和开姆尼茨理工大学的联合项目。给我们留下深刻印象的是——这个项目非常有特色，并且可以用于各种应用程序。毫无疑问，BirdNET 的目标是成为一个一站式商店，在鸟儿唱歌时识别它们。

BirdNET 有很多方法可以帮助你。从可能是我们当中最受欢迎的选项开始，有 [iOS](https://apps.apple.com/us/app/birdnet/id1541842885) 和 [Android](https://play.google.com/store/apps/details?id=de.tu_chemnitz.mi.kahst.birdnet) 应用程序——给我们口袋里带麦克风的“智能”设备提供了一个即使是最厌恶应用程序的黑客也能尊重的功能。然而，BirdNET 团队也谈到将声音识别引入我们的浏览器、Raspberry Pi 和其他 SBC，甚至微控制器。我们不能等着有人把鸟网带到 RP2040 上！[代码是开源的，](https://github.com/kahst/BirdNET-Analyzer)[模型是免费提供的](https://github.com/kahst/BirdNET-Analyzer/tree/main/checkpoints)——几乎没有一个用例不能用这些来覆盖。

关于那个树莓派版本！有一个姐妹项目叫做[bird net-Pi](https://birdnetpi.com/)——这是一个易于安装的用于 Raspberry Pi 操作系统的软件包。为您的 Pi 配备了 USB 声卡后，您可以使用“精简”版本的 BirdNET 让它进行 24/7 记录和分析。然后，你得到一个网络界面，你可以登录并看到实时识别的鸟叫声。不仅如此——bird net-Pi 还处理声音并创建频谱图，将声音保存在数据库中，甚至可以向您发送通知。

BirdNET-Pi 项目也是[开放的，当然是](https://github.com/mcguirepr89/BirdNET-Pi)。不仅如此——bird net-Pi 团队强调一切都是完全本地的，除非你选择其他方式，或许决定[与他人分享。](https://github.com/mcguirepr89/BirdNET-Pi/wiki/Sharing-Your-BirdNET-Pi)许多人确实公开了他们的 BirdNET-Pi 实例，还有[一个可爱的互动地图](https://app.birdweather.com/)显示了世界各地的鸟叫声！

毫无疑问，BirdNET 是一个高投入的项目——也是一个光辉的例子，表明一个专注的研究团队可以用神经网络和一个令人钦佩的目标做些什么。对于我们许多人来说，当我们听到外面的鸟叫时会感到高兴，知道我们可以将 USB 声卡插入我们的 Pi 并了解更多关于它们的信息是令人愉快的——即使我们还不能通过视觉发现或识别它们。我们之前已经[讨论过微控制器](https://hackaday.com/2021/07/06/recognising-bird-sounds-with-a-microcontroller/)上的鸟类声音识别——也是使用机器学习。