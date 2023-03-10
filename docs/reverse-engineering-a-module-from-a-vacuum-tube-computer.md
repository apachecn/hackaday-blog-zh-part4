# 对真空管计算机的模块进行逆向工程

> 原文：<https://hackaday.com/2020/09/10/reverse-engineering-a-module-from-a-vacuum-tube-computer/>

最好先承认，真空管可能会让一些年轻一代的工程师感到困惑。是的，我们知道如何用栅极控制从阴极到阳极的电子流，以及如何用它来放大和控制电流。但是，在查看电子管电路的原理图时，仍有一些东西并不总是一目了然。也许我们只是在错误的时间长大。

一个显然还没有老到能够驾驭第一波电子学浪潮，但似乎仍然掌握了热离子发射概念的人是[天兔电气]，他一直在做一些伟大的工作，从旧的真空管计算机中逆向工程模块。下面的视频重点介绍了 IBM 650 的双管可插拔模块，这款机器的历史可以追溯到 1954 年。易贝的发现只不过是两个管座和一对电阻器，用一个金属环连接到一个插头上。在几乎一无所获的情况下，[天兔]仍然能够找出插座中会有什么样的电子管——九针插座是一个很大的线索——并确定该模块很可能是一个双与非门。为了测试他的理论，[天兔]对 IBM 使用的原始电压做了一些改动，制造了一个突破性的 PCB。这是一种有趣的技术组合，但他能够遍历真值表，并确认他的模块是一个双与非门。

视频有点长，但它充满了珍闻，真正有助于澄清如何管工作。在这篇关于三极管如何工作的文章的帮助下，你将踏上热离子启蒙之路。

 [https://www.youtube.com/embed/e6OqUsPVWHc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/e6OqUsPVWHc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

