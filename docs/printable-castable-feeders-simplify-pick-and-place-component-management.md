# 可印刷、可浇铸的进料器简化了取放元件管理

> 原文：<https://hackaday.com/2020/05/14/printable-castable-feeders-simplify-pick-and-place-component-management/>

不用说，我们喜欢看到人们想出的所有聪明的方法来填充他们的印刷电路板，尤其是自动化的解决方案。手动拾取和放置接近微观的元件的想法足以成为在商店中添加拾取和放置的理由，但这通常会将馈送元件的问题留给用户的想象。[这款可量产的无源元件进料器](https://github.com/dining-philosopher/litefeeder)就是这种想象的一个很好的例子。

我们见过的几乎所有自制 PnP 元件进料器的设计都有两个共同点:它们是 [3D 打印的](https://hackaday.com/2019/11/07/3d-printed-magazines-tame-the-smd-tape-beast/)，或者它们是[有点复杂的](https://hackaday.com/2018/02/09/custom-parts-feeder-aims-to-keep-pace-with-pick-and-place/)。并不是说这些都是不好的事情，但它们确实提出了问题。即使是一个中等规模的项目，打印足够多的送纸器也要花很长时间，而且送纸器的电机和传感器越多，发生故障的几率就越大。[dining-philosopher]仅使用两个部件的简单设计解决了这两个问题，这两个部件可以用树脂浇铸。杠杆臂被附在 LitePlacer 工具上的柱塞压下，偏移量刚好足以使吸盘与胶带上的元件位置对齐。当工具在拾取零件后离开时，下臂中的棘爪向前移动，与带链轮孔啮合并前进到下一个组件。

[dining-philosopher]在他的版本中没有解决覆盖膜剥离问题，而是选择手动剥离，并使用重物保持拉紧，露出下一个组件。但是在一个很好的合作例子中，[杰德·史密斯]在最初的设计中增加了一个自动剥膜器。这让事情变得有点复杂，但削皮器是由前进的胶带驱动的，所以它可能是值得的。

 [https://www.youtube.com/embed/S1jxeCK4YC0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/S1jxeCK4YC0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

