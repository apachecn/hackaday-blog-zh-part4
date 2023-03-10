# OpenAI 听到你的低语

> 原文：<https://hackaday.com/2022/09/22/openai-hears-you-whisper/>

如果你希望不用买东西就能尝试高质量的语音识别，祝你好运。当然，你可以借用手机上的语音识别功能，或者强迫 Raspberry Pi 上的一些虚拟助手来为你处理这些信息，但对于你不想依赖于一些封闭源代码解决方案的主要工作来说，这些都不太好。OpenAI 已经推出了 [Whisper](https://openai.com/blog/whisper/) ，他们声称这是一个开源神经网络，“在英语语音识别方面接近人类水平的鲁棒性和准确性。”它似乎至少在其他一些语言上也能工作。

如果你试着演示一下，你会发现说得快或带着可爱的口音似乎不会影响结果。该帖子提到，它接受了 68 万小时的监督数据训练。如果你对一个人工智能说那么多话，你会花 77 年不睡觉！

在内部，语音被分割成 30 秒的片段，形成声谱图。编码器处理频谱图，解码器使用一些预测和其他试探法来消化结果。大约三分之一的数据来自非英语来源，然后被翻译。你可以阅读[论文](https://cdn.openai.com/papers/whisper.pdf)关于通用训练如何在标准基准上表现不如一些专门训练的模型，但他们相信 Whisper 在特定基准之外的随机演讲中表现更好。

“小”版本的模型大小仍然是 39 兆字节,“大”版本超过 1.5 兆字节。所以这可能不会很快在你的 Arduino 上运行。不过，如果你真的想编码，这一切都在 [GitHub](https://github.com/openai/whisper) 上。

还有其他的[解决方案](https://hackaday.com/2021/12/27/voice-command-made-mostly-easy/)，但是没有这个健壮。如果你想走助理这条路，这里有[的一些灵感](https://hackaday.com/2018/01/05/teaching-alexa-to-3d-print/)。