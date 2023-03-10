# Commodore 上的 HiFi 音频 64–48 khz，哟！

> 原文：<https://hackaday.com/2020/01/09/hifi-audio-on-the-commodore-64-48khz-yo/>

在 20 世纪 90 年代中期开发 CD 音质的音频硬件之前，家用电脑和游戏机通常只能用合成音乐来凑合。由于当时的存储和 RAM 限制，没有太多其他实用的选择。然而，如果你愿意忽略实用性，你可以做一些很棒的事情——比如在 Commodore 64 上播放高质量的音频！

该项目是[Antonio Savona]的作品，他开始在 Commodore 64 上播放高保真音频，只使用正确的硬件。这意味着没有 16MB 的 RAM 扩展，也没有疯狂的高容量手推车。那个时代最大的手推车只有 1MB，就像 Ocean 生产的那样,[Antonio]打算塞进整整 90 秒的音乐。

以 8 位样本为 48 KHz 的采样速率为目标意味着盒式磁带在其 1MB 的存储空间中只能容纳 20 秒的原始音频。这还不够好，所以音频必须被压缩，目标是 4:1 的比率以达到 90 秒的目标。C64 的 CPU 运行速度仅为 1MHz，当以 48 KHz 播放时，只有 21 个时钟周期来处理每个样本。

显然，[Antonio]已经设置了相当大的挑战，一些熟练的汇编代码被用来完成这项工作。最后的结果是音频听起来令人印象深刻的好，因为它是由一个 6502 泵出的，肯定是流汗完成这项工作。

我们喜欢围绕这些部分的一个好的 C64 hack，并且[现在甚至有可能从零开始建立一个新的](https://hackaday.com/2019/03/12/its-raining-brand-new-commodore-64s/)如果那是你特别渴望的。休息后的视频。

 [https://www.youtube.com/embed/UYAf_awh5XA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/UYAf_awh5XA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

