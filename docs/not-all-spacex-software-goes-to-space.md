# 不是所有的 SpaceX 软件都去太空

> 原文：<https://hackaday.com/2021/06/01/not-all-spacex-software-goes-to-space/>

SpaceX 一直愿意打破航天传统，如果他们觉得有更务实的解决方案。今天，这一点在他们的星舰开发设施中使用起重机等标准建筑设备时最为明显。但是在我们看不到的他们的软件部分中也可以找到同样的解决问题的焦点。最近我们在幕后得到了两种不同的观点。首先，StackOverflow 博客发布了一个关于“[太空中的软件](https://stackoverflow.blog/tag/software-in-space/)的四集系列，紧接着 SpaceX Reddit 上的[向我提问(AMA)环节](https://www.reddit.com/r/spacex/comments/ncj4vz/we_are_the_spacex_software_team_ask_us_anything)。

有些 StackOverflow 系列涵盖了之前讨论过的内容。主要是在第一部分讨论他们的老爷车猎鹰和龙车，还有一些在[第二部分](https://stackoverflow.blog/2021/05/11/building-a-space-based-isp/)讨论 Starlink 的 beta 程序是[到达越来越多的人](https://hackaday.com/2021/05/24/starlink-a-review-and-some-hacks/)。两人都证实，航天软件必须满足非常严格的要求，并且大多接近金属定制的 C++代码。但是在第三部分中，我们收到了令人着迷的新信息，它关注于代码验证和测试。在这里，他们利用了许多开源基础设施，这在软件初创公司中比在航空航天公司中更常见。本系列的第四个也是最后一个组成部分[涵盖了支持 SpaceX 硬件制造的软件，这在此之前很少讨论。(不幸的是，没有任何关于 SpaceX 软件开发人员从 StackOverflow 复制和粘贴代码的频率的信息。)](https://stackoverflow.blog/2021/05/13/building-the-software-that-helps-build-spacex/)

最近的 Reddit AMA 同样与一年前的 SpaceX 软件 AMA 有一些重叠，但在过去的一年中有关于 SpaceX 工作的新信息。有船员龙从测试过渡到业务车辆，以及前面提到的星舰发展计划。我们的评论部分对触摸屏界面在真实航天器中的实用性进行了大量讨论，在这里我们了解到 SpaceX 为构建一些实用有效的东西进行了大量研究。

> 它还向我们展示了本质上每一部科幻电影的界面都是不现实的，在极端条件下是不可读的。

在这个研究过程中，他们学到了很多关于虚拟触摸界面的陷阱。公平地说，电影和电视中的飞船用户界面更关心的是看起来酷而不是有用。

如果你不喜欢标准的 AMA 格式，其中一名投稿人将所有 SpaceX 的答案及其相关问题[以更易读的形式编辑在这里](https://www.reddit.com/r/spacex/comments/nd9ipw/summary_of_spacex_software_ama/)。尽管这些活动明显有招募的一面，但我们很高兴了解到 SpaceX 如何继续专注于完成工作，而不是严格遵循航空航天传统。这种态度可以追溯到[这家公司](https://hackaday.com/2020/06/13/blow-dryers-and-metal-shears-hacks-of-early-falcon-9-flights/)成立之初。