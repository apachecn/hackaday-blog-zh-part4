# 无论你走到哪里，树莓派都会演奏一首迷笛

> 原文：<https://hackaday.com/2020/06/08/raspberry-pi-plays-a-midi-tune-wherever-you-may-roam/>

MIDI 控制器键盘非常棒，因为它们可以让您控制插入的任何合成器。唯一的缺点是:你需要一个合成器来将 MIDI 音符转换成真实的声音，这让一些夏夜篝火小夜曲变得有点复杂。但对[乔迪]来说不是，他决定制造[纳米皮，一种便携式的 MIDI 乐器，内置树莓皮](https://www.youtube.com/watch?v=UdR3oF37UaQ)。

使用 Korg nanoKEY2 USB MIDI 控制器作为设备的基础，[Geordie]将其拆开，添加了一个 Raspberry Pi Zero W，一个为其供电的电源组，一个连接同样添加的 USB 音频接口的 USB 集线器，以及控制器本身。由于 nanoKEY2 天生纤薄，这些都不适合它，所以他设计并 3D 打印了一个框架来增加它的高度。他没有在内部布线，而是决定将电源和数据线布线到外部，并将它们连接回设备本身，这样他就可以在需要时单独使用电源组和控制器本身。

在软件方面，Pi 运行您常用的开源软件合成器 Fluidsynth。为了控制 Fluidsynth 本身——例如更换仪器——[ Geordie]实际上在他的手机上使用 Termius SSH 客户端，允许他以这种方式关闭 Pi。虽然 Fluidsynth 的内置 MIDI 路由器可以替代地重新映射 nanoKEY2 的附加按钮，但该功能似乎仅限于相同类型的信息，因此按钮的控制更改信息无法重新映射到所需的程序更改信息。嗯，如果需要的话，总是可以选择安装一些额外的按钮。或者你可以在软件方面做些聪明的事情。

正如你可能已经注意到的，nanoPi 不包括任何扬声器——考虑到它的大小，这可能是最好的。因此，虽然它不是一个完全独立的工具，但它是一个很好的，紧凑的设备，可以在任何地方与你的耳机一起使用。由于其灵活的布线，你还可以将任何其他 USB MIDI 控制器连接到它，例如[这个小木管乐器控制器](https://hackaday.com/2017/11/13/pocket-woodwind-midi-controller-helps-you-carry-a-tune/)，或者[那个播放所有流行歌曲的控制器](https://hackaday.com/2017/07/28/four-chords-should-be-enough-for-anyone/)。

 [https://www.youtube.com/embed/UdR3oF37UaQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/UdR3oF37UaQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent) 
 [https://www.youtube.com/embed/muioXGz59qY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/muioXGz59qY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

