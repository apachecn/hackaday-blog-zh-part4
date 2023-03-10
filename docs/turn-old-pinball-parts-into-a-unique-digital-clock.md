# 将旧弹球零件变成独一无二的数字时钟

> 原文：<https://hackaday.com/2018/12/13/turn-old-pinball-parts-into-a-unique-digital-clock/>

打造一个真正独一无二的数字钟变得越来越难了。从电子显示器到翻转点和翻转卡，所有的东西似乎都做得太死了。但是这个[弹球得分卷轴时钟](https://www.elektormagazine.com/labs/pinball-clock-180307-1)设法保持独特的时钟球在比赛中，可以说。

还不完全清楚这种构建应该归功于谁，但这篇文章是由[Lucky]写的。他们也没有提到哪台弹球机放弃了它的机电计分显示器。我们的猜测是一台 60 年代的机器，在分数膨胀时代之前，它需要的不仅仅是四位数。实际上，显示器的驱动器被设计成使得可以使用来自机电时代的任何弹球机的得分单元。ESP8266 在 RTC 的帮助下保持时间，并通过一组 MOSFETs 驱动计分单元的线圈。下面的视频显示，它不会成为床头柜上的一个伟大的时钟；令人欣慰的是，它有一个用户配置的安静时间，以限制清醒时的噪音。它还每半小时闪烁一次日期，响螺线管操作的钟声，作为奖励，它可以用来在软件中内置的弹球游戏中记分。

我们喜欢用这样的时钟来纪念老式弹球机。我们已经看到了用一台旧机器的后玻璃制成的单词钟，还有用四个玩家的后玻璃显示日期和闹钟时间的 T2。

 [https://www.youtube.com/embed/lQL2Vk1Hj-o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/lQL2Vk1Hj-o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[Emma Lovelace]的提示。