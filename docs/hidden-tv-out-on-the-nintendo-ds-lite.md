# 任天堂 DS Lite 上的隐藏电视输出

> 原文：<https://hackaday.com/2021/02/28/hidden-tv-out-on-the-nintendo-ds-lite/>

DS Lite 是任天堂最受欢迎的掌上游戏机之一，但所有人都不知道的是，它有一个隐藏的功能，可能会使它更受欢迎。通过对硬件和固件的挖掘，【迷失任天堂历史】团队发现 [DS Lite 中的片上系统(SoC)可以输出复合视频信号](https://lostnintendohistory.github.io/DS-TV-OUT)。

SoC 可以输出 10 位数字输出，工作频率为 16.7 MHz，但在引导过程早期，它被库存固件禁用，因此需要定制固件。它仍然需要转换成模拟信号，因此带有 DAC(数模转换器)和运算放大器的小型适配器板连接到上屏幕的柔性电缆。板上的一组按钮允许您选择在电视上显示哪个屏幕。适配板是开源的，GitHub 上有[gerber 和原理图。](https://github.com/LostNintendoHistory/Lost-NDS-TV)

当前版本的转接板禁用了上部屏幕，但[失落的任天堂历史]团队正在考虑设计一个直通板来消除这一缺点。TV-out mod 也可以与流行的[微距 mod](https://hackaday.com/2012/08/22/turning-a-ds-into-a-game-boy-advance/) 结合，在微距 mod 中，上部屏幕被移除，以将其变成 Game Boy Advance。任天堂 DS 是一个受欢迎的黑客主题，我们已经报道他们[十多年了](https://hackaday.com/2005/04/21/more-homebrew-nintendo-ds-fun/)。