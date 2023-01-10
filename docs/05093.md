# 定制的 Nixies 在高达 100，000 赫兹的频率下运行

> 原文：<https://hackaday.com/2019/12/12/custom-nixies-perform-when-cranked-up-to-100000-hertz/>

随着谢妮钟的流行，我们认为发光管只适合变化缓慢的应用是情有可原的。但我们忘记了，在它们成为业余爱好者的必备配件之前，Nixies 被用于各种科学仪器，从频率计数器到精密万用表。在这样的应用中，数百或数千赫兹的更新速率并不罕见，而不起眼的谢妮可以轻松处理显示刷新。

但是刷新 100 千赫的谢妮怎么办？这是一位客户向[手工谢妮制造商【Dali bor farn】](https://hackaday.com/2016/10/04/the-art-of-making-a-nixie-tube/)提出的问题，他想要一个计时器来校准高速摄像机。这是一个壮举，[Dalibor]不确定他的定制管可以处理。下面的视频展示了他努力寻找答案的过程。

如果你曾经想了解像谢妮这样的气体放电显示器的物理特性，从 5:13 开始的 15 分钟将会给你所需要的一切。这个基本问题可以归结为受激氖的半衰期，或者受激分子的一半需要多长时间才能回到基态。这反过来决定了特定阴极在关闭后将持续发光多长时间，从而决定了有多少位数字将同时发光。

为了回答这个问题，他们与布拉格的一家公司合作，使用了一台每秒能拍摄 90 万帧的摄像机。即使他们发现每个阴极都有很长的余辉时间，即使在 100 kHz 的频率下，也很清楚哪个数字是当前被照亮的。他们还观察了在寒冷的谢妮和温暖的环境中数字的启动，在 26:30 左右产生了一些有趣的镜头。

我们欣赏[Dalibor]对细节的关注，不仅体现在他的定制电子管的工艺上，还体现在确保它们能完成工作上。他最近对他的一些高端钟表做了一次失败分析，显示了对他的产品和品牌的同样关注。

 [https://www.youtube.com/embed/TK3E55fytC0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/TK3E55fytC0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[Chris Muncy]的提示。