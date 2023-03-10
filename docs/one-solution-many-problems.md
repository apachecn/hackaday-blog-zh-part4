# 一个解决方案，许多问题

> 原文：<https://hackaday.com/2022/05/21/one-solution-many-problems/>

当你的一个问题有多个解决方案时，你可能认为你很幸运，你可以挑选，但是当一个解决方案有许多问题时，你更幸运！本周，我在一个新的地方偶然发现了一个旧的解决方案。这个项目是[一个奇妙的老式 MIDI 吉他制作](http://tryndelka.narod.ru/fretstrn_e.htm)，由【Aleksandr Goltsov】制作的 Tryndelka。旧的解决方案呢？开关矩阵二极管。

你看，[亚历山大]正在制作一把电吉他，琴弦被拉到一定的电压，然后与金属品接触。每个品被切成六块，这样琴弦就可以单独读出，微控制器连续扫描每根琴弦，测试它是否被按下。完成了，对吗？不对！当同时按下两个或更多的弦时，问题就来了——你想要的弦的电路径将穿过你没有扫描的弦上的闭合开关。解决方案是大量的二极管。

在我们要把它带到 Shmoocon 的前一天晚上，大约凌晨 3 点，我在连线一个 MAME 橱柜的过程中艰难地发现了这个问题。我们终于让整个 USB/button 代码正常工作了，所以我们玩了几轮街头霸王以示庆祝。我们最终注意到，按下一个按钮，甚至向特定方向移动操纵杆，都会阻止其他一些按钮工作，或者完全改变它们的功能。后来在网上快速搜索，我们手工焊接了 64 个二极管直到天亮。美好时光！

但是开关矩阵需要二极管的事实，以及确切的原因，永远铭刻在我的脑海里。看到它在各种背景下出现是很有趣的，从 DIY 键盘到 MIDI 吉他，再到 [Charliplexing](https://en.wikipedia.org/wiki/Charlieplexing) 。(是 LED 里的“D”！)是经典之一——解决了很多问题。

This article is part of the Hackaday.com newsletter, delivered every seven days for each of the last 200+ weeks. It also includes our favorite articles from the last seven days that you can see on [the web version of the newsletter](https://mailchi.mp/hackaday.com/hackaday-newsletter-649368). Want this type of article to hit your inbox every Friday morning? [You should sign up](http://eepurl.com/gTMxQf)!