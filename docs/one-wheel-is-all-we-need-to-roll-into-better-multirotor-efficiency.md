# 我们只需要一个轮子就能实现更好的多旋翼效率

> 原文：<https://hackaday.com/2020/11/07/one-wheel-is-all-we-need-to-roll-into-better-multirotor-efficiency/>

多旋翼飞机享有许多固有的优势，但作为用蛮力对抗重力的机器，能效并不在考虑之列。为了扩大射程，已经探索了几种空地混合设计。飞行汽车基本上是在地面上行驶，而不是必须在空中行驶。但它们都面临着同样的挑战:使汽车在地面上工作良好的组件在空中时会消耗里程。[秦有明等]探索尽可能减少自重，提出了 [*单被动轮空地混合动力*](https://arxiv.org/abs/2003.09242) 。

正如论文的标题所表明的那样，他们在这个设计中完全采用了极简主义。传动轴、刹车、方向盘甚至其他车轮都不见了。剩下的只是一个无动力的轮子栓在他们的双旋翼飞行器的底部。最小化对飞行特性的影响是很好的，但是在地面上如何工作呢？作为一个权衡，这些转子必须保持旋转，即使在“地面模式”。他们负责保持机器直立，还必须处理转向等任务。在评估这样一个折衷的地面飞行器是否值得麻烦之前，这些和其他控制算法问题必须被解决。

令人高兴的是，结果是一个响亮的“是”。尽管转子在地面上必须继续运行以完成不同的工作，但这仍然比在空中悬停要省力得多。功耗测量显示节省高达 77%，还有许多潜在的调整空间等待未来的探索。其中之一是更好地理解与地面效应的相互作用，这是我们已经看到的能够实现新颖设计的东西。这不完全是我们承诺的飞行汽车，但它的发展仍将是有趣的，在所有其他正在开发的巧妙想法中[让多旋翼在空中停留更长时间](https://hackaday.com/2019/10/12/flying-batteries-for-drones/)。

[ [IROS 2020 展示视频(时长 10:49)](https://www.iros2020.org/ondemand/episode?id=1000&id2=Aerial%20Systems%20-%20Mechanics%20and%20Control%20II&1604660080105) 需要免费注册，至少在 2020 年 11 月 25 日之前可用。下面嵌入了 42 秒总结]

 [https://www.youtube.com/embed/22SXYY39KjM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/22SXYY39KjM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

