# 机器学习检测分心的政客

> 原文：<https://hackaday.com/2022/01/17/machine-learning-detects-distracted-politicians/>

[德里斯·德普特]擅长于高度技术化的项目，有着坚实的艺术倾向，这件作品也不例外。[佛兰德滚动器](https://driesdepoorter.be/theflemishscrollers/)是一个软件系统，它可以观看佛兰德政府的直播会议，并使用 Python 和机器学习来识别和突出显示拿出手机并开始滚动的政治家。结果呢？很自然地在 Twitter 和 Instagram 上发布了。该项目始于 2021 年 7 月，自那以来一直在尽职尽责地运行，因此到目前为止，我们预计将手机放在摄像头可以看到的地方可能会被认为是新手的错误。

这个项目也可以被认为是一个很好的例子，说明如何根据应用程序正确处理结果的可信度。在这种情况下，假阴性(一名政客正在使用手机，但软件没有正确检测到它)比假阳性(一名成员被错误地识别，或在没有使用移动设备时被错误地叫出来)更容易接受。)

[Keras](https://keras.io/) ，开源软件库，用于物体检测和面部识别(这里 Keras 的 GitHub 库是)。)我们已经看到它被用在从[蝙蝠探测](https://hackaday.com/2017/08/10/we-should-stop-here-its-bat-country/)到[自动垃圾分类](https://hackaday.com/2019/09/01/automate-sorting-your-trash-with-some-healthy-machine-learning/)的所有事情上，所以如果你对机器学习应用感兴趣，不妨一睹为快。