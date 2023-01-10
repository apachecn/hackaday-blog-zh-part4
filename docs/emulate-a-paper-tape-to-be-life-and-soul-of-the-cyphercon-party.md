# 模仿纸带，成为塞弗肯党的生命和灵魂

> 原文：<https://hackaday.com/2019/04/28/emulate-a-paper-tape-to-be-life-and-soul-of-the-cyphercon-party/>

最近的 Cyphercon 徽章配备了一个非常聪明的集成纸带阅读器，并具有派对模式的隐藏功能，其中所有的灯都会闪烁。当[Gigawatts]在会议结束后发现这一点时，已经太晚了，无法找到磁带来激活它。解决办法？[构建一个磁带模拟器](https://github.com/gigawatts/cyphercon4)，将微控制器连接到徽章的磁带传感器，将数据直接发送到其中。

这是一条来自[AND！XOR] 显示了闪烁的隐藏模式，如果你错过了它，你可以在[我们的评论](https://hackaday.com/2019/04/12/cyphercon-badge-has-a-paper-tape-reader-built-in/)中找到关于这个神奇徽章的所有信息。仿真器采用 TI Stellaris LaunchPad LM4F120 和一组直接焊接到徽章背面跳线的跳线。十六进制值是通过[一个带复选框界面的浏览器内 HTML 页面](https://github.com/gigawatts/cyphercon4/blob/master/punch-tape-decoder.html)从磁带创建的，一个草图将十六进制转换成磁带，徽章运行代码。GitHub 自述文件包括对纸带格式的描述，以及一些样本磁带，包括当你厌倦了派对模式时的徽章重置磁带。

我们中的大多数人都没有足够的运气去塞弗肯并获得一枚徽章。但是我们仍然对徽章设计者的独创性，以及徽章所属的 CTF 游戏的复杂性印象深刻。