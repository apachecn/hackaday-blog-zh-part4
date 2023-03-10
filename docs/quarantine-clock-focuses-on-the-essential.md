# 隔离时钟关注本质

> 原文：<https://hackaday.com/2020/04/12/quarantine-clock-focuses-on-the-essential/>

在这些自我隔离、社会距离和生活停滞的可怕时代，时间本身会变得相当模糊，甚至单词钟也可能看起来不必要的精确——特别是如果你碰巧有一个更特殊的昼夜节律。让我们面对现实吧，现在你通常的时间表可能已经变得无关紧要了，所以为什么还要为日期或确切的时间而烦恼呢？如果你能体会到这一点，那么[mwfisher3]已经为你准备了[完美的时钟](https://github.com/mwfisher3/QuarantineClock)，它只显示一周中的某一天，并粗略估计这一天的进度。

使用一个 Raspberry Pi 和一个备用触摸屏，[mwfisher3]有一个简单的游戏开始，所以时钟本身只是在 Kiosk 模式下运行的 Chrome，显示一个本地网站，一天中的时间映射到它们的文本表示数组。然后，几行 JavaScript 用当前日期和“时间”更新网站内容，一个 Python 脚本使用 [phue](https://github.com/studioimaginaire/phue) 库，根据飞利浦色调运动传感器的读数处理屏幕背光。

虽然这绝对是我们见过的最简单的时钟项目之一，但这种简单性实际上为一些简单的基于 JavaScript 的 web 显示提供了很好的介绍，没有太多的模糊和干扰。但是如果这不是你的事情，而你喜欢更机械的东西，我们最近报道了遵循相同想法的的[这一天钟，然后还有](https://hackaday.com/2020/04/08/what-day-is-it/)[这个灯箱](https://hackaday.com/2018/10/19/decorative-light-box-lets-you-guess-the-time/)以艺术的方式获得粗略的时间估计。