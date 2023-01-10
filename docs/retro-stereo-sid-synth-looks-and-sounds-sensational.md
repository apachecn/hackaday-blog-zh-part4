# 复古立体声 SID Synth 外观和声音耸人听闻

> 原文：<https://hackaday.com/2021/09/10/retro-stereo-sid-synth-looks-and-sounds-sensational/>

多年来，人们已经做了大量工作来模仿 Commodore 64 6581 SID 芯片，但正如[SlipperySeal]所说，没有什么能打败真正的芯片。他对基于 MIDI SID 的合成器的演绎不仅听起来很棒，而且看起来很有商业价值。

6581 SID 可以说赋予了 Commodore 64 在 8 位时代所有家用电脑中最好的声音功能(如果你不同意，请务必在评论中“关闭声音”)。6581 是一个三声部模拟合成器，有着令人眼花缭乱的设置。当时，大多数家用电脑只能发出不同长度和频率的“哔哔声”。

当你把 MIDI 和 SID 的功能混合在一起时，你会得到类似于[SlipperySeal]的令人敬畏的 synth，被称为“Monty”。虽然通往这一点的道路不幸导致了几个 SID 芯片的爆炸，但这种牺牲似乎得到了回报。

意识到“只有”三种声音的局限性，Monty 被设计成并行使用两个 SID 芯片，总共有六种声音，形成令人愉悦的立体声。MIDI 命令通过 ATmega1284p 微控制器传输到双 sid。至此，SID 已经被很好地理解了，[SlipperySeal]在 [GitHub](https://github.com/slipperyseal/monty) 上详细解释了 SID 编程的基础。

这不是第一个基于 C64 SID 芯片的 MIDI 合成器，但是[SlipperySeal]确保了他的与众不同。以电路板为中心的七段显示器构成了一个非常简单的可视化效果，当同时运行两个 Monty 电路板时，这种效果看起来更好，每个电路板都响应交替的 MIDI 通道(查看下面的视频)。自然，我们也喜欢包含不祥的、神秘的按键开关的项目。

 [https://www.youtube.com/embed/tqf2bS5UaQM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/tqf2bS5UaQM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

