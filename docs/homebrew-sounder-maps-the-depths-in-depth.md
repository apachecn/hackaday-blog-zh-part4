# 自制测深仪绘制深度图

> 原文：<https://hackaday.com/2021/09/06/homebrew-sounder-maps-the-depths-in-depth/>

对于那些喜欢在船上闲逛的人来说，有足够多的事情要担心，而不用担心你是否会搁浅。除了根据图表向你展示底下到底有什么之外，真的没有办法知道。但是，在没有这种图表的地方，人们该做些什么呢？简单— [自制水深记录仪](https://github.com/Neumi/3D_water_depth_logger)。

令人欣慰的是，一等兵手动布置测深绳并报出海底深度的日子已经一去不复返了。[Neumi]的探测设备使用现成的声纳测深仪，一个与 NMEA，或国家海洋电子协会，输出。结合 GPS 模块和带有 SD 卡的 Arduino，该设备不仅可以跟踪其下方有多少水，还可以准确地跟踪测量点的位置。整件事情被装配到一个充气橡皮艇上，让它在一个小码头的范围内缓慢往返，在角落和缝隙中工作。一点点 Python 和 matplotlib 将这些数据拼接成一幅港口水深图，细节非常精细。该图表还考虑了潮汐，因为水位在收集所有数据的四个小时内变化很大。在视频中看到它在跳跃之后的动作。

揭示深海的奥秘是一件很酷的事情，即使它们并不那么深。想再深入一点吗？我们以前也见过这种情况。

 [https://www.youtube.com/embed/nWLPmjaNJ6I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/nWLPmjaNJ6I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

