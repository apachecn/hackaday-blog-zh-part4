# 给阿姆斯特拉德 CPC 一个声音和一套鼓

> 原文：<https://hackaday.com/2019/08/12/giving-the-amstrad-cpc-a-voice-and-a-drum-kit/>

早在 80 年代，家用电脑在音频或多媒体方面整体上没有多大能力。可以说，直到 Amiga 等 16 位计算机的出现，音乐家们才能够制作出原声质量的音乐，而不必将实际的录音室设备插入他们的机器。[Michael Wessel]正试图通过他雄心勃勃的 LambdaSpeak 3 项目将其中一些功能和更多功能引入 Amstrad CPC[，这是一款完全从零开始构建的扩展卡，挤满了各种功能。](https://hackaday.io/project/165677-lambdaspeak-3)

首先，也可能是它的名字，是语音合成器。[迈克尔]已经建立了一个仿真模式，他的卡可以像最初的 SSA-1 扩展一样工作，能够由当时相同的软件控制。默认情况下，该卡通过 Epson S1V30120 子板(基于 DECTalk synthesis)提供这种模式，但是为了进一步验证，您也可以选择安装 SP0256-AL2 芯片，与 1985 年最初的 Amstrad 硬件中使用的芯片相同。

至于该项目的音乐部分，该板支持 4 通道 PCM 播放，很像 Amiga 的声音产品。这可以用于鼓机音序器程序，它有一个 Amdrum 模式，模拟另一个从最初的 Amstrad 天扩展。样本回放也可以与语音合成一起使用[，如图所示](https://www.youtube.com/watch?v=M7aI7KLEi1s)，随机的音位变体节拍在发电厂乐团录音中听起来不会不合适。最后，通过使用 LambdaSpeak 上包含的 UART 接口，您还可以通过给 CPC 提供 MIDI 输入/输出并将控制器与计算机的 AY-3-8912 声音芯片实时连接，将 CPC 本身变成合成器。

如果你喜欢让旧电脑重获新生的现代扩展，你知道吗，你可以在网上买到任何复古电脑，也许是一台 [TRS-80](https://hackaday.com/2019/02/11/a-network-card-for-the-trash-80/) 、一台[阿米加](https://hackaday.com/2019/07/03/amiga-in-the-mist-gets-online-with-an-esp8266/)甚至是一台[心灵感应组织器](https://hackaday.com/2019/08/03/raspberry-pi-helps-vintage-psion-find-its-voice/)？如果你对将旧系统的声音芯片与现代 USB MIDI 控制器结合使用感兴趣，[让微控制器承担所有繁重的工作](https://hackaday.com/2019/07/30/chiptunes-via-usb-midi-with-the-ay-3-8910/)是很容易的。

 [https://www.youtube.com/embed/M7aI7KLEi1s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/M7aI7KLEi1s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/RRG1JTxKXD8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/RRG1JTxKXD8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

