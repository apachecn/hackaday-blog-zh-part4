# 在家放松一下，参加一个网络即兴表演

> 原文：<https://hackaday.com/2020/08/26/slack-off-from-home-with-a-networked-jam-session/>

那些在疫情之前经常在办公室工作的人:你一点都不怀念和同事在一起的日子吗？也许只有几个？通过聊天窗口或视频会议，你只能享受到有限的乐趣。即使你们碰巧都是准备好了乐器的音乐家，你们的即兴演奏也可能会因为延迟问题而变得糟糕。

[Eden Bar-Tov]和一些同学有一个打破在家工作单调的更好的主意——一个为 2020 年及以后建造的协作测序仪。不是每个人都一次按下按钮，然后期待最好的结果，而是这个团队轮流创造一个旋律。开始的时候给每个人随机分配一个乐器，第一个去的负责打下节拍。

每个音乐盒内都有一个 ESP8266，它通过 MQTT 与节点服务器通信，以一串数字的形式发送每个旋律。在每个人的回合开始之前，LED 矩阵显示三秒倒计时，然后滚动歌曲的当前状态。当边缘的 LED 灯变得疯狂时，你的回合就结束了。

如果你不知道自己在做什么，音乐可能会令人沮丧，但这种乐器是为非音乐家设计的。只有五个可能的音符可以演奏，而且它们总是来自同一个音阶以避免不和谐。循环总是在 4/4，这使得事情变得容易。玩家甚至不用担心停留在时间上，因为他们的贡献会自动与节拍匹配。休息之后来看看。

厌倦了整天坐在室内，却还想做音乐？在自行车上安装一个模块合成器，你已经解决了两个问题。

 [https://www.youtube.com/embed/ZrzRNx4XE8Y?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ZrzRNx4XE8Y?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

