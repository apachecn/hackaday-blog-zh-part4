# 术语 2 是 Siri，就像 1976 年一样

> 原文：<https://hackaday.com/2022/11/23/termi2-is-siri-like-its-1976/>

你长周末有什么计划？如果你没有时间或者不想投入到一个新项目中，为什么不掸掉未完成的东西，或者像 Hackaday 校友(卡梅伦·科沃德)最近做的那样，用新的大脑升级旧的项目。

在这种情况下，这个项目是一个终端打字机——确切地说，是德州仪器的 Silent 700 终端——类似于 70 年代后期的 Siri。终端打字机是一种特殊的机器，它使用声学耦合器发送和接收来自远处主机的哔哔声和哔哔声。Termi 的第一次迭代使用了 Raspberry Pi Zero W 来运行查询 Wolfram Alpha 的脚本，[Cameron]认为在登录要求、引导时间和使其工作所需的奇怪格式之间，必须有更好的方法。

事实证明，更好的方法是使用 ESP32 并读取“串行端口”，这是一个具有两个串行连接的专有端口，一个用于声学耦合器，另一个用于常规串行通信。我们最喜欢这个构建的一点是，不管是大脑，所有的问题和答案都有一个永久的记录。休息后请务必观看视频。

 [https://www.youtube.com/embed/eDkJeqvbM9A?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/eDkJeqvbM9A?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

