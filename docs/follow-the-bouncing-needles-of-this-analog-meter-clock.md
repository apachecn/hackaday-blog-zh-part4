# 跟随这个模拟时钟跳动的指针

> 原文：<https://hackaday.com/2019/01/29/follow-the-bouncing-needles-of-this-analog-meter-clock/>

我们的社区似乎永远不会厌倦时钟建设。似乎有无限的方法来标记时间的流逝，寻找独特的方法来显示它是无穷无尽的魅力。

这个模拟伏特计时钟似乎真的受到了评论[r/DIY 线程](https://www.reddit.com/r/DIY/comments/akc9ft/i_made_a_clock_from_analogue_voltmeters/)的 Redditors 的欢迎，我们在那里第一次发现了它。[ElegantAlchemist]的设计非常简单——只是三个动圈式仪表和漂亮的工业外观挡板。电表连接的是 300 伏交流电，因此移除了整流器和平滑电容，用一个更适合项目所需的 0-5 伏直流电范围的串联电阻代替。在 Corel Draw 中，显示小时、分钟和秒的新表盘被迅速制作出来，所有东西都被放入一个坚固而多彩的铝制“踏脚盒”中，通常用于效果踏板。一个 Arduino Nano 和一个 RTC 以一个漂亮的、有弹性的动作驱动仪表。简单，造价低廉，而且很受欢迎。

观察力敏锐的读者会注意到它与我们不久前讨论过的时钟有相似之处。那个人选择了 3D 打印的外壳作为飞机仪表组的外观。我们喜欢[ElegantAlchemist]的备用表壳设计，但想知道这款钟放在精致的木质表壳中会是什么样子。