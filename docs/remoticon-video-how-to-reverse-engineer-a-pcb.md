# Remoticon 视频:如何对 PCB 进行逆向工程

> 原文：<https://hackaday.com/2020/12/01/remoticon-video-how-to-reverse-engineer-a-pcb/>

你手里拿着一个不是你做的产品的电路板。这东西是怎么工作的？这是一个多么令人畏惧的问题，但是如果你知道自己在做什么，这是可以解决的，也是可以接近的。好消息是 Eric Schlaepfer 确切地知道他在做什么，并且[将反向工程印刷电路板的过程浓缩到这个优秀的车间](https://www.youtube.com/watch?v=dQ9Mh9BbyP0)。它是在 2020 年黑客日 Remoticon 期间现场展示的，编辑过的视频，你可以在下面找到，刚刚发布。演讲的幻灯片已经发布在[研讨会项目页面](https://hackaday.io/project/175076-remoticon-pcb-reverse-engineering)上。

需要证明他有我们都想要的技能吗？去年，埃里克成功地对传说中的声霸声卡进行了逆向工程，并生产出了他自己的全功能嵌入式替代产品，名为 Snark Barker。然后[重新设计它，使其与古老的 MCA 总线架构](https://hackaday.com/?p=450317)一起工作。哇哦。

 [https://www.youtube.com/embed/dQ9Mh9BbyP0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/dQ9Mh9BbyP0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



Eric 分两部分应对挑战。首先是通过收集尽可能多的信息来生成物料清单，然后通过自由使用搜索引擎和数据表来填充其余的细节。他把所有的东西都放进一个电子表格里，每一栏都是印在板上的零件名称(U1、R53、C4 等)。)、封装类型(您可以通过经验了解这一点)、topmark(印在零件上)以及从上面收集的零件号。

下一步是通过拍摄高分辨率图像对电路板本身进行逆向工程，有时会为此从电路板上移除一些部件，以及一个原理图，其中包含您在第一步中注意到的每个部件，但没有连接的走线。Eric 演示了如何使用 GIMP image editor 绘制轨迹，当他开始解决拼图时，在原理图中添加网络。当他在自己的层上绘制轨迹时，在棋盘图像之间来回切换立即开始揭开两层之间的连接。

他当然让它看起来既快又容易，对他来说也是如此。关键是在你能依靠经验解开症结之前，先掌握一些这样的方法。但无论这是你的第一次牛仔竞技表演，或者你是一个经验丰富的老手，有条不紊的方法是令人钦佩的，也是每个人的技能组合中受欢迎的一部分。

作为一个即兴的评论，埃里克提到他可以就变形金刚做一个小时的演讲。是的，请！Eric 在他的 Twitter 账户 [@TubeTimeUS](https://twitter.com/TubeTimeUS) 上以深入探究工程话题而闻名，我最喜欢的一些是[他解开营火大陪审团报告](https://twitter.com/TubeTimeUS/status/1306359385656946688)，我们在 9 月曾报道过[，以及](https://hackaday.com/2020/09/17/closely-examining-how-a-pge-transmission-line-claimed-85-lives-in-the-2018-camp-fire/)[一个专利巨魔如何打倒准将](https://twitter.com/TubeTimeUS/status/1317930223816429568)的故事。他也是团队中的一员，展示了最好的集成电路演示之一，以真正理解硅是如何让世界运转的。