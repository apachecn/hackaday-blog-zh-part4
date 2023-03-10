# 秘密敲门打开门

> 原文：<https://hackaday.com/2020/05/25/secret-knock-unlocks-door/>

看任何一部关于禁酒令的电影，你可能会看到角色通过秘密敲门进入地下酒吧。在老电影里，一个小滑门会打开，这样门卫可以检查你，让你进去。有了【伊斯迈尔森的】电子锁，暗号[自动开门](https://github.com/IsmailSan/Secret-Knock-Detecting-Door-Lock)。你可以在下面的视频中看到它是如何工作的。

(编者注:Grrr…GitHub repo 在写作和出版之间被拉了出来。如果你对爆震检测器感兴趣，去看看下面一段的链接。)

该设备使用压电扬声器来检测爆震。扬声器是一种换能器，像许多换能器一样，在某种程度上，它可以在两个方向上工作。一个伺服电机控制着锁舌。一个 Arduino 操纵着一切。

代码相对简单。它保存了一组敲击之间的预计延迟，并将它听到的与这些延迟进行比较。如果你完成了这个程序，门就会打开。如果我们锁定该国的黄金供应，我们可能会增加一些额外的安全措施，但对于一把轻型锁来说，应该没问题。

电路也很简单。有一个模拟输入连接到一个电阻和传感器。Arduino 完全能够直接驱动小型伺服系统。加个电池就搞定了。

我们已经有一段时间没有在这里看到敲锁了，但它们曾经风靡一时。这里有一个[好看简单的](https://hackaday.com/2009/11/04/knock-detecting-lock/)，一个[用逻辑芯片](https://hackaday.com/2011/08/30/knock-lock-with-logic-chips/)，当然还有一个[用 555s](https://www.electrobob.com/secret-knock-detector-with-555/) 打造的。如果敲门不是你的风格，尝试用按钮或[甚至电容传感器](https://hackaday.com/2012/08/06/knock-lock-balks-knock-uses-capsense-without-shock/)代替压电。不能敲！

 [https://www.youtube.com/embed/nlROXX6Bug8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/nlROXX6Bug8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

