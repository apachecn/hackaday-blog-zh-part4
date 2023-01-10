# 那些组件测试人员是如何工作的？

> 原文：<https://hackaday.com/2019/10/01/how-do-those-component-testers-work/>

大多数人至少见过那些在中国网站上花 10 美元左右就能买到的廉价组件测试器。如果你以前没见过，他们通常有某种多针插座。你把一个元件放入插座，按下按钮，它就会识别出这个元件是什么，哪个引脚是哪个引脚，以及这个元件的价值。例如，您可以插入一个电阻、电容、电感、二极管或晶体管，并获得哪个引脚是哪个引脚的读数。这看起来很神奇，但是安德烈亚斯·斯皮斯研究了这一切是如何工作的，并在最近的一个视频中总结了他的发现。

[Andreas]甚至引用了我们之前关于这个话题的文章,并且，正如我们所做的，深入挖掘了这个被中国卖家一次又一次克隆的设备的原始开发者。尽管不同的版本有一些差异，但基本思想是相同的。AVR CPU 使用一些模拟和数字诡计来进行许多不同的测量。

通过研究测试人员如何用很少的外部组件完成工作，你可以学到很多编码技巧。去[原项目](https://www.mikrocontroller.net/articles/AVR_Transistortester#Introduction_.28English.29)也有帮助。小心点。你从易贝花 7 美元买来的测试器可能无法使用原始代码——一些制造商出于不同的显示或其他原因做了简单的修改。

我们已经看到这些被黑客攻击来做其他事情，尽管可能没有原来的有用。[也许更有趣](https://hackaday.com/2019/05/03/play-tetris-on-a-transistor-tester-because-why-not/)，但没那么有用。

 [https://www.youtube.com/embed/4Xsg8lpP75s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/4Xsg8lpP75s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

