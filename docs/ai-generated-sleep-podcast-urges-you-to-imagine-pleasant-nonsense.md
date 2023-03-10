# 人工智能生成的睡眠播客敦促你想象愉快的废话

> 原文：<https://hackaday.com/2022/03/26/ai-generated-sleep-podcast-urges-you-to-imagine-pleasant-nonsense/>

[Stavros Korokithakis]发现听着童话入睡的体验令人宽慰，这导致了一个令人着迷的项目，通过使用机器学习产生轻度不连贯的童话并大声朗读它们来满足这种愿望。其结果是一种神奇的自动化，机器生成的听觉睡眠援助。连 logo 都是机器生成的！

[![](img/c3a68c7a6dcdcd8549ea12218971c0a1.png)](https://hackaday.com/wp-content/uploads/2022/03/logo.jpg)

The *Deep Dreams Podcast* is entirely machine-generated, including the logo.

该项目利用 OpenAI 的 GPT-3 的自然语言生成能力来创建童话般的内容，这些内容是 T2 的，听起来很自然，但 T4 的不够连贯，不足以构成一个合理的情节。这种准清晰、如梦似幻的效果非常适合敦促听众在昏昏欲睡时想象愉快的废话(感谢[内森·W·派尔](https://twitter.com/nathanwpyle)对这个术语的使用)。

我们特别喜欢阅读[Stavros]在创建这个项目时遇到的方法和挑战。例如，他谈到好听的叙述不仅仅是指着一堵文本墙的文本到语音转换引擎，然后发出“GO”的声音。一部好的剧集会有策略性的停顿、背景音乐和音频渐变。这就是 pydub(一个用于处理音频的 Python 库)派上用场的地方。至于语音，文本到语音的质量甚至超过了几年前的水平(当然也超过了 80 年代的[机器生成语音](https://hackaday.com/2020/08/27/38-years-later-the-atari-2600-learns-to-speak/))，但仍然需要一些工作来确定最适合内容的声音，该项目逐渐取得了进展。

如果你想看驱动这一切的代码，深度梦境播客有一个 [GitLab 库](https://gitlab.com/stavros/deep-dreams)，你可以[去播客本身](https://deepdreams.stavros.io/)听一听。