# 这位业主控制了他们专有的警报系统

> 原文：<https://hackaday.com/2019/04/27/this-owner-took-control-of-their-proprietary-alarm-system/>

当有消息传来时，提供消息的人觉得他们必须向我们保证，尽管表面上看，他们的主题不是在帮助犯罪，但这肯定会引起我们的注意。[Flam2006]有一个 Brinks 家庭安全系统，只能使用只有安装人员才能使用的特殊设备进行配置，尽管他们通过易贝的销售成功获得了一个，但他们还是麻烦地对其协议进行了逆向工程，并用 Python 编写了[一个软件仿真器](https://github.com/flarn2006/BHSTools/)。当一个所有者黑进他们自己的安全系统来获得对他们所拥有的东西的完全控制时，那就是我们的职责所在。

通信通过 RS485 串行线进行，遵循二进制而非 ASCII 数据的分组结构。有一个几乎即插即用的系统，用于识别连接到控制器的设备，尽管它仅限于控制器已经知道的那些设备。有一个官方的控制器编程方法的视频，以及一个正在运行的软件。为了让你开心，我们把它们贴在了休息时间的下面。

在你自己的财产上执行这些任务的能力是一项重要的权利，但这项权利有时受到诸如 DMCA 等立法的威胁。我们已经接触过无数次，但我们和更广泛的媒体报道过的最引人注目的例子可能是那些关于 John Deere 拖拉机零件锁定的故事。

 [https://www.youtube.com/embed/Ds8WccQH8_E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Ds8WccQH8_E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/SxdBnXzYWWQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/SxdBnXzYWWQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

