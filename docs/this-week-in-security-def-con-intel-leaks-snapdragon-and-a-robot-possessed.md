# 本周安全:国防会议，情报泄露，骁龙，和一个机器人着魔

> 原文：<https://hackaday.com/2020/08/14/this-week-in-security-def-con-intel-leaks-snapdragon-and-a-robot-possessed/>

上周末，DEF CON 举行了他们的“安全模式”会议:整个会议不是在物理场地举行，而是在网上举行。所有的演示都可以在官方的 DEF CON YouTube 频道上看到。我们将在这里介绍一些演讲，并关注 HaD 上的其他文章，这些文章详细介绍了我们感兴趣的其他演讲。


### 开锁

在我们的每周综述中，我们并不经常涉足物理安全，但开锁路线是 DEF CON 的一大部分。这是一个完美的借口。首先是[一个由[Jared Dygert]做的关于保险箱破解](https://www.youtube.com/watch?v=hjT-H_S2XAE)的演讲。你知道电影中的一个场景吗？超级小偷一边转动拨号盘，一边听着声音，打开了保险箱。是啊，算了吧。真正的技术和声音没有任何关系。一个典型的三号码组合保险箱在锁定机构内有三个轮子。每一个轮子上都有一个窄槽，或者说门。当三个门排成一行时，锁杆可以落入槽中，第四个轮子将锁拉开。

第四个轮子是打开保险箱的钥匙，因为锁杆直接骑在轮子的外表面上。那里的门与其他的形状不同，一边有一个弯曲的边缘。可以准确地感觉到锁杆何时开始落入大门。因为那个特殊的第四道门的形状，有可能测量宽度，并通过延伸发现锁杆下降了多远。由于带有未知门的三个轮子的大小并不完全相同，因此可以绘制最大轮子的表面并发现门的位置。如需演示，请观看上面链接的视频。

提到开锁人，很难不大声喊出两个 YouTubers，[【波什尼亚比尔】](https://www.youtube.com/user/bosnianbill)和[【开锁律师】](https://www.youtube.com/channel/UCm9K6rby98W8JigLoZOh6FQ)。本周，我看到了来自这对充满活力的搭档的律师的一段视频，这是我很久以来看到的最礼貌但最野蛮的烧伤。在你观看之前，知道他使用的工具是[麻雀圆盘拨片](https://www.sparrowslockpicks.com/product_p/disc.htm)，他和【波什尼亚比尔】一起设计并测试了这个工具。
 [https://www.youtube.com/embed/NSuaUok-wTY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/NSuaUok-wTY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent) 

### 龙的致命弱点

骁龙处理器在高端 Android 设备中非常受欢迎。这些处理器封装在一个片上系统(SoC)中，实际上包含了许多处理器和设备。骁龙 SoC 具有处理器、GPU、Wifi 调制解调器、图像信号处理器和数字信号处理器。我们经常谈论运行在 CPU 上的软件的安全漏洞。如果我告诉你在其他处理器内核上运行的软件也存在漏洞，会怎么样？是的，很明显也有写得很差的代码。一直不明显的是如何找到这些漏洞，然后如何攻击它们。现在，多亏了安检处的研究人员，以及他们对阿基里斯的研究，我们知道了一种攻击龙的脚跟的方法。

当一个应用程序需要使用骁龙 DSP 时，它会调用一个序列化库，称为`stub.so`文件。数据序列化后，利用 DSRPC 驱动程序通过共享存储器传输到 DSP。除了要处理的数据，应用程序还会发送处理库。这个库本质上是将在 DSP 上运行的程序。有一个代码签名要求。DSP 将只运行高通签名的代码，但没有版本检查或撤销机制。本质上，高通签署的任何 DSP 库都可以在任何 DSP 上运行。更糟糕的是，Android 应用程序可以在没有特殊权限的情况下访问 DSP。即使只创建了一个易受攻击的 DSP 库，弱代码签名方案也意味着每个高通 DSP 都是易受攻击的。

一些文章表明，从网上下载的恶意视频或音频文件会触发该漏洞。这是不正确的。到目前为止，只有直接访问 DSP 的应用程序才能发起攻击。在周四的虚拟新闻发布会上，一位检查站研究员谈到了这一点。虽然理论上视频文件有可能触发一个尚未发现的漏洞，但他们发现的缺陷是一个反序列化错误，只有恶意序列化过程才会触发。这意味着使用官方序列化过程处理的数据不会触发此漏洞。反序列化错误实际上源于分发给 OEM 并用于构建单独库的软件开发工具包。简单来说，不仅仅是一两个 DSP 库存在漏洞，而是全部，这就是“400 漏洞”的来源。

一旦恶意应用利用漏洞打破反序列化例程，实现代码执行，接下来会怎样？高通至少做了适当的用户/内核分离，还需要一个额外的漏洞来升级权限，直到完全妥协。一旦出现这种情况，主要威胁就是数据泄露。DSP 上的恶意软件可以检查其他应用程序共享进行处理的所有数据。这可能意味着完全访问设备的麦克风，并可能在使用时使用摄像头。我可以问 Checkpoint 他们是否已经成功地永久修改了 DSP 的固件，因为这种修改甚至可以通过完全的工厂重置而存在。他们的回答是，他们已经调查了这个问题，但无法做出永久性的修改。这并不奇怪，因为这种性质的固件通常不存储在 SoC 本身，而是作为引导过程的一部分从主系统闪存加载。

到目前为止，这组漏洞并没有给日常用户带来巨大的风险。不安装不受信任的应用程序的常规建议仍然是最佳解决方案。这里的主要危险是，DSP 恶意软件可能被已安装的应用程序用来在没有任何权限的情况下访问麦克风音频。修复这些漏洞的过程在未来几年都将是一件令人头疼的事情。不仅需要更新单个易受攻击的库，还需要解决签名问题，这样易受攻击的库就不会被轻易执行。目前似乎没有任何可用的修复程序。

 [https://www.youtube.com/embed/CrLJ29quZY8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/CrLJ29quZY8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



为了让你看得开心，下面是 DEF CON 的另一个精彩演讲，其中[Christopher Wade]深入探讨了固件黑客技术，主要是在 Android 设备上。

 [https://www.youtube.com/embed/aLe-xW-Ws4c?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/aLe-xW-Ws4c?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



### 英特尔泄露 20 GB

上周，大量英特尔代码和文档被公之于众。英特尔的官方解释是，合作伙伴或客户一定滥用了他们对英特尔“资源和设计中心”的访问权限，并从那里泄露了文件。然而，根据 ZDnet 的报道，泄密者声称在一个没有正确配置的 CDN 服务器上发现了该文档。

不管怎样，泄漏似乎是真实的。时间会告诉我们刚刚发布的 20 GB 中包含了哪些有趣的花絮。由于这些信息都被标记为机密，所以对于程序员可以用这些信息做什么，存在一点法律上的灰色地带。

### 机器人驱魔人？

最后，为了好玩，McAfee 的研究人员在“temi”电话会议机器人中发现了[一组漏洞。在一篇令人惊讶的详细报道中，他们描述了攻击者如何在没有任何有效凭证的情况下拥有机器人，用它来驾驶机器人并监视附近的任何东西。McAfee 的研究人员已经与 temi 的供应商分享了他们的所有发现，并且修复程序已经可用。](https://www.mcafee.com/blogs/other-blogs/mcafee-labs/call-an-exorcist-my-robots-possessed/)