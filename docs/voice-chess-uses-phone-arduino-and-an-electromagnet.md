# 语音象棋使用电话、Arduino 和电磁铁

> 原文：<https://hackaday.com/2019/08/30/voice-chess-uses-phone-arduino-and-an-electromagnet/>

【Diyguypt】可能是一个利他主义者，为不会操纵棋子的人提供了玩游戏的手段。或者他可能只是双手忙于食物和饮料而没有时间玩耍。无论哪种方式，他的[语音命令棋盘](https://www.instructables.com/id/Voice-chess-a-Chess-Board-With-Voice-Commands-1/)似乎都能工作，尽管它有许多象征性和字面上的移动部件。你可以看看下面的视频，看看它是如何工作的。

语音部分由安卓手机处理，使用谷歌的语音服务，所以如果你不想让谷歌听到你最新的开场白，你会想放弃这个。这款手机使用一个通过蓝牙与 Arduino 对话的应用程序，这意味着 Arduino 需要一个蓝牙模块。

Arduino 控制着倒置的 3D 打印机。该装置不是热端朝下，而是有一个朝上的电磁铁。每个棋子底部都有一个小垫圈，使其容易受到磁铁运动的影响。在移动到新的位置之前，电磁铁需要释放一个工件。有可能一个小的伺服移动一个永久磁铁靠近电路板移动和远离电路板重新定位可以做同样的工作，虽然我们怀疑这可能是棘手的。

我们以前见过这种情况，通常以哈利波特为主题。我们有点喜欢一个更[明显的象棋机器人](https://hackaday.com/blog/page/2/?s=chess)，但那只是我们。

 [https://www.youtube.com/embed/odIh5PzQ_sc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/odIh5PzQ_sc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

