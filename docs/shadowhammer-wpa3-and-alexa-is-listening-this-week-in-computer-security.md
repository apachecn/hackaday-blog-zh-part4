# Shadowhammer、WPA3 和 Alexa 正在收听:本周计算机安全

> 原文：<https://hackaday.com/2019/04/19/shadowhammer-wpa3-and-alexa-is-listening-this-week-in-computer-security/>

让我们来了解一下计算机安全新闻吧！大新闻是 shadow hammer——华硕的实时更新实用程序提示用户下载一个没有任何描述或变更日志的更新。人们认为这很奇怪，但华硕正确地签署了更新，防病毒扫描报告它是安全的。

近一年后，卡巴斯基实验室宣布，他们已经确认这一奇怪的更新确实是一次供应链攻击——通过另一家供应商攻击目标。另一个最近的例子是添加到 CCleaner 的后门，当时一个不知名的参与者破坏了 CCleaner 的构建系统，并使用该后门来攻击其他使用 CCleaner 的公司。有趣的是，CCleaner 中的后门与华硕 updater 中的后门有一些相似之处。结合华硕是这次早期入侵的目标公司之一的知识，卡巴斯基实验室的研究人员认为，CCleaner 攻击可能是华硕被入侵的途径。

暗影之锤静静地坐在它感染的绝大多数机器上。它专门针对大约 600 台机器，通过它们网卡的 MAC 地址来识别。我们还没有看到任何关于谁在目标名单上的报道，但卡巴斯基正在托管一项服务来检查你的 MAC 是否在名单上。

当我们还在等待完整的技术论文时，研究人员做了一个关于 Shadowhammer 的近 30 分钟的演示，嵌入了关于 Dragonblood 的新闻，亚马逊监听你的对话，以及 NSA 提供 Ghidra 源代码。跳完后再见！
 [https://www.youtube.com/embed/I6RnZUMftk0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/I6RnZUMftk0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent) 

## WPA3 和龙血

WPA3 现在是个东西了。它旨在减轻 WPA2 的弱点，几乎没有任何设备支持它，并且已经发布了一篇具有花哨名称的论文，详细介绍了它的弱点。[龙血](https://papers.mathyvanhoef.com/dragonblood.pdf)。作者已经发现了一个拒绝服务漏洞和一些旁道密钥攻击。我发现最有趣的两种攻击是降级攻击和计时攻击。

降级攻击滥用了针对旧设备的 WPA2 内置支持。攻击者能够对试图连接到网络的客户端发起中间人攻击。即使协议检测到攻击并中止连接，也会泄漏足够的信息来启动离线字典攻击。

第二种攻击是针对 WPA3 的密码推导功能之一的定时攻击。通过测量运行这个派生函数所花费的时间，攻击者能够确定正在处理的密码或密钥的统计信息。

作者还谈到了使用 Spectre 风格的缓存攻击来提取用户密码的更多信息的可能性。如果用户的密码出现在攻击者的字典中，这些统计数据源的组合可以给攻击者提供足够的信息来获取用户的密码。要点是和往常一样，选择不太可能在字典中找到的长密码。

## 我总觉得有人在听我说话…

### 而且我没有隐私…

在这条只能被描述为惊人而又显而易见的新闻中，[亚马逊将 Alexa 捕捉到的声音片段发送给承包商和员工](https://www.bloomberg.com/news/articles/2019-04-10/is-anyone-listening-to-you-on-alexa-a-global-team-reviews-audio)，以便更好地训练他们的语音转文本神经网络。这很明显，因为当 Alexa 无法理解我们，但要求人类倾听时，亚马逊还能做什么。想想 Alexa 听到的所有奇怪的声音，从淋浴时难听的歌声，到不是为别人准备的私人谈话，也令人吃惊。现在我们知道，有人真的在听——也许。

## 国家安全局在开源 Ghidra 上做得很好

你可能还记得我们谈论过 NSA 最新的开源项目 GHI DRA T1。源代码已经从[推送到 Github](https://github.com/NationalSecurityAgency/ghidra) ，拉取请求也源源不断。通常的警告是:确保你从一个有信誉的来源下载。

安全是一项永无止境的任务，所以我们不可避免地会回来做更多的工作。知道一些我们应该报道的事情，把它放到我们的提示栏！