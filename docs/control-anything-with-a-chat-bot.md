# 用聊天机器人控制任何东西

> 原文：<https://hackaday.com/2019/01/05/control-anything-with-a-chat-bot/>

在物联网的世界里，很容易就能把东西连接到互联网上。但是你应该用什么来沟通和控制它呢？有许多可用的标准和工具，但是最好的选择总是使用您手头的工具。[Victor]发现自己处于这种情况，并发现控制联网汽车的最佳方法是使用他已经拥有的 Flask 服务器。

遥控汽车原本应该配备 Arduino，但微控制器在到达时丢失了。他有一个树莓派，并能够设置它来取代 Arduino。与 Arduino 相比，他还利用这个机会使用了 Pi 的扩展功能，并编写了一个 Flask 服务器来控制它，就像你在与聊天机器人通信一样访问它。例如，向 Flask 服务器发送单词“向左/向前”将相应地控制汽车。

聊天机器人本身也包含一些精华，对于任何使用正则表达式的项目都很有用。它似乎也很容易扩展。该项目还使用语音命令，并通过大量使用 [Mozilla 的语音识别套件](https://developer.mozilla.org/en-US/docs/Web/API/Web_Speech_API)来做到这一点。如果你想独自深入语音识别领域，你也可以在闲暇时[探索 TensorFlow](https://hackaday.com/2017/03/24/ten-minute-tensorflow-speech-recognition/) 。