# 宇宙中最重要的设备是由一个 555 定时器驱动的

> 原文：<https://hackaday.com/2021/09/23/the-most-important-device-in-the-universe-is-powered-by-a-555-timer/>

Hackaday 评论区因为一个重复出现的主题而变得臭名昭著，这个主题类似于“*我不知道他们为什么用 Arduino，他们可以用 555 定时器来做这件事！*“如果你曾经有过同样的想法，那么这篇文章就是为你而写的！

那么，宇宙中最重要的设备是什么？这是现代道具#195-290-1，最初建于 20 世纪 70 年代的电影道具。它是[John Zabrucky]创造性思维的产物，他在 1977 年创建了现代道具，为科幻电视和电影制作服务，希望用他们的道具发明未来。现代道具公司的产品以其高质量和无可挑剔的工艺而闻名，直到[关门以便【约翰】退休的那一天](https://www.latimes.com/entertainment-arts/business/story/2020-01-03/modern-props-closes-its-doors)之前一直都很抢手。

这种特殊的设备被称为宇宙中最重要的设备，因为它在现代产品中无处不在，我们都听说过:几部*星际迷航*特许经营，*最后的星际战士*，*霹雳游侠*，*飞机 II* ，*奥斯丁力量*，以及无数其他产品。下次你坐下来看科幻电影时，看看你是否能发现它！请务必查看休息时间下方的视频，了解几个示例。

没有人知道最重要的设备是做什么的，除了它有来回闪烁的红灯。多亏了安装电子设备的人(吉恩·特恩博)的评论，我们才知道它是如何供电的。[Gene]解释说 45w NPN 功率晶体管通过升压变压器驱动氖管。晶体管本身连接到 74C4514 解复用器，解复用器本身由 7493 二进制计数器驱动。7493 是靠什么驱动的？你猜对了:古老的 555 定时器。因此，555 计时器运行着宇宙中最重要的设备。

我们确实认为[Gene]的最后评论更能说明自道具最初制作以来发生了多大的变化。在解释了这个设备之后，他说“现在我们只需要用一个 Arduino 来做同样的工作。”确实如此。

别急，555 爱好者。我们已经用这个[真空管 555](https://hackaday.com/2021/03/28/should-have-used-a-vacuum-tube-555/) 给你盖上了，还有 [Trollduino，一个 Arduino 护盾上的 555](https://hackaday.com/2021/01/17/arduino-wannabe-should-have-used-a-555-oh-wait-it-does/)。感谢[马特 K]的伟大提示。别忘了将你最喜欢的黑客技术提交到我们的[举报热线](https://hackaday.com/submit-a-tip/)！

 [https://www.youtube.com/embed/phPp5oYnps0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/phPp5oYnps0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

