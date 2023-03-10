# 喷涂阴极射线管的曲线描绘

> 原文：<https://hackaday.com/2019/02/24/curve-tracing-on-spray-painted-crts/>

当两个正弦波分别标绘在它们各自的 X 轴和 Y 轴上时，就形成了李萨如曲线。你可以使用示波器和几个信号发生器看到一个，如果你玩那些“在沙子里追踪的钟摆”玩具，或者如果你真的需要一些科学的东西来装饰你的家庭，你可以用一个拆卸的 CRT 来追踪它们。这就是[Emily] [对 LissaJukebox](https://hackaday.io/project/163565-lissajukebox-aka-dedicated-lissajous-machine) 所做的。它追踪曲线。不，这不是一个曲线跟踪器，这完全是另一个工具

如果你要把曲线放在 CRT 上，你显然需要一个 CRT，而且它需要看起来很好。有几个选择，从旧的示波管，在旧的 VHS 摄像机中发现的阴极射线管，到更容易驱动的微小静电管。为了这个建筑，[艾米丽]选择了一台老式的普通黑白电视机。但是屏幕是绿色的，对吗？是的，但是如果你小心地遮住阴极射线管，买一些彩色玻璃喷漆，阴极射线管可以是你想要的任何颜色。除了紫色，紫色的彩色玻璃喷漆不知什么原因没用。

为了生成各种函数，[Emily]使用了 XR2206 函数生成器，在亚马逊、易贝和其他各种在线零售商上以套件形式出售，价格低廉。其中一个信号发生器控制 X 轴，另一个控制 Y 轴，这两个信号发生器都馈入一个 15 瓦的立体声放大器板，以驱动 CRT 中的偏转线圈。如果你在家跟着，是的，这是危险的。不要碰 CRT，否则它会使你的心脏停止跳动。我们这些心如煤黑的人是安全的。

需要做一些修改，将 XR2206 函数发生器“工具包”变成对这个项目更有用的东西。通孔电位计被面板安装电位计取代，范围/振幅设置现在由旋转开关控制。

有用吗？嗯，实际上，如果你正在为一个电视节目搭建布景，你需要一些看起来“科学”的东西，LissaJukebox 应该正合你的胃口。除此之外，它看起来很漂亮，我们现在知道有一种喷漆可以把你的旧的，无聊的黑白 CRT 变成一种辉煌的琥珀色荧光粉。没有比这更好的了。