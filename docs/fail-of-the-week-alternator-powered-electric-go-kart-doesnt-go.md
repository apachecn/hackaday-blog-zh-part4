# 本周失败:交流发电机驱动的电动卡丁车不走了

> 原文：<https://hackaday.com/2021/10/25/fail-of-the-week-alternator-powered-electric-go-kart-doesnt-go/>

给一个爱开快车但不喜欢大声喧哗的六岁小孩送什么？[当然是把燃气卡丁车改装成电动](https://www.youtube.com/watch?v=HpmVXWBJjrc)！(视频，嵌在下面。)这个目标让[罗伯特·邓恩]的老化车轮朝着卡丁车的方向走了很长一段路，卡丁车几乎可以，但不太……管用。

如果你看过罗伯特的任何视频，你就会知道他不会走捷径。这个人毕竟拥有一只特拉班和信赖罗宾。他没有购买电池组，而是用单独的 LiFePO4 电池制作了自己的 5S24P 电池组。这些电池通常是点焊的，所以[罗伯特]制造了一台 Arduino 控制的传家宝级点焊机。现在，虽然焊机可以处理薄镍条，但它不能完成焊接大电流镀镍铜的任务。当解决方案的尝试失败后，[罗伯特]建立了一个夹紧铜母线系统来处理电池的高电流连接。

如果电池不够硬，[Robert]还决定不在这个项目中使用现成的电机。他将汽车交流发电机改造成无刷电机。在之前，我们已经[介绍过使用这种转换的项目。我们自己的](https://hackaday.com/2016/08/14/alternator-becomes-motor-for-this-electric-go-kart/)[【珍妮榜】甚至写了一个关于它的教程](https://hackaday.com/2020/01/16/car-alternators-make-great-electric-motors-heres-how/)。[Robert]不幸的是他的体型有很多问题。

在第一个视频中，[Robert]使用一个普通的无名电机控制器，并尝试无传感器运行电机。像他之前的其他人一样，他发现电机在工作台上运行良好，但在负载下无法启动。给卡丁车一个滚动启动，它就会跑起来。这是无传感器电机的常见问题，电机控制器使用无动力线圈作为传感器，有时在低速/高扭矩情况下启动电机会有困难。解决方案是在电机上增加霍尔效应传感器。[罗伯特]做了所有这些，测试了霍尔效应和线圈布线的所有 36 种组合，它仍然不起作用。

快进到[Robert]关于这个项目的第二个视频。他换了一个更好的电机控制器，造了一个好看的电池盒(两次)，然后把所有东西都装回去。发动机在工作台上表现很好，启动起来也很好。但每当卡丁车踩下一半油门时，电机控制器就会以“霍尔传感器错误”为由停止工作。

看起来[Robert]建造他的马达是正确的——霍尔传感器安装在线圈中间[,很像[austiwawa]在他的电动自行车建造中发现的](https://hackaday.com/2021/01/24/an-alternator-powered-electric-bicycle-gives-rotor-magnetic-field-insight/)。虽然没有出现在 YouTube 视频中，[罗伯特]甚至试图隔离和屏蔽他的大厅电线，但什么也没有改变。在这一点上，[罗伯特]从这个项目后退了几个星期，或者至少直到他六岁的儿子说服他修理它。

我们不得不称赞[罗伯特]不仅报道了他的成功，也报道了他的失败。卡丁车和点焊机都是伟大工艺的例子。我们确信，再多做一点修补，他就会让他的交流发电机转换马达工作起来。知道问题出在哪里吗？请在评论中告诉我们！

 [https://www.youtube.com/embed/HpmVXWBJjrc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/HpmVXWBJjrc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/3Cq4mGpZnV8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/3Cq4mGpZnV8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

