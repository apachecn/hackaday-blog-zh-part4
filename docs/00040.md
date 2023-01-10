# 少年帽控制游戏

> 原文：<https://hackaday.com/2018/07/17/teensy-hat-controls-games/>

[卡森]不知道如何使用加速度计，直到他把一个连接到一个十几岁的孩子，并把它放在一顶帽子里。其结果是[一个操纵杆](https://www.youtube.com/watch?v=nT4XKmwGZDc)，如果你长时间玩视频游戏，可能会导致你的颈部问题。你可以在下面的视频中看到这个设备是如何产生的以及它是如何工作的。

我们喜欢在与帽子集成之前构建电路并进行测试的方法。他用一个小试验板，上面挂着一半的小针脚。这似乎是可行的，尽管我们担心短路或浮动引脚会引起问题。当然，如果用上拉电阻驱动断开的引脚作为输出或输入，这可能没什么大不了的。

很多视频更侧重于一些特定游戏的自定义控制器的设置，但它似乎工作得很好。我们不禁羡慕那些可以毫不费力地移动脖子的人。

老实说，这个控制器看起来不太实用，尽管在视频的结尾，他确实在使用方面有所提高。这是一种用加速度计进行实验的有趣方式，然而，如果加上电池和一些无线通信，这样就不会拖着电缆了。

代码[可通过 Pastebin](https://pastebin.com/4QyhrMgv) 获得。最大的收获是需要设计一个死区，这样微小的动作就不会变成控制输入。

如果你对这些加速度计的工作原理更感兴趣——这很有意思——[Bill Hammack]有[的视频。如果你不喜欢移动你的头，你也可以用同样的方法控制](https://www.youtube.com/watch?v=KZVgKu6v808)[和](https://hackaday.com/2015/08/16/hand-controlled-robot-uses-accelerometer/)。

 [https://www.youtube.com/embed/nT4XKmwGZDc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/nT4XKmwGZDc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

