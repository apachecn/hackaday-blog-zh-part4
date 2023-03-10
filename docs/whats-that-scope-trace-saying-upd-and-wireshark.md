# 示波器描迹显示什么？UPD 和 Wireshark

> 原文：<https://hackaday.com/2022/08/14/whats-that-scope-trace-saying-upd-and-wireshark/>

像我们许多人一样，Matt Keeter 有许多联网设备和一个示波器。他决定要看看网络上有什么。虽然我们大多数人可能会接触 Wireshark，但他是从 PCB 层开始的。特别是，他让——或者更确切地说，让某人——将一个有源差分探头焊接到一个以太网交换机上。附加的范围是一个 Textronix，但它没有分析仪读取网络数据。然而，他能够捕获 190 多 MB 的数据，并编写了一个简单的解析器来分析从交换机中提取的网络数据。

探测点位于网络交换机和 PHY 之间，后者使用 QSGMII(四路串行千兆位媒体独立接口)将一个编码通道扩展为四个物理连接。顾名思义，这将四个 SGMII 通道挤在一对上。

正如网络方案中常见的那样，8 位字节被编码为 10 位代码组，以确保有足够的位转换来恢复同步时钟。解码软件必须检查流以找到成帧字符，然后与发送的时钟同步。

接下来是对协议和解码它的 Python 代码的一个很好的浏览。这看起来很复杂，但是代码相当短，执行起来也很快。产量？可以用 Wireshark 处理的 Pcap 文件。总的来说，这是一篇很棒的分析。他还指出，已经有其他工具可以用来做这种解码工作，但是这有什么意思呢？

Wireshark 可以做许多不同种类的分析，即使你通常不从示波器捕捉。如果你知道正确的密钥，你甚至可以[解密 SSL](https://hackaday.com/2022/03/22/wireshark-https-decryption/) 。