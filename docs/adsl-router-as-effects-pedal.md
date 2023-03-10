# 作为效果踏板的 ADSL 路由器

> 原文：<https://hackaday.com/2022/09/08/adsl-router-as-effects-pedal/>

摩尔定律可能不像我们曾经认为的那样不可改变，因为芯片制造商正在努力在给定的硅面积上安装越来越多的晶体管。但是在过去的几十年里，这种趋势惊人地一致，产生了许多连锁反应。随着计算机变得越来越快，与它们相关的一切也变得越来越快，垃圾抽屉往往会很快装满各种计算机外围设备和部件，这些设备和部件可能工作得很好，但就是跟不上速度。[Bonsembiante]有一个旧的 ADSL 路由器，由于时代的变化，它已经过时了，[但是他没有扔掉它，而是把它变成了一个吉他效果踏板](https://bonsembiante.hashnode.dev/how-to-connect-a-guitar-to-an-adsl-router)。

这种构建背后的原则是路由器本质上是一台 Linux 机器，完全支持 ALSA。当然，这意味着刷新自定义固件，这不是最简单的任务，但一旦设备添加了声音支持，它就能够与 USB 声卡接口。创建了一个额外的 C++程序来处理从吉他和声卡接收的实际音频。对于这个演示，[Bonsembiante]编写了一个环形缓冲区，并将其反馈到输出中以实现回声效果，但可以设想任何效果或许多效果都可以被编程。

对于任何寻找路由器正在执行的信号处理的源代码的人来说，它被列在单独的 GitHub 页面上。但是，如果你的零件箱里没有这种特定型号的路由器，有[更容易获得的 Linux 机器](https://hackaday.com/2017/09/12/pedal-pi-simple-programmable-guitar-pedal/)可以代替完成这项工作。

 [https://www.youtube.com/embed/tY-h0w9j89o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/tY-h0w9j89o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

