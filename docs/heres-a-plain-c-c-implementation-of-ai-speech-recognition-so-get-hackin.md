# 这是一个简单的人工智能语音识别的 C/C++实现，所以开始吧

> 原文：<https://hackaday.com/2022/11/27/heres-a-plain-c-c-implementation-of-ai-speech-recognition-so-get-hackin/>

[Georgi Gerganov]最近分享了一个在各种平台上运行高质量的人工智能驱动的语音识别的优秀资源。自动语音识别(ASR)模型仅使用两个源文件就完全实现了，并且不需要依赖关系。因此，高质量的语音识别不涉及调用远程 API，并且可以以相当直接的方式在不同的设备上本地运行。上图显示它在 iPhone 13 上本地运行，但它能做的不止这些。

[![](img/ba750326e851e2513e66c0f5a38c592d.png)](https://hackaday.com/wp-content/uploads/2022/11/Whisper-Console.png) 

利用【Georgi】的 OpenAI 的 *Whisper* 端口，实现在各种设备上本地运行的健壮语音转录要容易得多。

【Georgi】的工作是 OpenAI 的 *Whisper* 模型的一个移植，[这是一个非常强大的软件](https://hackaday.com/2022/09/22/openai-hears-you-whisper/)，它在将人类语言转换成文本方面做得非常出色。 *Whisper* 很容易设置和使用，但这个端口更容易让系统以其他方式工作。拥有这种模型的轻量级实现意味着它可以更容易地集成到各种不同的平台和项目上。

OpenAI 的 *Whisper* 通常的工作方式是给它输入一个音频文件，它会吐出一份转录。但是[Georgi]展示了其他可能给黑客灵感的东西:[一个简单的实时音频输入例子](https://github.com/ggerganov/whisper.cpp#real-time-audio-input-example)。

通过使用一个工具来流式传输音频并每半秒钟将它馈送给系统，可以获得相当好的(某种)实时结果！这当然不是一个理想的方法，但是 *Whisper* 的健壮性和准确性使得结果看起来非常好。

你可以在分页符下面的视频中快速观看演示。如果它给了你一些想法，那就去[该项目的 GitHub 库](https://github.com/ggerganov/whisper.cpp)看看吧！

 <https://hackaday.com/wp-content/uploads/2022/11/194935793-76afede7-cfa8-48d8-a80f-28ba83be7d09.mp4?_=1>

[https://hackaday.com/wp-content/uploads/2022/11/194935793-76afede7-cfa8-48d8-a80f-28ba83be7d09.mp4](https://hackaday.com/wp-content/uploads/2022/11/194935793-76afede7-cfa8-48d8-a80f-28ba83be7d09.mp4)