# 旁道攻击将电源变成扬声器

> 原文：<https://hackaday.com/2020/05/11/side-channel-attack-turns-power-supply-into-speakers/>

如果你在一个安全的地方工作，那里的任何一台电脑都很有可能被拆成最少的外围设备。毕竟，一台计算机的部件越少，能变成突破空气间隙的传感器的东西就越少，对吗？所以没有打印机，没有照相机，没有麦克风，当然也没有扬声器。

不幸的是，当[Mordechai Guri]能够将计算机电源变成扬声器从空气隙机器中泄漏数据时，删除这些外围设备对你没有什么好处。在[的一篇 arXiv 论文](https://arxiv.org/pdf/2005.00395.pdf) (PDF 链接)中，【Guri】描述了一种相当迂回和复杂的旁道攻击，他称之为 POWER-supply。这是一种双管齐下的攻击，需要利用发射器和接收器来实现它。通过标准方法传送的发送器恶意软件在气隙机器上运行，并控制 CPU 的工作负载。功率使用的这些变化导致大多数电脑常见的开关模式电源的振动，尤其是变压器和电容器。由此产生的音频信号被智能手机上感染了恶意软件的接收器接收到，可能是被某人带到了气隙机器附近。数据被手机的麦克风接收、缓冲，并在稍后泄露给攻击者。

是的，这很复杂，需要两个漏洞来安装所有的部分，但在正确的条件下，这是可行的。谁敢说接收器恶意软件不能被旧的薯片袋漏洞攻击所取代？无论如何，我们很高兴[Mordechai]和他的安全研究员同事们正在寻找弱点，挑战什么是安全的，什么是易受攻击的假设。

 [https://www.youtube.com/embed/VTTq-wBFu-o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/VTTq-wBFu-o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[ttl]的提示。