# 用电传打字机发短信

> 原文：<https://hackaday.com/2019/04/23/texting-with-a-teletype/>

你如何让孩子们对旧技术感兴趣？显然，是通过连接到电话上。那些孩子和他们的手机。当[马雷克]得到一台老式电传打字机时，[他把它连上了 GSM 网络](https://hackaday.io/project/165003-gsm2teletype)，配备了所有的功能，包括一个以令人印象深刻的 50 波特运行的 40mA 电流回路。

这里所说的电传打字机是 70 年代捷克斯洛伐克制造的老式 T100 电传打字机。这是送给[Marek]的工作场所——克拉科夫城市工程博物馆的礼物，这个项目实际上是一个实验，旨在研究将这种电传打字机作为互动展览的可能性，而不是当前环路和电话系统时代的人工制品。

电流回路是或曾经是将电传打字机连接到任何东西的标准方式，所以[Marek]所要做的就是建造一个盒子，将信号从 GSM 调制解调器转换到这个电流回路。对于原型，有问题的微控制器是一个旧的 AT89C2051(因为它是放在零件抽屉里的)。这被转移到 PIC32 微控制器和 SIM800 GSM 模块上。这是一个由两部分组成的外壳，GSM 接口位于外壳的一半，由简单的 DC 电源组成的电流环路发生器位于外壳的另一半。

这个接口能够从键盘向 GSM 网络发送和接收信息，所以理论上你可以用老式的电传打字机给你的朋友发短信。这个功能还没有实现，但是它已经是你能想到的最酷的东西了。你可以看看下面的电传视频。

 [https://www.youtube.com/embed/IXxyjy1meAU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/IXxyjy1meAU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

