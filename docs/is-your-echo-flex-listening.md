# 你的 Echo Flex 在听吗？

> 原文：<https://hackaday.com/2021/01/14/is-your-echo-flex-listening/>

我们总是很惊讶，亚马逊或谷歌没有聘请电视节目主持人凯尔塞·格拉玛作为他们智能家居设备的代言人。毕竟，他的口头禅是，“我在听……”也许他们不想提醒你，从理论上讲，该设备可能会将你说的一切发送给他们或邪恶的黑客或政府机构。当然，有一个静音按钮，它会点亮一个红色的 LED。

但是如果你真的有妄想症，那还不够。毕竟，同样想偷听你的人会很乐意去假闯红灯。【Electronupdate】也有同样的想法，决定来回答这个问题:[静音键真的会让你的麦克风静音吗？](https://electronupdate.blogspot.com/2021/01/amazon-echo-flex-microphone-mute-real.html)答案不仅需要一些案例打开和分析，甚至还有一些 IC 解封。

我们对分析的深度印象深刻。微小的 SMD 部件被标上令人困惑的标记，如果你真的有妄想症，你无论如何也不会相信它们。但是看看实际的电路芯片就很清楚了。问题中的零件原来是一个施密特触发器、一个触发器和一个与非门。

最后似乎是麦克风没电了红色静音灯就亮了。所以看起来静音键是真的。这些评论已经在推测间谍甚至可以在红灯亮着的情况下监听——或者至少出现在红灯上——的方式，但还不清楚这是否真的可能。

拆掉[家务助理](https://hackaday.com/2018/07/12/teardown-of-sonos-and-amazon-smart-speakers-reveals-interesting-engineering-details/)是家常便饭。如果你认为这样的设备不能被合作，[再想想](https://hackaday.com/2017/08/03/the-amazon-echo-as-a-listening-device/)。

 [https://www.youtube.com/embed/yfBNql0-k_s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/yfBNql0-k_s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

