# 手持机器人消除了吉他调音的乏味

> 原文：<https://hackaday.com/2021/09/24/handheld-bot-takes-the-tedium-out-of-guitar-tuning/>

即使有花哨的智能手机应用程序和定制的调谐器，给吉他调音也可能是一个乏味的过程，尤其是对初学者来说。拨动琴弦，判断音符是升还是降，相应地收紧或放松，重复。然后对所有六根弦做同样的事情。难怪有些人在吉他方面永远不会走得很远。

幸运的是，科技可以来拯救我们，这就是 Guyrandy Jean-Gilles 的便捷开源自动吉他调音器。调谐器内部有一个 Raspberry Pi Pico，麦克风连接到 ADC。在 Pico 上运行的程序监听拨弦的声音，并确定音符是升还是降。然后，微型钢琴驱动一个小的 DC 齿轮马达朝适当的方向转动，使弦轴转动到正确的方向，使琴弦调音。调谐器充分利用 3D 打印部件，STL 包含在项目报告中。[Guyrandy]也对项目做了一些更新，使调音器更容易使用。

虽然[Guyrandy]的设计基于这个有一个可负担得起的商业版本，但我们真的很喜欢他在这里推出自己的设计，并让每个人都可以免费使用这个设计。我们也喜欢这个想法，不能使用需要视觉反馈的调谐器的吉他手也可以使用这个——就像[这个](https://hackaday.com/2010/06/27/audible-tuner-for-the-blind/)。

[via [r/raspberry_pi](https://www.reddit.com/r/raspberry_pi/comments/pn7z7y/automatic_guitar_tuner_with_the_pico_sound_on/)