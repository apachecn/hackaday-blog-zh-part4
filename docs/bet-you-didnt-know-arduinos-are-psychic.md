# 我打赌你不知道 Arduinos 是灵媒

> 原文：<https://hackaday.com/2020/11/24/bet-you-didnt-know-arduinos-are-psychic/>

你已经没有娱乐自己和家人的方法了吗？如果你已经读完了所有的书，看完了所有的电影，那么是时候探索硅的精神能力了。[Hari Wiguna]有办法让他们猜很长时间。

这个技巧不需要太多，只需要几个 Arduinos，一些瞬时按钮，一个数字键盘和大量的数学帮助。正如你在休息后的演示中看到的，这两者之间没有任何联系，甚至没有 802.11(n)。在随机发生器 Arduino 上，[Hari]按下一个按钮就产生随机数，直到观众看到他们喜欢的一个。然后[Hari]用另一个按钮锁定号码。

接下来发生的事情很关键:随机发生器生成另一个随机数，但用它作为设置一个标记数字的提示。随机数发生器 Arduino 从 9 中减去两位数中较大的一位，并将结果存储为标志。当下一个在正确位置有标志位的数字出现时，后面的数字将是开始时选择的随机数。

灵媒 Arduino 的秘密是它知道它收到的第一个猜测是特别的。它和随机数发生器做同样的数字计算，所以当猜测者用数字输入猜测时，它知道下一个输入的数字是赢家。清澈如泥？看看下面的第二个视频，在那里[Hari]解释了这个魔术，一个魔术经典的新版本。

寻找一个更刺激的方法来产生随机数？尝试使用[鱼缸](https://hackaday.com/2019/12/09/generating-random-numbers-with-a-fish-tank/)、[熔岩灯](https://hackaday.com/2018/01/04/the-grooviest-random-number-generator-ever/)，或者[来自外太空的μ介子](https://hackaday.com/2020/01/20/random-numbers-from-outer-space/)。

 [https://www.youtube.com/embed/gWtNpHCqAWY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/gWtNpHCqAWY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/dhbPKnjh50g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/dhbPKnjh50g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

