# 用这个烦人的蜂鸣器打破大写锁定习惯

> 原文：<https://hackaday.com/2019/11/13/break-the-caps-lock-habit-with-this-annoying-buzzer/>

备受指责的 Caps Lock 键几十年来一直在引发问题，它的继续存在引起了足够的争议，以至于谷歌决定在他们的 Chromebooks 中一起放弃它。在业内其他人决定跟随他们之前，他们可能不会缺少尴尬的电子邮件或过于咄咄逼人的评论，这些都是这个危险的关键的直接结果。

但是[【格伦·艾金斯】认为他有解决方案](https://bikerglen.com/blog/updates-to-the-annoying-caps-lock-warning-buzzer/)。他的发明是一个微小的 USB 通知设备，只有一个目的:只要按下 Caps Lock 键，就会发出可怕的声音。你可以把它想象成键盘上的小 LED 指示灯，但它会发出可怕的尖锐噪音，让你无法忽视。这之所以成为可能，是因为 Caps Lock 状态是在操作系统级别处理的，而不是在本地输入设备上。

通知程序是围绕 PIC16F1459 构建的，因为它允许他实施 USB 2.0，同时保持较低的器件数量。除了 PIC 之外，电路板还使用一些无源器件和一个晶体管，通过 PWM 信号驱动蜂鸣器。为了避免重复劳动，所有东西都被设计成适合他已经为他的[单键键盘开发的外壳，我们去年已经介绍过](https://hackaday.com/2018/05/19/one-key-keyboard-is-exercise-in-sub-millimeter-design/)。[Glen]和一位是德科技的同事一起制作了一个关于蜂鸣器的制作和使用的精彩视频，休息后你可以看到。

在光谱的另一端，甚至更小的是“USB Capslocker ”,它旨在将键盘的这个已经很麻烦的功能武器化。

 [https://www.youtube.com/embed/TKJELAEZjT4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/TKJELAEZjT4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

