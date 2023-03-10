# π皮波示波器

> 原文：<https://hackaday.com/2022/11/06/a-pi-pico-oscilloscope/>

示波器系列的预算端是所谓的袖珍示波器。大约一副纸牌大小，他们结合了一个微控制器和一个液晶显示屏，使仪器的带宽达到几十千赫，性能不太好。它们有点像玩具，但话说回来，如果所需要的只是一个简单的音频范围，它们在小包装中是一个可以接受的选择。现在[]jgpeiro]已经做出了一个比玩具套件领先几光年的产品，[使用了树莓 Pi Pico，100 MHz ADC，并努力设计一个更好的输入电路](https://hackaday.io/project/188051-rpscope)。

最简单地说，这可以是一个简单的运算放大器和 ADC 电路，为 Pico 供电，但它有多个精心设计的级来提供全带宽，增益、失调和触发设置由一系列 DAC 芯片在软件控制下设置。这一点和相当大的带宽使它成为一个更可行的示波器，我们希望看到它得到进一步发展。

相比之下，[我们来看看几年前的最佳比赛](https://hackaday.com/2018/08/06/review-a-20-mhz-pocket-scope-for-not-a-lot/)。