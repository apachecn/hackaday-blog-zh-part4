# 液晶显示器播放点击率

> 原文：<https://hackaday.com/2022/08/18/lcd-monitor-plays-the-hits/>

在过去，将 AM 收音机放在电脑或显示器附近，并故意造成干扰以产生粗糙的声音，这并不罕见。你错过了吗？不要！多亏了[luambfb],你现在可以用一个普通的液晶显示器来做同样的事情。您需要相关显示器的水平刷新率。

当然，做这件事没有学习它如何工作有趣。这种效果依赖于 LCD 在刷新一行时发出信号的事实。黑色行发射相对低的能量，而白色行发射更多的能量。灰度……好了，你明白了。

该软件接受一个输入文件，允许你创作自己的曲子。每分钟有固定的节拍数，一组音符和休止符编码在一个文本文件中。该项目借鉴了一个名为 [Tempest for Eliza](http://www.erikyyy.de/tempest/) 的老项目的想法，你可以在下面的视频中看到(在它的页面上也有这个项目的视频)。

当然，Tempest 来自于使用这些信号读取监视器上的数据的术语这是可能的，但很困难。虽然看起来这是一个现代问题，但[它的起源可以追溯到二战](https://hackaday.com/2015/10/19/tempest-a-tin-foil-hat-for-your-electronics-and-their-secrets/)。

 [https://www.youtube.com/embed/oLQbp6hj7-c?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/oLQbp6hj7-c?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

