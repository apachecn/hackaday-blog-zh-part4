# 显示 HTML 界面和管理网络节点…在太空中！

> 原文：<https://hackaday.com/2020/06/08/displaying-html-interfaces-and-managing-network-nodes-in-space/>

SpaceX Crew Dragon 上的触摸屏界面只是它与过去太空飞行器的众多差异之一，但这些大屏幕产生了巨大的视觉冲击。仪表上布满指针的面板，或者数不清的拨动开关都不见了。它看起来很像日常平板电脑上的网络交互，这是有充分理由的:我们看到的是由谷歌 Chrome 浏览器底层的相同软件核心呈现的 HTML 和 JavaScript。这一点和许多其他细节都包含在与 SpaceX 软件团队成员的 Reddit[*问我任何事情*](https://www.reddit.com/r/spacex/comments/gxb7j1/we_are_the_spacex_software_team_ask_us_anything/)*中。*

 *在这种背景下，各种渠道都提到了铬，但没有回答明显的后续问题:铬有多深？在这部《AMA》中，我们了解到它一点也不深入。Chromium 只是 UI 渲染引擎，他们的容错飞行软件交互在别处。Chromium 等组件被隔离，以帮助保持系统行为的可预测性，因此一个冻结的标签不会使胶囊崩溃。有点令人惊讶的是，他们没有使用专门的实时操作系统，而是用 [PREEMPT_RT 补丁](https://rt.wiki.kernel.org/index.php/Main_Page)构建的轻度定制的 Linux，以获得更好的实时行为。

除了猎鹰火箭和龙太空舱，这个 AMA 还涵盖了 Starlink 的软件工作，在设计权衡中提供了有趣的对比。因为有如此多的卫星(甚至更多正在发射的卫星)，单个航天器的损失不是任务失败。这给了他们快速迭代的空间，将星座更像数据中心的服务器机架，而不是典型的卫星操作。在船员龙代码被冻结了几个月的地方，Starlink 代码更新很快。很快，当新发射的 Starlink 卫星到达轨道时，它们的代码通常已经落后于星座的其他部分。

最后，在空间约束代码之外还有一些零散的答案。他们的地面支持显示器(可见于霍桑任务控制室)是用 LabVIEW 构建的。他们还证实，与一些说法相反， [SpaceX ISS 对接模拟器](https://hackaday.com/2020/05/15/docking-with-iss-isnt-as-easy-as-you-might-think/)实际上并没有运行与 Crew Dragon 相同的代码。啊好吧。

任何对为太空编写软件感兴趣的人都会喜欢阅读 AMA 中的这些和其他细节。由于它有一个方便的副作用，即作为一个招聘活动，如果有人有加入该团队的雄心，就会收到大量的申请邀请。我们当然不能否认帮助书写人类太空飞行下一章[的吸引力。](https://hackaday.com/2020/06/01/nasas-long-delayed-return-to-human-spaceflight/)

[图片来源: [SpaceX](https://www.flickr.com/photos/spacex/49927519643/)*