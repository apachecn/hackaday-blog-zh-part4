# 快速且(不太)脏的负电压电源

> 原文：<https://hackaday.com/2021/11/16/quick-and-not-very-dirty-negative-voltage-supply/>

在每个硬件黑客的职业生涯中，都会有一段时间，他们第一次意识到他们的项目需要一个负电压轨。意识到这一点后，通常大约 10 毫秒后，他们会接触到电子技术，试图弄清楚如何在设计中引入零下电压。事实证明，有很多方法可以完成这项工作，从昂贵的电源到你可以设计的花哨的调节器，但如果你很懒(像我一样)，你可能只是想要一个简单的、近乎嵌入式的解决方案。

[菲利普·皮奥尔斯基]在那里掩护你。在最近的一个视频中，[他演示了如何将 Ebay 上的一个“中国特供”1 美元的降压转换器变成一个升压-降压转换器](https://www.youtube.com/watch?v=r49BwY0eFPA)，能够充当负电压电源。他意识到，通过交换调节器的输入和输出，你可以从根本上逆转产生的电势。当然，有一些注意事项，包括高启动电流和有限的最大值。电压，但他设法绕过其中一些与一点聪明的重新布线和一点博奇工作。

当然，如果你对电源有严格的要求，你可能想花钱买一个专业制造的，或者自己设计一个满足你确切需求的。对于我们大多数人来说，像这样快速简单的解决方案就能完成工作，让我们专注于设计的其他方面，而不必花太多时间担心电源。当然，[如果电力电子设计*是*的事，我们也能帮你搞定](https://hackaday.com/2020/04/25/in-depth-design-of-a-flyback-converter/)。

 [https://www.youtube.com/embed/r49BwY0eFPA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/r49BwY0eFPA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[Bornach]的提示！