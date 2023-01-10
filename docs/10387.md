# 12-Arduino 管弦乐队奏响《星球大战》的号角

> 原文：<https://hackaday.com/2021/06/11/12-arduino-orchestra-plays-star-wars-fanfare/>

早在音乐合成器的早期，一些希望在他们的乐器中使用复调音乐的设计师会简单地为他们希望演奏的多个音符构建多个音调发生器。[凯文]对他的 Arduino 管弦乐队采取了同样的方法，并着手让它演奏《星球大战:新的希望》的闭幕曲。

该构建包括 12 个 Arduino Nanos，每个都连接到电源、一个扬声器和相同的 MIDI 电缆。MIDI 电缆在单独的 MIDI 通道上传送每个 Arduino 的音符数据，允许每个 Arduino 在管弦乐队中扮演自己的角色。[Kevin]然后着手将《星球大战》的音乐整理成一个适合 Arduinos 的 MIDI 文件，大致设置六个声部为高音，六个声部为低音。Arduinos 使用 simple tone()功能播放收到的音符。结果是世界上最著名的太空歌剧第四集的结尾部分非常合拍。

它可能不整洁，不整齐，或者没有效率，但它肯定是有趣的。十二个 Arduinos 带着闪烁的 led 和可爱的小扬声器发出哔哔声，成为了热门话题。这是一种类似于软盘驱动器的方法，通过添加更多的软盘驱动器来播放更多的音符。 [我们也看到了同样的事情发生在 SEGA 的声音芯片上。](https://hackaday.com/2018/01/08/eight-segas-singing/)休息后的视频。

 [https://www.youtube.com/embed/qswqjhcMhPk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=142&wmode=transparent](https://www.youtube.com/embed/qswqjhcMhPk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=142&wmode=transparent)

