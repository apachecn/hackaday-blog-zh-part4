# 这个合成器演奏所有人都知道的唯一音阶

> 原文：<https://hackaday.com/2018/10/24/this-synth-plays-the-only-scale-everybody-knows/>

[randomprojectlab]正在为 Hackaday 奖制作一个围绕五声音阶的合成器。这是 Pentasynth，它基本上只是一个键盘，每个音阶有五个音符。

每种音乐形式都有一些共同点。几乎每一种音乐传统，从西方艺术音乐到印尼民间音乐都使用五声音阶。这只是一个没有四度和七度音阶的大调音阶，或者只是在钢琴上弹黑键。[这是一个人人皆知的音阶](https://www.ted.com/talks/bobby_mcferrin_hacks_your_brain_with_music)，也是音乐教育各流派的基础。在五声音阶上闲逛是所有酷家伙在吉他中心做的事情。这绝对是所有音乐的基础。

这个构建的硬件是 Adafruit Metro Mini，或者基本上是带有 ATMega328 的 Arduino。这会生成三个音频通道、两个方波(键盘和低音伴奏各一个)和一个伪随机噪声鼓点。按键是 3D 打印的，外壳是 CNC 的亚克力。

大多数教育音乐玩具都有一些额外的功能，让作曲变得更容易。Pentasynth 也不例外，它有一个添加鼓点的按钮，一个添加低音线的按钮，以及一个使键盘成为大调或小调的开关。这是一个伟大的想法，你可以看看下面的视频。

 [https://www.youtube.com/embed/5M7slJN6BCE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/5M7slJN6BCE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



The [HackadayPrize2018](https://hackaday.io/prize) is Sponsored by: [![Microchip](img/20eb9d92b47da4c15177567c02a65727.png)](https://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey)  [![Supplyframe](img/2d012d9fc9c7873688699aeadb4742d2.png)](https://supplyframe.com/)