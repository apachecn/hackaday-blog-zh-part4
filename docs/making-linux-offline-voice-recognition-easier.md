# 让 Linux 离线语音识别更容易

> 原文：<https://hackaday.com/2021/09/25/making-linux-offline-voice-recognition-easier/>

对于任何你想命名的任务，一台基于 Linux 的台式计算机可以使用与其他平台上的应用程序相媲美或更好的应用程序来完成工作。然而，这并不意味着让它工作总是很容易，语音识别只是那些困难的设置之一。

一个名为 [Voice2JSON](https://voice2json.org) 的项目正试图简化语音工作流程的使用。虽然它不提供实际的语音识别，但它确实使事情变得更容易，然后以自然的方式使用语音。

该软件可以与几个后端集成来进行离线语音识别，包括 CMU 的 pocketsphinx，丹·波维的 Kaldi，Mozilla 的 DeepSpeech 0.9 和京都大学的 Julius。然而，代码不仅仅是这些工具的薄薄的包装。快速训练过程产生语音识别器和意图识别器。所以你不仅知道有车库门，而且对车库门的开关有所了解。

此外，这些工具都可以在 Unix 风格的管道中工作，这令人耳目一新。以下是项目网站上的配置示例:

```
[GarageDoor]
open the garage door
close the garage door

[LightState]
turn on the living room lamp
turn off the living room lamp
```

有一些模板特性，因此您可以在单个规则中指定可选单词和替换单词。还有其他功能，比如将客厅灯这样的物体映射到更适合计算机的物体上。

总的来说，这看起来是一个有趣的工具。如果你用它做了一些有趣的事情，一定要给我们一个[提示](https://hackaday.com/submit-a-tip/)，这样我们就可以报道它了。同时，我们已经看了[的 Linux 演讲](https://hackaday.com/2018/01/17/speech-recognition-for-linux-gets-a-little-closer/)很久了。当然，我们真正想要的是像企业号一样的[语音命令](https://hackaday.com/2016/06/08/talking-star-trek/)，我们不得不承认它越来越近了。