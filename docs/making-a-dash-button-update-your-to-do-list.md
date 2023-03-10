# 让一个破折号按钮更新你的待办事项列表

> 原文：<https://hackaday.com/2019/04/18/making-a-dash-button-update-your-to-do-list/>

亚马逊的 Dash 按钮是有用的小设备，让你按下按钮就可以自动订购各种各样的普通家居用品。它们便宜、无线且容易获得，这使得它们适合黑客攻击。在这种情况下，[Inbar]和[Ezra] [找到了一种让 Dash 按钮更新其待办事项列表的方法。](http://www.failuntilyouwin.com/project/iot/2019/03/31/using-an-amazon-dash-button-with-anydo.html)

[Inbar]使用 Any.do 来管理他的待办事项列表。没有公共 API，但该服务可以配置为响应 Alexa 命令。自然，这意味着如果一个破折号按钮可以被配置成触发语音命令，Alexa 就会对列表进行必要的添加。

这是通过大量的 Python、树莓 Pi 和苹果的文本到语音引擎实现的。Raspberry Pi 被设置为无线热点，Dash 按钮连接到该热点。当按下按钮时，当按钮试图呼叫总部时，会发出 DHCP 请求。通过从这个请求中抓取 MAC 地址，Raspberry Pi 可以识别哪个按钮被按下，然后播放苹果公司的 Samantha voice 的录音样本。这个声音被特别选择为 Alexa 最可靠理解的声音，Alexa 负责解析语音命令并更新 Any.do 上的列表。

这是一种厚颜无耻的黑客行为，它不关心与各种服务和工具接口的本质。相反，它结合了一系列易于使用的软件和硬件，同样可以完成工作。

正如我们所见，[亚马逊的破折号按钮已经被彻底修改了。](https://hackaday.com/2015/12/02/amazon-dash-button-pwn3d/)休息后的视频。

 [https://www.youtube.com/embed/xJCstaNtBqk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/xJCstaNtBqk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

