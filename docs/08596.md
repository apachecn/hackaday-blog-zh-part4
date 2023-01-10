# 随着你喝酒，精神控制啤酒乒乓变得更容易

> 原文：<https://hackaday.com/2020/12/09/mind-controlled-beer-pong-gets-easier-as-you-drink/>

如果你喝得越多，啤酒乒乓就变得越简单，这不是很好吗？你知道，这样你就可以多喝点了？[Ty Palowski]已经用自动化的，精神控制的啤酒乒乓做到了这一点。

[Ty]开始做一个啤酒乒乓桌，可以在两端来回移动杯子。Arduino Nano 控制步进器，步进器控制滑块，杯子通过磁铁的魔力随着滑块移动。精神控制部分比你想象的要便宜。早在 2009 年，Mattel 发布了一款名为 Mind Flex 的游戏，其中包含一个脑电图耳机，并使用脑电波引导空气流中的泡沫球通过一个小障碍课程。这些耳机在易趣上售价约为 12 美元，或者至少在这篇文章发表之前是这样的。

[Ty]破解打开耳机增加了一个 HC-06 蓝牙模块与 Arduino 对话。它使用一个名为脑波 OSC 的程序从耳机中获取原始数据，并将其分为专注和放松的水平。Arduino 程序监控注意力水平，当注意力达到某个阈值时，它会以预定的速度来回移动杯子，速度范围从 1 到看起来不可能的 10。休息过后，请看两段视频。第一个包括自动啤酒乒乓部分的制作，第二个是[Ty]加入精神控制的地方。

我们已经看到一种不同的耳机——对黑客友好的 neuro sky mind wave——弹出几次。这里有一个被黑客攻击来诱导清醒梦的。

 [https://www.youtube.com/embed/RzPBX09sT4Y?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/RzPBX09sT4Y?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/-y8CHWx6aGY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/-y8CHWx6aGY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



通过 [r/duino](https://www.reddit.com/r/arduino/comments/k6qe1t/as_promised_from_the_comments_of_my_last_video/)