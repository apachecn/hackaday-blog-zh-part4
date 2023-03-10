# 四个步进器组成一个四声部的 MIDI 乐器

> 原文：<https://hackaday.com/2020/08/15/four-steppers-make-a-four-voice-midi-instrument/>

任何廉价 3D 打印机的所有者都会告诉你，它们可能是非常嘈杂的设备，因为它们的步进电机和驱动器的组合是为了成本而不是安静而选择的。但是，如果噪音是一种资产，烦人的踏步机声音可以用作乐器吗？这个问题[大卫·斯霍尔滕]已经用 [Stepper Synth](https://hackaday.io/project/173791-stepper-synth) 解决了，这是一个使用 Arduino Uno 和四个步进电机来创建四声部 MIDI 合成器的设备。

硬件方面，它和你想象的一样简单，一个有四个步进电机的盒子，每个电机的轴上都有一个红色的 3D 打印的标志，以显示旋转。下面是 Arduino，加上一个机器人控制盾和一组步进驱动器板。在软件方面，它使用 MIDI-over-serial，所以作为一个 Windows 用户，他对主机的指令只适用于该操作系统。Arduino 利用了 [Arduino MIDI 库](https://github.com/FortySevenEffects/arduino_midi_library)，他分享了关于禁用未使用电机以防止过热的技巧。

你可以在休息时间下面的视频中听到它的运行，我们很惊讶地说它听起来并不太糟糕。在那里的某个地方有一些几乎让人想起教堂风琴的东西，用某种声学外壳来改进它会很有趣。

这不是我们带给你的第一个这样的乐器，一个特别令人印象深刻的例子是看一看[flop tron](https://hackaday.com/2016/07/13/nirvana-like-youve-never-heard-them-before/)。

 [https://www.youtube.com/embed/1Op7-QJsL9I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/1Op7-QJsL9I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

