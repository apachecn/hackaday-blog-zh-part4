# 黑客乘法:纸上二进制乘法

> 原文：<https://hackaday.com/2020/02/07/hacking-multiplication-binary-multiply-on-paper/>

我们经常注意到，无论古人是否知道二进制，我们都可以用手指数到 1023。我们在观看[Numberphile]关于[“俄罗斯”乘法](https://www.youtube.com/watch?v=HJ_PP5rqLg0)的最新视频时想到了这一点(见下文)。显然，这种方法可以追溯到很久以前，有时被称为埃塞俄比亚或农民乘法。甚至古埃及人也做了一种。

如果你曾经为微控制器写过很长的乘法代码，你可能知道它是如何工作的。数字每减半就等于右移一次。每次加倍都是左移。丢弃偶数意味着只取最低有效位为零时的值。[布斯的算法](https://en.wikipedia.org/wiki/Booth%27s_multiplication_algorithm)效率更高，但是“俄罗斯”的方法在纸上做起来很简单。

俄罗斯方法和埃及方法的主要区别在于，你是从被乘数之一(俄罗斯)开始，还是从 1 开始，一路向上(埃及)。不管怎样，你应该从最小的被乘数开始。

例如，假设你有 321 x 17。你会选择 17，因为它比较小，然后把它分成两半，形成你桌子的左边。扔掉任何一半，因为那些是从右边移出的位。表格的右侧从另一个数字(321)开始，每行加倍。所以:

```
17     321
 8     642
 4    1284
 2    2568
 1    5136
```

8、4 和 2 的行是偶数，因此它们代表长乘法中的零乘。你可以把它们划掉。剩下一排是 17 和 1。把这些加起来，你得到 5457，正确答案。

如果你想看二进制的例子，考虑 9×3，我们知道它是 27，使用俄罗斯的方法得出 9+18。在二进制中，我们会说:

```
    1001
x   0011
-----------
 000000
  000000
   10010 (18)
    1001  (9)
-------------
 0011011 (27)
```

奇怪的是，这只是埃及人知道如何计算的一种方法。直到 2002 年，人们才完全理解了他们处理分数的一些方法。

这是一个很好的例子，说明了死记硬背的方法是如何起作用的，即使你不明白为什么会这样，但是如果你明白了就更好了。当然，这年头，我们可以只[问一台电脑](https://hackaday.com/2019/05/11/mathics-how-to-do-hard-math-when-youre-not-an-mit-janitor/)。

 [https://www.youtube.com/embed/HJ_PP5rqLg0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/HJ_PP5rqLg0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



m