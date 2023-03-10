# 通过口琴进行数字表达

> 原文：<https://hackaday.com/2020/09/15/digital-expression-via-harmonica/>

很有可能你是用鼠标、轨迹球、触控板或者手指点击了这篇文章。我们的手是我们大多数人与数字世界互动的方式，但这不是每个人的选择，[舒高桥]希望给他们一个新的表达自己的渠道。一些不能用手的人将能够使用[Magpie MIDI，它可以充当键盘、鼠标、MIDI 设备](https://hackaday.io/project/174136-magpie-midi-an-adaptive-midiinterface-harmonica)，并最终成为游戏控制器。这种通用人机界面设备(HID)不同于用嘴操作的操纵杆，因为它有气压传感器而不是按钮。传感器可以识别呼气和吸气之间的差异，因此 13 个端口可以是中性的、正的或负的，这就像有 26 个分立的按钮。

口琴安装在一个模拟的 X-Y 操纵杆上来移动鼠标指针或操纵 MIDI 声音，就像一个晦气棒。[舒]知道标准口琴有 10 个端口，但他选择了 13 个，因为所有 26 个字母都可以在键盘模式下通过吹气或啜饮来访问。输入数量超过 Arduino Leonardo 的模拟输入，因此有一个多路复用器来读取所有输入。没有足够的时间来获得一个有足够的本地端口的 Arduino，像 Teensy 一样，内置 HID 支持。大部分结构是 3D 打印的，因此零件将是可替换的，甚至可能是可定制的。

即使有两只手，我们也喜欢用不同的硬件来练习，但是 T2 口琴是一个很好的工具，可以安装在你的电脑上。

 [https://www.youtube.com/embed/hUoyafEdK-Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/hUoyafEdK-Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



The [HackadayPrize2020](https://prize.supplyframe.com) is Sponsored by:[![Supplyframe](img/193ca31946d20fcfa39296cb816a4c50.png)](https://supplyframe.com/)[![Digi-Key](img/4fc24a8a6b4498aecfe987b00009d192.png)](https://www.digikey.com/)[![Microchip](img/8dd361210bbb0e5592c24f87e4e2267e.png)](https://www.microchip.com/)[![Arm](img/7d728b281b85469ef9013d45001f14b4.png)](https://www.arm.com/)