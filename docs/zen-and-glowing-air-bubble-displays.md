# 禅和发光气泡显示器

> 原文：<https://hackaday.com/2023/01/04/zen-and-glowing-air-bubble-displays/>

当你在一个媒介中工作足够长的时间，你越来越深入地了解它是如何工作的，你最终会成为它的主人。【枝野幸男】大概是[LED 气泡显示屏](https://hackaday.io/project/188229-glowing-air-bubble-3d-display)的大师。

早在 1994 年，她就有了一个想法，用水柱和一排螺线管来注入空气，在气泡中形成图案。随着时间的推移，她开始意识到这些作品，首先是在水中，然后改用甘油来制作更慢、更可预测、更球形的气泡。29 年后，最新的版本实现了她的最初设想，用 8×8 的喷嘴阵列在缓慢上升的圆柱中制造 3D 形状。

为了感受增量过程的不同阶段，你真的应该观看所有的视频，水中的[版本 1](https://youtu.be/wpaDbDAH25U)、甘油中的[版本 2](https://youtu.be/hw06hDYq7kQ)、带有字体和 FFT 模式的[版本 3](https://youtu.be/hbAsAEsmHuo)，以及最后嵌入下面的 3D 版本 4[。](https://www.youtube.com/watch?v=f_nGCs4pkUM)

理论上看起来很简单:及时向液体中注入气泡，你就能得到图案。但这里的细节包括每个气泡用单独的管子，以防止它们相互作用，并仔细注意时间。事实上，气泡时钟必须不断调整自己，以考虑甘油的粘度，在这个视频演示中，甘油的粘度随温度变化。方便的是，通用 DS3231 时钟模块还内置了一个温度传感器，这一切都是代码问题。

螺线管的轻轻点击让人想起了翻转点显示，但气泡的缓慢上升更令人沉思。虽然后来的模型的精度令人钦佩，但我们肯定也喜欢水版本的跳跃效果，当一个新的气泡被引入，气压进入新的环境。有趣的东西！

这是我们看到的第一次气泡表演吗？绝不可能。而且不是[最大的](https://hackaday.com/2014/08/14/bubble-displays-are-increasing-in-resolution/)或者[最简单的](https://hackaday.com/2018/11/30/air-bubble-characters-float-along-this-unique-scrolling-display/)。但就我们而言，它是最精致、最放松、最进化的运动之一。但我们不得不承认，我们也期待着第 5 版。下一步是什么？

 [https://www.youtube.com/embed/f_nGCs4pkUM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/f_nGCs4pkUM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

