# 游戏男孩的互动剪辑:坐下来看或采取控制

> 原文：<https://hackaday.com/2021/09/21/interactive-clips-for-game-boy-sit-back-and-watch-or-take-control/>

这种情况多长时间发生一次？你发现自己在向某人描述游戏中发生的事情，而他们不确定他们知道你在说地图的哪一部分，或者他们从来没有到那一步。在电子游戏中制作一个书签不是很酷吗？这样你就可以直接跳到游戏的开头，用实际的游戏向你的朋友展示你的意思。

这就是[jol Fran usic]和[Adam Smith]为 Game Boy 提供的精彩[可玩报价背后的想法——剪辑制作创造了一个 4-D 游戏玩法，既可以作为视频观看，也可以在剪辑范围内现场播放。该系统建立在 PyBoy 仿真器的修改版本上。](https://joel.franusic.com/playable_quotes_for_game_boy)

[![Game Boy game ROM -- complete and partial](img/068a8bcdfc279da8835f01de71bf62fc.png)](https://hackaday.com/wp-content/uploads/2021/09/visualized-game-boy-quote.png)

Left: the full game ROM. Right: a bookmarked slice of the game ROM with the rest set to zero.

基本上，一个可玩的报价是由一个保存状态和所有必要的，加上一片游戏的 ROM，其中包括足够的游戏数据来重新创建一个互动剪辑。所有内容都被压缩并隐写编码成一个 PNG 文件。这里有一个你现在就可以玩(或看)的俄罗斯方块的报价——你可能从帖子的缩略图中认出它。[你可以在游戏网站](https://tenmile.quote.games/)上找到其他人，这个网站允许人们创造、分享和建立在彼此的作品上。

在游戏领域之外，这种沉浸式互动工具还可以做更多的事情，我们很高兴看到这种工具的发展方向以及人们用它做什么。

以前没听说过 PyBoy？[让我们给你介绍一下](https://hackaday.com/2020/04/26/snakes-and-ladders-game-boy-emulator-in-python/)。