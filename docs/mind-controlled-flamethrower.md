# 精神控制喷火器

> 原文：<https://hackaday.com/2021/05/12/mind-controlled-flamethrower/>

精神控制可能看起来像是科幻剧里的东西，但就像平板电脑、通用翻译器或虚拟现实设备一样，实际上是一项已经进入现实世界的技术。虽然这些设备通常需要先进和昂贵的设备来正确地解释脑电波，但有了正确的机器学习系统，就有可能以小得多的预算做像[这种精神控制火焰喷射器](https://www.youtube.com/watch?v=Y4YidkzHzRk)这样的事情。(视频，嵌在下面。)

[Nathaniel F]已经在尝试使用脑机接口和机器学习，并想看看他是否能结合这两种技术建立一些实用的东西。他没有求助于脑电图机器来读取大脑模式，而是选择了一个便宜得多的 Mindflex，[将其与运行 TensorFlow 的机器学习系统](https://www.hackster.io/NathanielF/using-machine-learning-to-mind-control-a-flamethrower-27ba4c)配对，以弥补其一些缺点。这个过程是由 Raspberry Pi 4 完成的，当它检测到正确的思维模式时，它会向 Arduino 发送命令来发射火焰喷射器。不要忘记这个建筑的火焰喷射器部分:它完全是由[纳撒尼尔 F]设计和建造的，并且使用气体和电弧打火机。

虽然该构建花费了许多小时的训练来收集适量的数据以构建神经网络，并作为他所希望的概念证明，但[Nathaniel F]指出，可以通过用更好的 EEG 替换过时的 Mindflex 来改进它。不过现在，我们喜欢在现实世界中看到像这样的项目中的科幻，或者在其他精神控制的项目中，比如这个[将义肢转换成精神控制的音乐合成器](https://hackaday.com/2020/02/19/hacked-prosthesis-leads-to-mind-controlled-electronic-music/)。

 [https://www.youtube.com/embed/Y4YidkzHzRk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Y4YidkzHzRk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

