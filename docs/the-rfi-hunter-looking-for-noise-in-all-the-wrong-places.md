# RFI 猎人:在所有错误的地方寻找噪音

> 原文：<https://hackaday.com/2020/01/15/the-rfi-hunter-looking-for-noise-in-all-the-wrong-places/>

下次你拿到一个新设备，兴奋地打开它的塑料包装的小电源时，记住这一点:你每插上一个开关模式电源，一个业余无线电操作员就会流下一滴眼泪。一个嘈杂的，宽带，充满谐波的眼泪。

这一事实对您的干扰程度很大程度上取决于您在麦克风的哪一边，但射频干扰(RFI)是我们至少都应该知道的事情。[Josh (KI6NAZ)]在他的火腿小屋中敏锐地意识到 RFI，但他没有诅咒不断上升的噪底，而是提出了一些有用的技巧来寻找并消除它——或者至少减少它的影响。

解决这个问题首先要找到 RFI 的来源，为此[Josh]使用了经典的“一次一个电路”的方法——切断面板中的每个断路器，并在接通每个断路器的同时监控噪底。这至少可以让你大致了解家里的违规设备在哪里。从那里，[Josh]使用一个小型短波接收器来定位问题区域，如冰箱、干衣机和他的简易电脑。家庭平板电视也被证明是相当嘈杂的。补救技术包括将每根电源线和电缆缠绕在环形线圈上，或者将铁氧体磁芯夹在它们周围，无论是在违规设备上还是在棚屋里。他甚至在干衣机上加了一个线路过滤器来抑制不必要的干扰。

从他的瀑布表演来看，[Josh]的努力得到了回报，他的噪底从 S5 降到了 S1 左右。糟糕的是，他不得不自己解决问题——毕竟，联邦通信委员会和 T2 的其他频谱监管机构并不知道存在问题。

 [https://www.youtube.com/embed/QQzmMOJvFfc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/QQzmMOJvFfc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

