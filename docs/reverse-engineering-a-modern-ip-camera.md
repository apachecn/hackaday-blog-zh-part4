# 对现代 IP 摄像机进行逆向工程

> 原文：<https://hackaday.com/2019/03/28/reverse-engineering-a-modern-ip-camera/>

安全摄像头曾经是模拟设备，反馈到满是小屏幕和商业级录像机的房间。随着技术的进步，IP 摄像机开始激增。早期的模型只是向本地网络提供一个视频流和配置页面。然而，针对国内市场的现代车型有所不同。更多时候是通过陌生的智能手机 app 进行配置，通过第三方服务器访问视频。这一切都有点模糊，所以[亚历克斯]决定在引擎盖下看一看。

探索从外部开始，由[Alex]用 Wireshark 捕获发送到摄像机和从摄像机接收的数据。立刻，红旗升起。出于未知的原因，摄像头试图通过 DNS 解析谷歌、脸书和阿里巴巴的服务器。然后拆卸，揭示了一个根访问串行终端是可用的。[Alex]用它来探测周围，发现固件更新脚本和解密所述更新的方法。

因此，这项工作是一个很好的例子，说明了如何从基本原则着手破解一个给定的设备。总的目标是找到一种方法来完全控制摄像头，重新编程以按照(亚历克斯)的意愿提供视频，而不是向远处的第三方服务器提供视频。这不是我们第一次看到 IP 摄像头被黑，我们怀疑这将是最后一次。如果你已经破解了一个，[一定要让我们知道。](http://hackaday.com/submit-a-tip)