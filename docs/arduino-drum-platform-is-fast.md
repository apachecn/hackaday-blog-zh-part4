# Arduino 鼓平台很快

> 原文：<https://hackaday.com/2022/06/28/arduino-drum-platform-is-fast/>

鼓是一种令人兴奋的学习乐器，但如果有室友或邻居参与，通常会被禁止。对于这个问题，仍然有电子鼓可以更安静地演奏，但问题变成了价格问题。为了解决至少一部分问题，[Jeremy]转向使用 Arduino 自行构建鼓模块，但他仍然必须解决第三个问题:如何让 Arduino 足够快，让鼓听起来自然。

在现实生活中播放音乐需要精确的时间，所以选择 C++作为语言会带来一些问题，因为它通常不如低级语言快。尽管它更容易使用，但[Jeremy]在一系列详细介绍他的架子鼓设计的博客文章中详细解释了这一点。他选择使用的特定 Arduino 上的硬件弥补了软件定时的一些解决方案，包括偶数系统、快速 EEPROM、硬件定时器和每秒可采样 150k 样本的 ADC。

也就是说，硬件并不是这个版本中唯一突出的东西。[Jeremy]已经在他的 GitHub 页面上为那些对这个版本感兴趣的人发布了源代码，并计划在不久的将来发布更多关于架子鼓版本的博文。然而，这并不是通向电子鼓的唯一道路，正如我们所看到的，这种构建[将模拟架子鼓转换成数字架子鼓](https://hackaday.com/2020/07/08/your-own-electronic-drum-kit/)。

 [https://www.youtube.com/embed/q5b9FrB0W1Y?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/q5b9FrB0W1Y?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

