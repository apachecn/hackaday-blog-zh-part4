# 实时显示您的讲话，帮助口罩时代的唇读者

> 原文：<https://hackaday.com/2022/01/23/display-your-speech-in-realtime-to-help-lipreaders-in-the-mask-era/>

当谈到减少致命病原体的传播时，口罩固然很好，但当人们说话时，它们会使人们更难理解。它们也使唇读成为不可能。[[凯文·刘易斯]着手建造一些有帮助的东西。](https://twitter.com/_phzn/status/1478504862170161152?ref_src=twsrc%5Etfw%7Ctwcamp%5Etweetembed%7Ctwterm%5E1478504862170161152%7Ctwgr%5E%7Ctwcon%5Es1_&ref_url=https%3A%2F%2Fhackaday.com%2Fwp-admin%2Fpost.php%3Fpost%3D516699action%3Dedit)

该系统由一个可以佩戴在胸部或身体其他部位的小屏幕和一个记录佩戴者讲话的翻领麦克风组成。使用运行在 Raspberry Pi Zero W 上的 Deepgram AI 语音识别 API，系统对语音进行解码，并将其显示在超像素屏幕上。

该 API 非常强大，可以设置为仅响应佩戴者的声音，或者在群组模式下，显示区域中多人的语音[，以另一种颜色显示其他声音。还有一个使用 iTranslateApp API 的翻译特性](https://twitter.com/_phzn/status/1478821408486699009)。

这是一个简洁的工具，在会议中或者在快速简单的机器翻译可以大大简化交流的情况下非常有用。休息后的视频。


> 面具让你很难听懂别人的话，要么是因为你依赖唇读？刚刚把这个黑到一起——它实时显示我和 [@DeepgramAI](https://twitter.com/DeepgramAI?ref_src=twsrc%5Etfw) 的讲话！pic.twitter.com/lPu4CZboIk
> 
> —凯文·刘易斯(他/他)(@ _ phzn)[2022 年 1 月 4 日](https://twitter.com/_phzn/status/1478504862170161152?ref_src=twsrc%5Etfw)