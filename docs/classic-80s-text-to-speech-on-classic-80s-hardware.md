# 经典 80 年代硬件上的经典 80 年代文本到语音转换

> 原文：<https://hackaday.com/2021/10/26/classic-80s-text-to-speech-on-classic-80s-hardware/>

我们这些生活在 70 年代末到 80 年代的人可能还记得 Speak & Spell，这是一个带有出色的文本到语音合成器的儿童玩具。虽然以今天的标准来看，它听起来有些过时，但它在当时是革命性的，并且正赶上那个时代各种计算机开始实现文本到语音转换功能的浪潮。虽然他们中的许多人使用专用硬件来执行语音合成，但一些计算机足够强大，可以在软件中完成这项工作，但其他人则不太能做到。[VIC-20 是后者中的一个，但由于 ESP8266，它被追溯性地赋予了这一功能](https://janderogee.com/projects/SerialSpeechSynthesisSAM/SerialSpeechSynthesisSAM.htm)。

这个项目来自[Jan Derogee]，他是这种复古计算机的鉴赏家，并建立在[Earle F. Philhower]的工作基础上，他将名为 SAM 的复古语音合成软件从汇编移植到 C 语言，这使得在 ESP8266 上运行成为可能。音频回放是在 I2S 端口上处理的，但需要做一些工作来使其顺利工作，因为该端口也处理与 VIC-20 的通信。一旦解决了这个问题，一个补丁就可以听到电脑的声音和语音合成器的声音。最后,[Jan]设计了一个串行命令接口，允许对模块进行控制。

虽然我们中没有多少人家里有 VIC-20，但这仍然是一个有趣的项目，它显示了像 ESP8266 这样的小型廉价芯片的广泛范围，这种芯片在 20 世纪 80 年代可能会有很高的价格。不过，如果你有其他 80 年代的硬件等着投入使用，看看这个项目[，它给古老的经典口语&拼写](https://hackaday.com/2012/12/03/teaching-the-speak-spell-four-and-more-letter-words/)带来了新的词汇。

 [https://www.youtube.com/embed/_YioAfmzkQc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/_YioAfmzkQc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

