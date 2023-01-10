# 使用语音命令启动吉普车

> 原文：<https://hackaday.com/2020/03/06/using-voice-commands-to-start-a-jeep/>

如果你有一辆在过去 5 年左右制造的汽车，它很可能是在有遥控钥匙的情况下按下按钮启动的。老式汽车用钥匙转动就可以了。当然，通过语音命令启动汽车会很酷，[这就是【约翰·福赛斯】开始做的事情](https://hackaday.io/project/169996-macbook-speech-recognition-starts-a-jeep)。

该产品使用 Macbook 的听写功能来处理语音识别。通过大量下载，它能够离线完成任务，使事情变得更容易。口述的单词被传递给 Python 脚本，该脚本搜索像“start”和“go”这样的单词作为触发器。当收到适当的命令时，Python 脚本通过 USB 串行连接向连接的 Arduino 发送信号。Arduino 然后触发连接到吉普车外部启动器螺线管的继电器，启动车辆。

作为最近流行电影的粉丝，[约翰]对系统进行了编程，以响应命令“贾维斯，让我们开始吧！”，导致车辆突然启动。未来也有改进的空间——该系统可以从更紧凑一点中受益，并且在完成句子和车辆启动之间有很长的延迟。树莓派和更快的听写软件在这方面可能会有所帮助。

我们已经看到语音命令被用于从国际象棋到寻找电子元件的各种事情。休息后的视频。

 [https://www.youtube.com/embed/j-GmDpiXWng?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/j-GmDpiXWng?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

