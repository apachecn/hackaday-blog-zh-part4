# 世界上最小的 MIDI 合成器，现在更好了

> 原文：<https://hackaday.com/2019/10/28/worlds-smallest-midi-synth-now-even-better/>

我们很确定没有国际公认的唱片仲裁者像“世界上最小的全功能复音立体声 MIDI 合成器，适合 DIN 外壳”。如果没有，肯定应该有，而且我们非常肯定 [[mitxela]的 Flash-Synth 会保存那个特定的记录](https://mitxela.com/projects/flash_synth)。

这是一些人无法独自面对挑战的教训之一。首先[mitxela]将一个 MIDI 合成器内置到一个 DIN 连接器中，然后几个月后，他制作了[一个更加精简的版本](https://hackaday.com/2016/03/30/the-attiny-midi-plug-synth/)。虽然两者都是大胆的工程壮举，但都不完全令人满意。只有方波合成和八个声部的限制，加上一些令人不快的音频问题和完全缺乏可制造性，下一个挑战是显而易见的。

我们不会假装遵循所有的音频奥秘，下面的视频和构建日志有很多，但技术成就是显而易见的。Flash-Synth 有一个 STM32，一个使其相形见绌的钽 SMD 滤波电容，以及一些位于柔性 PCB 上的支持元件，该 PCB 可折叠两次。这一点电路折纸连接到一个 5 针 DIN 插头，并塞进连接器的外壳，依次匹配到一个定制的金属外壳。立体声音频插孔位于组件的另一端，整个合成器由 MIDI 端口寄生供电。

下面视频的前半部分主要是一个演示，证明 synth 听起来很棒，可以做任何事情；跳到 22 分钟标记的血淋淋的建设细节。只要说[mitxela]过去在可笑的规模焊接方面的经验对他很有帮助就够了。

 [https://www.youtube.com/embed/KTvVS8guBsY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/KTvVS8guBsY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[Vikas]把这个放在我们的提示栏里。谢谢！