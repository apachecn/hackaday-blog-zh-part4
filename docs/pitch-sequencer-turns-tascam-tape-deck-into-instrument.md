# 音高音序器将 Tascam 磁带走带设备变成乐器

> 原文：<https://hackaday.com/2022/05/11/pitch-sequencer-turns-tascam-tape-deck-into-instrument/>

磁带最酷的地方在于，通过改变回放速度，你可以改变输出的音调。[Issac]决定利用这一点，[在他的 Tascam Porta 02 走带设备上执行一个奇特的数字控制音高调制。](https://www.instructables.com/Pitch-Sequencer-for-Tascam-Porta-02-PWM-Microcontr/)

该版本使用 Raspberry Pi Pico，它采用 PWM 来控制磁带机电机的速度。这是通过使用由 Pico 的 PWM 输出驱动的 NPN 晶体管实现的。这样可以精确控制电机速度，从而控制螺距。

解决了这个问题后，这个项目就有了有机发光二极管屏幕和旋转编码器。这些允许各种补丁或脚本在 Pico 上运行，以各种方式控制磁带播放器的电机速度。稍加努力，[Issac]还能够创建一个函数，将 MIDI 音符值转换为决定各种电机速度的 PWM 值。

接下来要做的自然的事情是把一个循环样本放入一个固定间距的磁带中，然后在 Pico 的控制下按顺序改变它。该序列的 8 个步骤可以通过旋转控制手动设置，将来，[Issac]甚至计划添加一个真正的 MIDI 输入，允许系统作为单声道合成器。

如果你更喜欢其他路线而不是变调诡计，[看看这个项目](https://hackaday.com/2011/03/17/pitch-shifter-makes-your-band-sing-higher/)。休息后的视频。

 [https://www.youtube.com/embed/hcBXBUudQDU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/hcBXBUudQDU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

