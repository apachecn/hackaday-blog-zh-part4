# 使用 AY-3-8910 通过 USB MIDI 进行芯片调谐

> 原文：<https://hackaday.com/2019/07/30/chiptunes-via-usb-midi-with-the-ay-3-8910/>

在 chiptune pantheon 中有许多古老的声音芯片，其中 AY-3-8910 可能是不太为人所知的一个。由于没有在任天堂或 Commodore 服过役，它在美国有些不受欢迎，但它在各种街机和弹球机上出名，并因其出现在印有 Amstrad 和 Sinclair 名称的机器上而拥有相当多的欧洲追随者。[【the spodshed】决定在 Arduino Pro Micro 的帮助下，为芯片设计一个 USB MIDI 接口。](https://www.instructables.com/id/Arduino-MIDI-Chiptune-Synthesizer/)

Arduino Pro Micro 是一个 Sparkfun 产品，使用 ATmega32U4 微控制器。它的 USB MIDI 功能使它成为这样一个构建的完美候选，它还包含足够的数字 IO 来运行 AY-3-8910，需要 13 条线来运行。[TheSpodShed]在 protoboard 上迅速完成了这个项目，只需要几个被动设备，以及声音芯片和 Arduino。

Arduino 代码的编写着眼于充分利用芯片有限的复音。synth 优先考虑最近收到的音符，同时也旨在尽可能保持当前请求的最高和最低音符仍在播放。这使得合成器在播放各种 MIDI 内容时，最有可能保持预期的低音和旋律不变。

这是一个整洁的建筑，显示了对一些人已经忘记的音乐芯片的热爱。当然，这不是唯一的选择——我们也看到过 [SAM2695](https://hackaday.com/2018/10/30/wavetable-general-midi-for-everyone/) 和 [YM2612](https://hackaday.com/2019/05/15/midi-synthesizer-from-a-sega-genesis/) 被给予同样的待遇。休息后的视频。

[https://player.vimeo.com/video/332946151](https://player.vimeo.com/video/332946151)