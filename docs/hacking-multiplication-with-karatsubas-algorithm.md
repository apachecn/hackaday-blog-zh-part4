# 用 Karatsuba 算法实现黑客乘法

> 原文：<https://hackaday.com/2021/11/16/hacking-multiplication-with-karatsubas-algorithm/>

人们倾向于痴迷于让计算机软件更快。当然，你可以提高时钟速度，增加更多的处理器，但通常提高速度的最有效方法是找到更好的方法。有时，这些方法与人类完成相同任务的方法非常不同，但它适合计算机的能力。[Nemean]有一个视频解释了一个更好的乘法算法，称为 [Karatsuba 的算法](https://www.youtube.com/watch?v=cCKOl5li6YM)，它实际上非常聪明。你可以看下面的视频。

为了帮助您理解算法，视频展示了一个简单的两位数乘两位数乘法。你可以看到第一个和最后一个数字本质上是一个乘法的结果。所有的中间数字加在一起。唯一可能改变第一位数字的是进位。

使用巧妙的数学，您可以计算第一个和最后一个数字，以及包含第一个和最后一个数字的中间部分的总和。通过减去它们，你可以用比传统方法更少的乘法运算得到所有需要的数字。加法和减法通常很便宜，所以用乘法来交换它们可以节省大量时间。

当然，这些天你的乘法可能发生在硬件中，但它可能仍然没有加法和减法快。然而，这种算法的复杂性意味着除非你要处理非常大的数字，否则不经常使用。无论哪种方式，这都是数学的巧妙应用，并推翻了“每个人”都知道的事实——最佳方法已经被发现。这让你想知道未来还有多少其他已知的东西会被证伪。

我们总是对奇怪的数学方法感兴趣。其中一些[相当多彩](https://hackaday.com/2016/01/25/bone-up-on-your-multiplication-skills/)。

 [https://www.youtube.com/embed/cCKOl5li6YM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/cCKOl5li6YM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

