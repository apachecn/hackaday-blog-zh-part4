# 本周的安全:VPN 网关、野外攻击、VLC 和 IP 地址诈骗

> 原文：<https://hackaday.com/2019/08/30/this-week-in-security-vpn-gateways-attacks-in-the-wild-vlc-and-an-ip-address-caper/>

我们将从更多的黑帽/DEFCON 新闻开始。Devcore 的[Meh Chang]和[Orange Tsai]查看了 Fortinet 和 Pulse 安全设备，发现了多个漏洞。( [PDF 幻灯片](https://i.blackhat.com/USA-19/Wednesday/us-19-Tsai-Infiltrating-Corporate-Intranet-Like-NSA.pdf))他们正在发布该研究的摘要，[Fortinet 研究的摘要](https://devco.re/blog/2019/08/09/attacking-ssl-vpn-part-2-breaking-the-Fortigate-ssl-vpn/)现已发布。

这…不太好。有多个预认证漏洞，以及似乎是故意的后门。

CVE-2018-13379 滥用在为设备登录页面请求不同语言时发出的`snprintf`调用。`Snprintf`是`sprintf`的替代方案，但是旨在通过包含写入目标缓冲区的最大字符串长度来防止缓冲区溢出，这听起来是个好主意，但是可能会导致恶意截断。

问题中的代码看起来像`snprintf(s, 0x40, "/migadmin/lang/%s.json", lang);`。
当加载登录页面时，请求一个语言文件，并将该文件发送给用户。乍一看，这似乎确实会限制从指定文件夹返回到. json 文件的文件。不幸的是，请求上没有进一步的输入验证，所以一种语言`../../arbitrary`被认为是完全合法的，避开了预期的文件夹。这将泄漏任意的 json 文件，但是因为如果超过指定的长度,`snprintf`不会失败，所以发送一个足够长的阿郎请求会导致。json”扩展也没有附加到请求中。

已经编写了一个 [metasploit 模块](https://packetstormsecurity.com/files/154146/FortiOS-5.6.7-6.0.4-Credential-Disclosure.html)来测试此漏洞，它请求`/../../../..//////////dev/cmdb/sslvpn_websession`的阿郎。这一长度足以迫使 json 扩展名从字符串末尾脱落，Unix 惯例是忽略路径中额外的斜杠。就这样，Fortigate 提供其文件系统上的任何文件，只是为了请求 nice。

比`snprintf`漏洞更令人担忧的是魔力价值似乎是一个有意的后门。作为 http 查询字符串发送的一个简单的 14 个字符的字符串绕过身份验证，并允许更改任何用户的密码—无需任何身份验证。这个故事还很年轻，可能是出于善意。如果这是一个诚实的错误，这是无能的表现。如果这是一个故意的后门，是时候让你所有的 Fortinet 设备退役了。

Pulse Secure VPNs 具有类似的预授权任意文件读取漏洞。一旦完整的报告发布，我们也会报道。

### 野外开发

但是等等，还有更多。藏起你的孩子，藏起你的妻子。据 ZDNet 报道，Webmin、Pulse Secure 和 Fortigate 已经被积极开发利用。根据来自不良数据包的报告，Webmin 后门在声明发布后的一天内就成为扫描的目标，并在声明发布后的三天内被利用。已经有一个僵尸网络通过这个后门传播。据估计，大约有 29，000 个易受攻击的面向互联网的服务器。

Pulse Secure 和 Fortinet 的 Fortigate VPN 设备也是攻击的目标。尽管这些漏洞首先被报告给了供应商，并在公开披露之前很早就修补了，但仍有数千个易受攻击的设备存在。显然，路由器和其他网络设备硬件是一劳永逸的解决方案，通常没有重要的安全更新。

## VLC 这次实际上很脆弱

VLC 媒体播放器发布了新的更新，[修复了 11 个 CVE](https://www.videolan.org/security/sb-vlc308.html)。这些 CVE 都是错误处理格式错误的媒体文件，只有通过打开带有 VLC 的恶意文件才能被利用。如果你安装了 VLC，一定要更新它。尽管没有任何针对这些问题的任意代码执行被证实，但它很可能最终会发生。

## 灰色市场 IP 地址

随着 IPv4 地址的耗尽，许多人开始使用替代方法来获取地址空间，包括犯罪分子。Krebs on Security [详细介绍了他对一个这样的故事](https://krebsonsecurity.com/2019/08/the-rise-of-bulletproof-residential-networks/)的调查:住宅网络解决方案公司(Resnet)。这一切都始于源自 Resnet 住宅 IP 地址的欺诈交易的上升。这是一家真正提供互联网连接的公司，还是一家犯罪企业？