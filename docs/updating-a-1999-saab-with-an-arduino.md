# 用 Arduino 更新 1999 年的 Saab

> 原文：<https://hackaday.com/2018/08/11/updating-a-1999-saab-with-an-arduino/>

除非你的车是新买的，否则你可能有过这样的经历:驾驶一辆新车，看到一些特性或功能，会引发一点嫉妒。这可能不足以让你跑出去为自己申请一笔新车贷款(这正是制造商所希望的)，但这绝对是你希望你的旧车型拥有的东西。但能报复又何必嫉妒呢？

[![](img/11573faf4dba31fa6519821f06b93068.png)](https://hackaday.com/wp-content/uploads/2018/08/saab_detail.jpg) 【萨博曼】希望他的 1999 款萨博 9-5 能有这样的功能:快速轻敲转向信号杆会触发指示灯闪烁三次。意识到这是一个电子问题，他想出了一个办法，通过在汽车的骰子模块中添加 Arduino Pro Micro，在他的萨博中改装这个功能[。](https://hackaday.io/project/158595-3-blink-modification-for-saab-9-5)

DICE(代表仪表板集成中央电子设备)模块控制车辆中的许多附件，如照明和雨刷。在闪光灯的情况下，它读取信号杆开关的状态，并根据需要打开和关闭闪光灯。在拨弄了一下骰子板后，[Saabman]发现了他正在寻找的 74HC151 多路复用器芯片:可以从引脚 1 和 2 读取闪光灯开关的状态，他甚至可以从引脚 16 为 Arduino 提供 5 V 电压。

在试验板上制作出电路原型后，[Saabman]用双面胶将 Pro Micro 贴在 74HC151 的顶部，并开始完善该项目的软件部分。Arduino 读取转向信号开关的状态，如果它们瞬间打开，它会将引脚从输入变为输出，并在三秒钟内保持高电平。这使得 DICE 模块认为驾驶员正握着转向杆，并将保持闪光灯工作。解决问题的一种非常优雅且不引人注目的方式。

黑客对车库并不完全陌生；从印刷难找到的零件到移植其他汽车制造商的 T2 最喜欢的功能，萨博的这种巧妙的改进有很多好公司。

 [https://www.youtube.com/embed/FzAu63haHRA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/FzAu63haHRA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

