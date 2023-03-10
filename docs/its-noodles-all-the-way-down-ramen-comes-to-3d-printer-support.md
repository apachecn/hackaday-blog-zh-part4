# 一路都是面条:拉面来 3D 打印机支持

> 原文：<https://hackaday.com/2021/02/20/its-noodles-all-the-way-down-ramen-comes-to-3d-printer-support/>

虽然拉面支撑听起来像是汤的服务台，但它实际上是[GeoDroidJohn]用来在 3D 打印上获得易于移除的支撑结构的技术。我们看到了下面的视频，我们不得不承认，它确实让我们想起了一块未煮过的拉面。

我们不得不进一步挖掘，找出他是如何做到的。我们终于找到了 Reddit 上的一个帖子，给出了简化 3D 的方法:

*   喷嘴直径/2=层高
*   每隔一层支撑材料，在-45°和 45°处交叉 15%
*   顶部或底部 90% 0 间隙的 5 个密集层。

我们不得不承认，我们尽量避免支持，在我们不能的地方，我们只是选择一个股票 Cura 设置。除了简化 3D 之外，还不完全清楚如何或者是否可以在切片器中复制这一点。当然，层的高度是给定的。我们认为在“线方向”框中[-45，45]的 15%支持密度可能会部分实现。也许某个精通 Simplify 和其他 slicers 的人可以帮助翻译。

无论如何，它确实让我们考虑尝试不同的支持结构。在此之前，我们已经玩过 Cura 的树支架，非常喜欢。所以也许默认并不总是最好的。

我们希望有时间尝试更多我们[读到的关于支架](https://hackaday.com/2020/02/18/everything-you-wanted-to-know-about-3d-printing-support-but-were-afraid-to-ask/)的内容。如果你想试试的话，你也可以在你的[打印机上安装一个记号笔](https://hackaday.com/2020/05/27/improving-3d-printed-supports-with-a-marker/)。

 [https://www.youtube.com/embed/aJ557py3uuE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/aJ557py3uuE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

