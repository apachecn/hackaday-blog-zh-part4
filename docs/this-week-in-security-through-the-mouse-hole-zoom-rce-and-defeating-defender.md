# 本周安全:通过老鼠洞，放大 RCE，并击败后卫

> 原文：<https://hackaday.com/2021/08/27/this-week-in-security-through-the-mouse-hole-zoom-rce-and-defeating-defender/>

由于不安全的驱动程序导致的 Windows 安全问题并不新鲜，但是[这次有点特别](https://www.bleepingcomputer.com/news/security/razer-bug-lets-you-become-a-windows-10-admin-by-plugging-in-a-mouse/)。插入一个 Razer 鼠标，告诉安装对话框你想安装到一个非标准的位置，然后 shift+右键点击浏览器窗口。选择一个 powershell，嘣，你现在有一个系统外壳。它不像 RCE 那样令人印象深刻，而且需要动手操作，但由于它的简单性，它很漂亮。

这是一个复杂的问题。首先，当插入 Razer 设备时，Windows 10 和 11 会自动下载并开始安装 Razer Synapse。注意，不仅仅是 Razer，任何像这样自动安装的品牌应用程序都可能以同样的方式存在漏洞。安装过程作为系统运行，因为它是自动启动的，所以不需要管理员帐户。问题的第二部分是安装程序本身没有采取任何预防措施来防止用户产生额外的进程。没有明显的方法来阻止从 FolderPicker 类中启动 Powershell，因此作为 SYSTEM 运行的安装程序必须放弃特权，以使这是一个安全的过程。真正的解决方案是微软对捆绑 WHQL 签名驱动的 GUI 安装程序说不。

## 变焦 RCE

Computest 的第 7 部门的研究人员在 Pwn2Own 上完成了一次令人印象深刻的黑客攻击，通过 Zoom 客户端实现了 [RCE。需要注意的是，攻击者必须被接受为联系人，无论是手动接受，还是在同一组织中接受。主要漏洞是 CVE-2021-30480，这是一个堆缓冲区溢出，是为连接远程客户端生成的字符串分配静态缓冲区的结果。虽然溢出是一个非常强大的漏洞，但要将其转化为一个完整的漏洞需要相当大的努力。](https://sector7.computest.nl/post/2021-08-zoom/)

为了实现这一目标，研究人员发现了一个数据泄露漏洞，这是基于图像链接中的 URI 混淆。格式错误的联系请求可能与奇怪的成员图像链接一起发送。在正常使用中，`pic_relative_url`字段将以一个前导“/”开始，并在`marketplacecontent.zoom.us`域指定一个图片。在他们精心制作的奇怪的联系请求中，他们使用了不以斜杠开头的相对 URL，而是以部分域名开头，如`example.org`。当 Zoom 客户端试图下载远程图像时，它最终从攻击者可以控制的域`marketplacecontent.zoom.usexample.org/...`发出请求。这个 URL 混淆错误可能与上面提到的溢出结合在一起，泄漏有关受害机器当前内存状态的数据。

使用的最后一个漏洞看似无关紧要，通过从 GIPHY 发送 GIF 可以绕过消息的最大大小限制。此外，发送多个副本不会触发多个下载，但会导致在内存中制作多个副本。将这些副本推入内存使研究人员能够建立他们的利用链，当限制在比赛的 5 分钟限制内时，完全攻击的成功率约为 50%。

 <https://sector7.computest.nl/post/2021-08-zoom/demo.webm?_=1>

[https://sector7.computest.nl/post/2021-08-zoom/demo.webm](https://sector7.computest.nl/post/2021-08-zoom/demo.webm)

**2011 年 8 月 27 日更新:**公司发言人联系了 Hackaday，就此问题发表了以下声明:

> 我们非常重视安全性，感谢 Computest 通过这种负责任的披露帮助我们提高平台的安全性。我们还想感谢零日倡议允许 Zoom 赞助并参与 Pwn2Own 温哥华 2021 比赛，从而发现这些问题。在 2021 年 4 月 19 日发布的 Zoom 版本 5.6.3 中，这些问题已通过服务器端修复和客户端修复得到解决。

## 关于飞马座的第二种意见

公民实验室发布了大赦国际对 NSO 集团飞马间谍软件项目的外部审查。他们的调查发现，大赦国际发现的技术方面是正确的——感染分析、IOCs 和确定的基础设施似乎都是正确的。大赦国际的报告提出的最大问题完全没有得到解决:目标名单。那份文件的来源和真实性仍然完全未经证实。

## 长期 Windows Defender 旁路

APTortellini 研究小组发布了他们击败 Windows Defender 的指南。一些评论者对第一步(提升到系统)嗤之以鼻。您甚至可能会想，如果您已经让一台机器成为 root 用户，那还有什么意义呢？获得系统访问权限只是真正恶意活动的开始。这项研究是关于如何使 Windows Defender 无效而不实际禁用它。

首先要知道的是，现代 Windows 系统采用了相当多来自 Unix 的元素，而 Windows 遗留的东西被固定在上面。为了说明这一点，请注意 Windows 10 的 C: drive 实际上位于`\Device\HarddiskVolumeX`，通过一系列符号链接使 C:符号起作用。其中一个链接是`\SystemRoot`，默认指向`\Device\BootDevice\Windows`。即使对于系统，链接也不能修改，但可以删除和重新创建。这个特定的路径恰好是 Windows Defender 加载其后端驱动程序的路径的一部分，`WdFilter.sys`。

该技术主要包括将`\SystemRoot`重新映射到一个虚假的 Windows 目录，然后重新启动 Windows Defender 服务，使其从欺骗的位置重新加载驱动程序。替换的驱动程序仍然必须被签署，但是这仍然留有很大的余地。在文章中，他们使用了[rw everything 驱动程序](http://rweverything.com/)。重新创建原始的符号链接，你就有了一个看起来工作正常的安慰剂防御程序，和一个运行的任意但已签名的驱动程序。

## 追回 6.1 亿美元

Poly 网络是一个分散的金融协议。我不打算赘述这到底意味着什么，因为这是一个安全专栏，而不是本周的区块链。只需知道它是一个区块链平台，使用智能合约来完成类似于银行或投资公司的事情。本月早些时候，保利网络出现了问题，超过 6 亿美元的资金被转移出了他们的控制范围。这一壮举似乎是智能合约本身的一个漏洞造成的。更多技术细节见[slow list](https://slowmist.medium.com/the-root-cause-of-poly-network-being-hacked-ec2ee1b0c68f)。

新的消息是，[白帽子先生]实际上已经把所有被盗资金的控制权归还给了保利网络。整个故事很离奇，又让人想起多年前[对道的攻击](https://www.coindesk.com/markets/2016/06/25/understanding-the-dao-attack/)。

## 伊朗出现更多可疑活动

紧随一个针对伊朗基础设施的黑客组织之后，我们又有了另一个组织闯入德黑兰 Evin 监狱的安全摄像头系统，并公布详细描述囚犯待遇的视频证据的故事。垃圾场的一部分是一个安全摄像头，显示主保安室的显示器。这确实是一个现实生活模仿艺术的例子。

> 这是伊朗最臭名昭著的监狱的安全控制室被黑客关闭的片段，简直就像电影一样。
> 
> 据美联社报道，黑客们正在泄露从 Evin 监狱偷来的闭路电视，以此来揭露对囚犯的虐待。pic.twitter.com/Ts2jbKmoqL
> 
> —艾德·克洛维斯(@ EdClowes)[2021 年 8 月 24 日](https://twitter.com/EdClowes/status/1430083273015840776?ref_src=twsrc%5Etfw)