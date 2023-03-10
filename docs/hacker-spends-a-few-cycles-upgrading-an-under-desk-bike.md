# 黑客花了几个周期升级一辆桌下自行车

> 原文：<https://hackaday.com/2021/05/06/hacker-spends-a-few-cycles-upgrading-an-under-desk-bike/>

疫情让你远远落后于你的锻炼目标？我们也是。但买了一辆桌下自行车，一边敲键盘一边骑自行车的人可不这么想。这辆自行车唯一的缺点是附带的应用程序——它的整体性能很差，而且需要太多的步骤才能骑行。了解你自己是值得的，[codaris]知道这将是一个主要的消极因素，[开发了一个桌面应用程序，它可以做所有的事情](https://codaris.github.io/UnderDeskBike/)，包括/一旦踏板开始旋转就启动。

[codaris]开发了一个 Windows 应用程序，可以实时显示锻炼数据，然后在踩踏板停止后将统计数据保存在 SQLite 数据库中。这需要相当多的工作才能实现，记录骑行期间的蓝牙流量，并与实时会话的 Wireshark 输出进行比较，以解码自行车和应用程序之间的通信。原来总共有六个命令，而[codaris]实际上只需要三个——连接、开始锻炼和继续锻炼。

该应用程序显示经过的锻炼时间、速度、跑步距离和当前转速。我们喜欢它在[codaris]开始踩踏板时就开始记录和显示数据，因为这也是我们的一个主要目标。

破解自行车的方法不止一种。【codaris】的灵感来自于[【pt x2】的出色工作，他用覆盆子 P](https://hackaday.com/2020/08/04/unbricking-a-2000-exercise-bike-with-a-raspberry-pi-zero-and-bluetooth-hacks/) i 拆除了一辆昂贵得多的自行车。

感谢提示，[Jhart99]！