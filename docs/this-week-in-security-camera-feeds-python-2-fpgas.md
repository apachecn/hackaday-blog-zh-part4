# 本周安全:摄像头馈送、Python 2、FPGAs

> 原文：<https://hackaday.com/2020/01/10/this-week-in-security-camera-feeds-python-2-fpgas/>

网络摄像机不断制造新闻，而且不是以最好的方式。首先是用于令人毛骨悚然的恶作剧的泄露的戒指账户，现在是小米的[陈旧的缓存向陌生人发送相机图像](https://www.androidpolice.com/2020/01/06/uh-oh-xiaomi-camera-feed-showing-random-homes-on-a-google-nest-hub-including-still-images-of-sleeping-people/)！不难想象这种缺陷是如何发生的:小米为了与谷歌的 Hub 服务集成，进行了一些视频馈送转码。当转码槽从一台摄像机重新分配到另一台摄像机时，旧数据会保留在缓冲区中，直到被新摄像机的输入替换。根本原因大概和一些 3D 游戏启动时显示的随机画面一样。

### 蟒蛇死了，蟒蛇万岁

[Python 2 终于走到了生命的尽头](https://www.python.org/doc/sunset-python-2/)。虽然这种变化有很多影响，但是安全考虑也很重要。Python 2 环境将不再接收更新，即使发现了严重的安全漏洞。在一种语言中多久会发现一个安全漏洞？也许不经常，但影响可能是深远的。就拿[这个 2016 年 zipimport](https://www.openwall.com/lists/oss-security/2016/06/16/1) 的 bug 来说吧。它无法清理正在处理的 ZIP 文件的文件头，导致了所有预期的问题。

由于 Python2 的持续流行和使用，很有可能会有第三方介入并接管该语言的维护工作，本质上就是派生 Python。除非发生这样的事件，否则绝对是时候远离 Python2 了。

### FPGAs 加速内存攻击

某些商业部门一直在推动更高的性能，因此，英特尔已经开始发运具有 FPGA 协处理器的服务器。这些 FPGAs 可以直接访问系统存储器，并且可以以非常高的数据速率工作。这种集成会导致不可预见的安全问题吗？

一组研究人员已经确定了至少一个这样的问题:手提钻。是的，这是漏洞的另一个别出心裁的名字。这实质上是从 FPGA 发起的 Rowhammer 攻击。在最好的情况下，他们证明了攻击速度是单个 CPU 的三倍。

### 特斯拉黑客

本周，对特斯拉 Model S WiFi 堆栈的一次非常详细的攻击引起了我的注意。由腾讯敏锐安全实验室发布，这是一个非常令人印象深刻的如何在车辆核心损害 Linux 系统的演练。

它首先将特斯拉与它连接的无线网络断开，并捕捉重新连接。有了收集到的信息，就可以对 WiFi 芯片本身发起攻击。一旦遭到破坏，Linux wifi 驱动程序中的漏洞就会被触发，从而在该系统上获得执行权限。值得一问的是，有多少驱动程序是为了防御他们支持的芯片而编写的？整个报道令人印象深刻，去读完整本吧。

### 零零碎碎的东西

抖音目前在年轻人中风靡一时。Checkpoint Research 的人决定看看应用程序和基础设施，[发现了一些漏洞](https://research.checkpoint.com/2020/tik-or-tok-is-tiktok-secure-enough/)。

思科公布了又一轮安全漏洞。它充满了像静态共享密钥和硬编码凭证这样的缺陷。

Firefox 发布了一个意想不到的点版本，仅比预定的版本晚了一天。 [72.0.1](https://www.mozilla.org/en-US/security/advisories/mfsa2020-03/) 为响应 0 天被主动剥削而被推出。除了 Mozilla 声明这是一个类型混淆错误之外，人们对这个漏洞还知之甚少。