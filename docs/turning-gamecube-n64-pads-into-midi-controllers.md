# 将 GameCube 和 N64 手柄变成 MIDI 控制器

> 原文：<https://hackaday.com/2021/06/19/turning-gamecube-n64-pads-into-midi-controllers/>

公平地说，任天堂 64 和 GameCube 都拥有各自主机一代中最独特的控制器。随着 *Smash Bros.* 社区继续青睐其传统的控制方案，后者的游戏手柄今天仍有很高的需求。然而，由于[po8aster]的工作，这两个控制器都可以很容易地重新用于音乐手段。

该项目有两种形式——分别是[GC MIDI 控制器](https://github.com/po8aster/GCMIDIController)和[N64 MIDI 控制器](https://github.com/po8aster/N64MIDIController)。每个都使用一个 Arduino Pro Micro 来运行节目，一个逻辑电平转换器，以及[【尼克胡德的】任天堂库](https://github.com/NicoHood/Nintendo)来与控制器通信。从那里，控制器输入被映射到 MIDI 信号，并通过传统或 USB MIDI 输出。

这两个版本都配有合成器模式和鼓模式，以便让用户有效地演奏旋律或打击乐。对于使用 GameCube 版本的大金刚邦戈控制器打鼓，也有一个特殊的映射。对于那些渴望购买工作单元而不是建造自己的单元的人来说，他们可以在[po8aster's]网站上购买。

将视频游戏硬件重新用于音乐目的是一件有趣的事情，我们确信有一些 chiptune 乐队会喜欢用这样的设置来表演。我们以前在任天堂硬件上见过其他伟大的 MIDI 黑客，从电路弯曲的 SNES 可视化器到 MIDI 合成器 Game Boy Advance。休息后的视频。

> 如果你想成为一个用视频游戏控制器播放音乐的酷呆子，我正在做一个生日大甩卖，所有东西都打八折！🎮🎶
> 
> 代码/链接👇RTs 赞赏🙏[pic.twitter.com/GqBpGUFWLe](https://t.co/GqBpGUFWLe)
> 
> –偷猎者(@偷猎者)[4 月 30 日，2021 年](https://twitter.com/Po8aster/status/1388137464456417283?ref_src=twsrc%5Etfw)