# GridSound——浏览器中的音频工作站

> 原文：<https://hackaday.com/2020/08/17/gridsound-an-audio-workstation-in-your-browser/>

如果你对创作音乐感兴趣，你会有令人惊讶的各种各样的开源选项供你选择，从 Audacity(相当简单的音频编辑器)到 Ardour(成熟的、值得录音室使用的 DAW)——还有 LMMS、玫瑰园、缪斯等等。任何介于两者之间的东西。[有了[Thomas Tortorini]的 GridSound 项目](https://gridsound.com/)，现在你的列表上又多了一个选择，除了这个在你的浏览器中运行。因此，如果你发现自己突然有了灵感，你只需要一个浏览器就可以了。

从功能集的角度来看，GridSound 倾向于 LMMS，提供架子鼓、钢琴卷帘窗和合成器。现在看来，你还不能录制真实世界的乐器，但这也是一项正在进行的工作，所以谁知道未来会发生什么。代码可以在 [GitHub](https://github.com/gridsound/daw) 上获得，你可以在这里探索 GridSound 本身[——不需要登录，除非你想保存你的工作。GridSound 在浏览器中运行，自然是用 JavaScript 编写的，并使用](https://gridsound.com/daw/)[网络音频 API](https://developer.mozilla.org/en-US/docs/Web/API/Web_Audio_API) 来执行实际的音频任务。

令人印象深刻的是，[Thomas] [选择了](https://github.com/gridsound/daw/issues/56#issuecomment-606964049)来反对任何一周一次的 UI 框架，而是用纯普通的 JavaScript 从头开始实现一切。事实上，整个代码库似乎是独立的，没有任何第三方依赖，这本身就值得一些尊重。当然，JavaScript 不是每个人都喜欢的——[“真正的开发人员使用汇编”](https://hackaday.com/2019/04/04/webassembly-what-is-it-and-why-should-you-care/)——所以如果你喜欢更实际的东西，[来点硬纸板音乐](https://hackaday.com/2019/10/08/making-music-from-cardboard/)怎么样？