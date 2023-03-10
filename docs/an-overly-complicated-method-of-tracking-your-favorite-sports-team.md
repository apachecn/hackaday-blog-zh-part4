# 一种过于复杂的追踪你最喜欢的运动队的方法

> 原文：<https://hackaday.com/2021/12/04/an-overly-complicated-method-of-tracking-your-favorite-sports-team/>

世界的大部分似乎都围绕着体育运动，而体育运动跟踪是一项相当大的业务。那么大家是怎么跟上自己喜欢的球队的呢？嗯，[杰克逊]和[莫拉德]决定[设计一个定制的物联网解决方案](https://www.hackster.io/434778/charlotte-football-record-tracker-020abb)。

他们的系统有点复杂，所以请原谅我们。首先，他们告诉 Alexa 这一周球队是赢是输。Alexa 然后将这些信息发送到 IFTTT，在 if TTT 中，两个不同的粒子氩板不断轮询结果，以决定下一步如何做出反应。一个粒子的反应是点亮一个 LED，绿色代表胜利，红色代表失败。另一个粒子板在 LCD 屏幕上显示结果。但这就是事情变得棘手的地方。他们的设计中更令人困惑的一个方面是一个粒子板，然后向 IFTTT 发送信号，告诉它记录输赢的次数。这似乎有点绕弯，因为该系统最初是从 IFTTT 开始的。不管怎样，他们似乎对结果很满意，我相信他们在这个过程中学到了一些东西。

这个项目可能不会满足任何功能需求，因为 [Alexa 已经知道了我们生活中的一切](https://hackaday.com/2016/12/28/police-want-alexa-data-people-begin-to-realize-its-listening/)，你可以随时问她你最喜欢的球队怎么样了。但是，嘿，我们都是[在 Hackaday 这里](https://hackaday.com/2021/08/24/fail-of-the-week-learning-how-not-to-silver-solder/)边做边学[我们都为到处建造无用的项目](https://hackaday.com/2021/03/03/complicated-and-useless-cancel-each-other-out/)而感到内疚，只是因为我们可以。在任何情况下，他们的项目都可以作为一个很好的介绍，将你的粒子与 IFTTT 或 Alexa 集成，因为这里似乎有很多可能不必要的握手。

 [https://www.youtube.com/embed/xyL4TCmMPRk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/xyL4TCmMPRk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

