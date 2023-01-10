# 自动棋盘游戏

> 原文：<https://hackaday.com/2022/03/04/automated-chess-board-plays-you/>

如果你曾经玩过国际象棋，甚至跳棋，你可能会考虑做一个棋盘，让计算机不用输入你的走法，也不用看着屏幕上的棋盘就能和你下棋。他不仅想到了它，而且还建造了它。

该板看起来很棒，并使用泡沫板，这使得它很容易复制。每个棋子内部都有一个小磁铁，XY 运动系统上的电磁铁可以选择性地拾取和移动棋子。此外，每个方块下面的簧片开关可以判断一个方块是否被占用。

这个系统很简单，但是很有效。毕竟，你知道棋子在开始时的位置。所以如果一个主教离开一个方块，一个新的方块得到一块，你可以假设它是主教。实际上不需要区分碎片。

一个液晶显示器和一些按钮就像一个象棋时钟，如果一步棋是非法的，它就会记录下来。Arduino 有一个非常基本的象棋算法，称为运行在 Arduino 上的 Micro Max，但我们想知道你是否可以连接到远程计算机来获得更复杂的游戏，甚至连接到互联网来玩远程人类，这是我们在之前见过的[。你甚至可以将它用于其他的](https://hackaday.com/2021/06/10/automatic-chessboard-lets-online-players-move-the-pieces/)[输入法](https://hackaday.com/2019/08/30/voice-chess-uses-phone-arduino-and-an-electromagnet/)。

 [https://www.youtube.com/embed/pr_EUNSYxKE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=17&wmode=transparent](https://www.youtube.com/embed/pr_EUNSYxKE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=17&wmode=transparent)

