# 对着水龙头说话

> 原文：<https://hackaday.com/2018/09/01/talk-to-the-faucet/>

你的手因为最近的项目而变得很脏，你需要流水来清洗它们。但是你不想把水龙头也弄脏吧。如果你能告诉他们打开热或冷，那不是很好吗？或者如果水太冷，你可以告诉他们把水加热。[Vije Miller]就是这么做的，[他在他的厨房水龙头上添加了伺服电机](https://hackaday.io/project/159473-voice-kitchen-faucet)，并让人工智能来解释他的语音命令。

仔细看照片，你可以猜到他是从一个单杠杆类型的水龙头开始的，那种可以用肘部工作的水龙头，所以这个项目可能只是为了好玩，从他下面的视频来看，他确实有幽默感。但是这个想法对于带有旋转旋钮的双龙头是可行的。然而，他确实意识到，在未来的版本中，他应该将伺服电机开口从顶板移到底部，以避免任何水进入。NodeMCU ESP8266 ESP-12E 板用于与语音识别端通信，但除了名字 JacobAI 之外，他将语音部分留给自己。我们暗中怀疑他有一个叫雅各布的朋友。

然而，我们可以为它想到一些选项，如我们在谈论[自然语言手机机器人](https://hackaday.com/2018/06/21/make-a-natural-language-phone-bot-like-googles-duplex-ai/)时提到的 DeepSpeech 和 Wit.ai，以及无处不在的 Alexa as [，这里使用另一个 NodeMCU 来打开圣诞树灯](https://hackaday.com/2017/12/31/an-iot-christmas-tree-for-your-hacker-mas-celebrations/)。

 [https://www.youtube.com/embed/Q8RrCvtyXEc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Q8RrCvtyXEc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

