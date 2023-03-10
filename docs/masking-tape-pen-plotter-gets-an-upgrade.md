# 遮蔽胶带笔绘图仪升级

> 原文：<https://hackaday.com/2022/07/10/masking-tape-pen-plotter-gets-an-upgrade/>

[创新先生]决定[制作他的小型笔式绘图仪](https://www.youtube.com/watch?v=Y_rrbo6_42U)(休息后的视频)在胶带上制作标签。其结果是一个令人印象深刻的紧凑型机器，使用您的智能手机远程控制。绘图仪是使用几种不同的技术构建的，一块胶合板作为底座，一个用于电机和笔支架的 3D 打印支架，以及一个用于固定丝杠和线性导轨组件的路由丙烯酸板。整个事情由安装在定制电机驱动器载板上的 Arduino Nano 控制。

这个建筑的灵感来自于[michimartini]又名[融化的奶酪熊]的一个项目，我们几个月前报道过这个项目。[创新先生]选择皮带而不是直接驱动，没有本地屏幕。它似乎也能更快地打印出来，但这可能是由于所用墨水笔的不同。一个名为 *TextToCNC* 的 Android 应用程序将标签文本转换成 g 代码， *Grbl 控制器*应用程序将这些命令发送到绘图仪。

我们喜欢开源项目的持续迭代，并期待看到下一代的样子。感谢[keithfromcanata]提交此技巧。

 [https://www.youtube.com/embed/Y_rrbo6_42U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Y_rrbo6_42U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

