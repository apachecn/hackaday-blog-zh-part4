# 基于带 RFID 的 Arduino 的儿童点唱机

> 原文：<https://hackaday.com/2022/12/16/kids-jukebox-based-on-arduino-with-rfid/>

针对儿童的消费电子产品往往很花哨，看起来很便宜，而且在这种情况下，它们通常必须经受住极端的压力测试。你可以买一个更高质量的正常使用的物品，但是这可能会在父母的口袋里烧出一个洞。为了解决儿童有声读物播放器的困境，[【Turi】为他的一个亲戚](https://turiscandurra.com/2022/11/grimmboy-arduino-controlled-kids-audio-player/)建造了这个格林博。

它的名字来自格林兄弟，这款播放器可以播放多种语言的儿童故事和寓言，每个故事和寓言都由一个类似的小盒式磁带代表，每个磁带中都隐藏着一个 RFID 标签。可以选择一盘磁带并将其放入播放器，位于其中心的 Arduino 将识别标签并播放存储在 SD 卡上的相应 MP3 文件。有简单的控制和所有的电路来支持它的锂电池。[Turi]用来构建它的所有源代码都可以在这个项目的 GitHub 页面上找到。

这也是阿鲁迪诺博客的特色，我们 T2 不久前也报道了一个类似的项目，只是略有不同。两者都基于 Tonuino 的想法，这是一个旨在将 Arduinos 转变为 MP3 播放器的开源项目。但是，如果你想构建一些具有更多功能的东西，看看[这个基于 RP2040 微控制器](https://hackaday.com/2022/09/20/walkmp3rson-is-an-mp3-player-like-sony-never-made/)的定制版本。