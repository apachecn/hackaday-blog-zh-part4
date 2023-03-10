# Poly 键盘的每个键上都有屏幕

> 原文：<https://hackaday.com/2022/10/17/poly-keyboard-has-screens-in-every-key/>

当在不同语言之间切换时，不同的键盘布局和字符集会阻碍有抱负的多语者。[Thomas Pollak]的 [Poly Keyboard](https://ko-fi.com/polykb/posts) 通过在键盘的每个键上都放置一个屏幕来规避这个问题。

在他的大量构建日志中，[Pollak]详细描述了他在将这款神奇的键盘投入使用时所面临的不同挑战。例如，有机发光二极管屏幕需要[字形渲染](https://ko-fi.com/post/A-Focus-On-Software-Q5Q8EXJYH)来处理按键上的图例。由于目标是真正的通用语言支持，他使用阿达果-GFX 库作为起点，并在他的 QMK 的[定制分支中扩展了对日语、韩语和阿拉伯语的支持。](https://github.com/thpoll83/qmk_firmware)

这座建筑对细节的关注令人印象深刻。除了致力于完整的字形支持，[Pollak]还测量了来自 OLEDs 的柔性电缆对按键开关的驱动所增加的额外力量。对于他测试的 Gateron 黄色开关，差异约为 62.2 克，而最初为 49.7 克。

如果你认为你已经看过其他的屏幕键盘项目，[Pollak]在他的日志中也包括了一个类似项目的[综述。这不是我们在 Hackaday 这里看到的第一个按键开关上有有机发光二极管的键盘，尽管](https://ko-fi.com/post/Comparing-With-Existing-Projects-S6S4F9Z98)[【虚空之星实验室】的幻影](https://hackaday.com/2021/10/30/a-hackable-keyboard-that-even-has-screens/)只有三个屏幕键，在后来的迭代中[移除了。如果你想在你的键盘上安装一个更传统的固定显示器，看看](https://hackaday.com/2022/08/02/the-rollercoaster-of-developing-the-ultimate-hackable-keyboard/)[【彭志惠】的模块板](https://hackaday.com/2022/07/28/smart-modular-keyboard-sports-an-e-ink-display-and-a-haptic-feedback-knob/)，它有一个电子墨水显示器和触觉反馈旋钮。

> 再来一次，因为这太有趣了；)现在加上葡萄牙语、意大利语、土耳其语、法语和西班牙语[# PolyKeyborad](https://twitter.com/hashtag/PolyKeyborad?src=hash&ref_src=twsrc%5Etfw)[# mechanical keyboard](https://twitter.com/hashtag/MechanicalKeyboard?src=hash&ref_src=twsrc%5Etfw)[#有机发光二极管](https://twitter.com/hashtag/OLED?src=hash&ref_src=twsrc%5Etfw)[pic.twitter.com/AC791tzEfp](https://t.co/AC791tzEfp)
> 
> —th poll(@ th poll 2)[2022 年 10 月 4 日](https://twitter.com/thpoll2/status/1577394618127290368?ref_src=twsrc%5Etfw)