# " Alexa，不要听我说，否则我会把你的耳朵割下来"

> 原文：<https://hackaday.com/2021/02/02/alexa-stop-listening-to-me-or-ill-cut-your-ears-off/>

自从我们开始邀请他们进入我们的家，我们中的许多人开始对我们的智能扬声器投以警惕的目光。他们到底在用我们不断产生的音频流做什么，其中一些来自最亲密和私人的时刻？当然，这些设备背后的大公司声称它们很好，但我们真的有人相信吗？

看起来最谨慎的方法是不要使用这些设备，但是它们是非常有用的工具。因此[这款亚马逊 Echo 的硬件静音开关](https://hackaday.io/project/177223-echo-dot-hardware-microphone-mute-modification)代表了数字勒德主义和忽视智能扬声器可能存在的隐私风险之间的中间地带。是的，这些设备都有禁用麦克风阵列的软件选项，但正如[Andrew Peters]所说，他的关注点主要是阻止对智能扬声器的外来攻击，其中一些攻击，如[激光诱导光声攻击](https://hackaday.com/2019/11/06/laser-based-audio-injection-on-voice-controllable-systems/)，我们之前已经讨论过。对于这项工作，只有麦克风的硬件级断开才能完成。

为了实现这一点，[Andrew]在他的 Echo Dot Gen 2 中嵌入了一个 Seeeduino Xiao。微型微控制器将七个(！idspnonenote)共享的公共 I S 数据线接地。)智能扬声器中的麦克风，有效禁用它们。启用和禁用麦克风是通过现有的点键完成的，通过点扬声器发送的音调提供反馈。这是一个非常巧妙的模型，安德鲁在研究这个模型时所做的大量文档令人印象深刻。下面的视频和附带的 GitHub 回购对其他智能音箱黑客来说应该是无价的。

 [https://www.youtube.com/embed/OSyf_FsDwfk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/OSyf_FsDwfk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

