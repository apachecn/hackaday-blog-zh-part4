# 《与克里斯蒂娜一起跳舞》:转变发生的地方

> 原文：<https://hackaday.com/2021/09/28/keebin-with-kristina-the-one-where-shift-happens/>

对我个人来说，这几周在 clacking front 是令人兴奋的。我得到了几个新的键盘，包括我的第一个 ALPS 开关，一个旧的 TI/99A 键盘，双叶 MD 开关，以及几个应该是原来的樱桃开关(哦，天啊，它们真好听！)关于我与键盘相关的偶然，已经说得够多了，还有黑客攻击和噼啪声！

## 把我的踏板放在金属上

[![Kinesis Savant Elite triple foot pedal. It's a keyboard for your feet!](img/c80981ce951554e9e93a322222358096.png)](https://hackaday.com/wp-content/uploads/2021/09/pedal-all-closed-up.jpg) 我从善意中拿起了这个身能学者精英的三重脚踏板。它运行良好，但我不喜欢它的编程方式——左箭头、右箭头和鼠标右键。我很容易就在 Kinesis 网站上找到了手册和驱动程序，但我很快了解到，你需要一台 32 位的计算机来编程。句号。看，Kinesis 从未为原始的 Savant Elite 踏板编写过更新的驱动程序，他们只是推出了一个新的驱动程序，人们必须再支付 200 美元或想出其他办法。

我刚用完 32 位计算机，所以我试着像手册上说的那样在 XP 兼容模式下运行这个程序，但它就是不工作。哦，手册上说如果你做的不对，你可以用砖头砸它，所以这很奇怪也很可怕。大约就在这个时候，我开始意识到打开它并把控制器换成更现代的东西是多么容易。一旦我进去，我看到所有三个开关使用 JST 插头和直角头。然后我想，为什么不重复使用这个装置呢？我可能要做一个新的板，但是把这些踏板的 jst 插到我自己的板上会有多棒？

[![](img/15d47e15a8b724188edd8eb96af2e485.png)](https://hackaday.com/2021/09/28/keebin-with-kristina-the-one-where-shift-happens/binary-comment-25/)

This is the original controller.

[![](img/ee96e2dbb999a6fce1398562595831f3.png)](https://hackaday.com/2021/09/28/keebin-with-kristina-the-one-where-shift-happens/binary-comment-28/)

I had GPIO/GND pairs to spare.

[![](img/8ecf7c69485ef9a70802d5f4f220da55.png)](https://hackaday.com/2021/09/28/keebin-with-kristina-the-one-where-shift-happens/binary-comment-27/)

Let’s see if I can cram it all in there!

但是，我不需要做一个新的板子！事实证明，Raspberry Pi Pico 有足够多的 GPIO 引脚和分布式接地引脚，我能够从 Kinesis 控制器上拆下接头，并将所有三组都贴在 Pico 的一侧。我差点没把盖子拧回外壳上，但这是值得的。

这套踏板比我的全塑换挡踏板高出一大截。它是由钢制成的，踏板绝对足够结实，可以穿着鞋使用，尽管我更喜欢穿着袜子打字员。到目前为止，我喜欢它。我已经习惯于使用踏板来换档，所以我将它分配给中间的踏板作为参考点。左踏板做 Ctrl，右踏板做 Alt。我唯一的抱怨是开关不是咔嗒响的，所以我没有得到我习惯的那种好的听觉反馈。我会考虑把它们换掉，可能会换成一些重的按键开关，比如樱桃红。如果不四处摸摸作为参考，很难区分踏板，所以我用一个粘性毛毡家具圈作为临时的归位装置，同时我想出一些更酷的东西来使用，比如半个弹力球什么的。

## 看看这个:键帽游乐场

作为[riskable]寻求建立一个完全 3D 打印键盘的一部分，他们在 OpenSCAD 中制作了一个键帽游乐场，这真的更类似于那些有卡丁车、迷你高尔夫球和保龄球的大型娱乐设施。但是，你知道，为了键帽的乐趣。你想让你的帽子看起来像一个破碎的手风琴风箱吗？当然可以。(你能想象在你思考下一行的时候拨弄那些键帽会有多有趣吗？)

这个游乐场很大，现在对公众开放。你可以在下面的演示视频中看到它是多么强大，可以定制从盘子到圆角到图例的所有东西。目前，它处理 DSA 和 DCA 档案，但[riskable]表示，制作新档案相当容易。如果你认为这很酷，[看看【riskable】的 3D 打印磁控开关](https://hackaday.com/2021/08/02/mag-lev-switches-are-the-future-of-clacking/)，它们将被放在这些独特的键帽下面。

 [https://www.youtube.com/embed/WDlRZMvisA4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/WDlRZMvisA4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



## 未来热点:转变发生作者:马辛维查里

[![](img/5b54764e0393db15739ff41221db41b6.png)](https://hackaday.com/wp-content/uploads/2021/09/marcin-wichary-shift-happens.jpeg)

Image via [Medium](https://mwichary.medium.com/shift-happens-5b049f5a93a8)

我一直想告诉你关于这本即将出版的书的事情，尽管这本书要到 2022 年才出版，但我觉得再等下去没有意义。

当我在研究奥古斯特·德沃夏克和寻找图片的时候，我看到了一条有用的推文，作者是旧金山的一名印刷工人，他正在撰写一本关于键盘(包括打字机)完整历史的书。

在过去的 18 个月里，我一直从[Marcin]的[低频邮件列表](https://www.getrevue.co/profile/shift-happens/)中获得关于这本书的定期更新。不仅仅是更新，每一个都提供了一个有趣的教训，从 [skeuomorphs](https://www.getrevue.co/profile/shift-happens/issues/a-tale-of-three-skeuomorphs-242308) 到 [moire lines](https://www.getrevue.co/profile/shift-happens/issues/moire-no-more-688319) ，因为它们与打印照片有关。如果更新是任何迹象，这将是美味的全面和充满梦幻般的照片。我迫不及待地想得到这本书！

## 历史的噼啪声:Nocoblick 音乐打字机

[![](img/ae68748d6d543dba0a2720eafefccee9.png)](https://hackaday.com/wp-content/uploads/2021/09/nocoblick-music-typewriter-1.jpg)

Image via [Music Printing History](https://musicprintinghistory.org/nocoblick/)

这不是第一台音乐打字机，但它是早期的一台。Nocoblick 音乐打字机产于德国科隆，在 1910 年至 1917 年间一直在使用。

这台机器的有趣之处在于，压盘的位置是由一个刻度决定的，这有助于准确放置纸币和符号。起初，机器使用预先印有五线谱的纸张，但后来的版本也设计了五线谱。

Nocoblicks 使用了一种由雷明顿的竞争对手乔治·布利肯斯德弗设计的可互换的类型轮——一个用于音符，另一个用于字母。只需简单地改变打字轮和轻弹控制杆，它也可以打印歌词。由于某种原因，Nocoblick 卖得不好，当 Blickensderfer 在 1917 年去世时，他的 type wheel 停产，[有效地杀死了任何使用它的机器](https://site.xavier.edu/polt/typewriters/nocoblick.html)。

## 向巨大的 F 键致敬

[![A giant, 3D-printed key switch that sends F to pay respects.](img/bca94923ca9c5230c79661f0c1846f12.png)](https://hackaday.com/wp-content/uploads/2021/09/giant-F-key-bv.jpg) 这个坏小子一发帖就蹿升 r/all 榜首，[我们不得不尽快把我们的镜头给你](https://hackaday.com/2021/09/01/big-f-key-to-pay-big-respects/)。它不会发出刮擦声和咔嗒声，但也超级棒。

[Jaryd]甚至用一个钻头和一个 3D 打印的圆柱体为这只野兽做了他们自己的弹簧。但是最好的部分是它的工作方式:通过启动一个连接到 Arduino 的普通大小的按键开关。

* * *

有关于键盘的热门提示吗？通过发送一两个链接来帮助我。不想让所有的黑客抄写员看到它？欢迎[直接给我发邮件](mailto:kristinapanos@hackaday.com?Subject=[Keebin' Fodder])。