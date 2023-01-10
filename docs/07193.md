# 谷歌提供的莫尔斯电码语音

> 原文：<https://hackaday.com/2020/07/16/speech-to-morse-code-courtesy-of-google/>

谷歌在世界上推出了一些非常不可思议的硬件和软件，但他们只能部分归功于【威士忌酒吧】最近完成的[语音到莫尔斯电码小工具](http://www.whiskeytangohotel.com/2020/07/send-morse-code-cw-with-your-voice.html)。

有了谷歌 AIY 语音帽，[威士忌酒吧]就有了一切他需要的东西来获取人类的语音，并将其转化为树莓 Pi 可以解析和处理的文本。通常，这将被传递到某种虚拟助理软件，但在这种情况下，Python 脚本将语音分解为单个字符，并查找它们的莫尔斯表示。所有这些“dits”和“dahs”然后被发送到 Pi 的 GPIO 引脚之一，一个继电器已经连接到该引脚。

在这一点上，你已经有了一个有趣的小玩具，它可以坐在你的桌子上，当继电器咔哒咔哒地传递信息时，将你的讲话转换成可听见的莫尔斯电码。事实上，如果你没有业余无线电执照，这可能是你应该停止的地方。但是，如果你已经做了适当的文书工作来通过空中传输，继电器可以连接到无线电来实际传输信息。

如果你认为让谷歌访问你的莫尔斯电码信息的内容太过分了，那么[你只能自己学习了](https://hackaday.com/2020/02/21/learning-morse-code-the-ludwig-koch-way/)。也许不再需要获得业余执照了，[但这并不意味着不值得了解](https://hackaday.com/2019/06/18/morse-code-catches-google-swiping-lyrics/)。

 [https://www.youtube.com/embed/sXofFDRuACI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/sXofFDRuACI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

