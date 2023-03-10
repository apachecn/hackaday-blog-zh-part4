# 本周的安全:自爆，加密后门，黑仔应用程序，和 VLC 启示录不是

> 原文：<https://hackaday.com/2019/07/26/this-week-in-security-selfblow-encryption-backdoors-killer-apps-and-the-vlc-apocalypse-that-wasnt/>

Selfblow(顺便说一句，不要在工作中谷歌这个)是[Balázs Triszka]的一个聪明的利用影响每一个使用`nvtboot`boot loader 的 Nvidia Tegra 设备-几乎所有设备，除了任天堂 Switch。这是 CVE 2019-5680，根据英伟达的评级为 8.2，但 CVE 的高评级并不能完全反映现实情况。利用该漏洞意味着写入引导设备，这需要 root 访问权限以及内核标志集，以便将引导分区暴露给用户空间。这个漏洞是作为[Balázs]和其他 LineageOS 开发人员为 Nvidia Tegra 设备构建开源引导加载程序的一部分发现的。

Tegra 引导过程有点不同，有几个阶段和一个专用的引导和电源管理 CPU (BPMP)。零级 ROM 将`nvtboot`加载到内存中，并开始在 BPMP 上执行。`nvtboot`的任务之一是验证下一个引导程序步骤`nvtboot-cpu`的签名。文件大小和存储位置嵌入在`nvtboot-cpu`头中。这里有两个问题使得这种漏洞成为可能。第一个是在执行签名验证之前，引导加载程序二进制文件被加载到它的最终内存位置。编写代码是为了在主 CPU 上开始执行引导程序之前验证它的签名，所以一切正常，对吗？

这种引导加载程序代码的第二个问题是，内存加载位置嵌入在固件头中，并且在将下一个引导加载程序阶段加载到内存之前，不会验证该位置。此时，我们都应该知道一旦允许无限制的内存写入会发生什么。这个漏洞究竟是如何利用无限制写入的，这特别有趣。头文件指示`nvtboot`在自己的签名验证例程之上编写下一个引导加载程序二进制文件，在自己身上炸了一个洞，因此得名。当`nvtboot`试图调用该函数来验证该文件是否被 Nvidia 正确签名时，它反而跳转到这个未签名的代码中执行。它优雅、有效，为开发 Tegra 设备的开源引导程序打开了大门。

### 加密后门

周二，司法部长威廉·巴尔在福特汉姆大学发表了演讲。他谈到的一个话题是加密中的后门，特别是在消费平台中。[Bruce Schneier] [看一下演讲](https://www.lawfareblog.com/attorney-general-william-barr-encryption-policy)的相关部分，并将其分解。他持乐观态度，因为他看到谈话从顽固坚持加密后门是无害的转变。现在，我们至少可以讨论弱化加密带来的社会损害是否值得它为执法部门提供的透明度。

然而，Schneier 在这个问题上的立场没有改变。他坚持认为，这项技术是中立的，如果你允许监听消费者的手机，你也允许监听核电站运营商、首席执行官和民选官员的手机。安全就是安全。

### 致命的代码

当医疗公司拒绝解决医疗设备中的漏洞时，您会怎么做？[你写了一个可以杀死](https://www.wired.com/story/medtronic-insulin-pump-hack-app/)的概念验证漏洞。在他们的辩护中，QED Secure Solutions 的研究人员向 FDA 披露了他们的杀手级应用程序，并在自愿召回后协调了公开发布。

问题中的设备是具有无线控制的胰岛素泵。内置的身份验证仅限于设备的序列号，因此攻击只需向所有可能的序列号发送命令。他们的工作利用了软件无线电的优势，并且经过测试，只能在几英尺之外工作。但这足以让不安全的设备(自愿)被召回。

### VLC 很脆弱？

本周 VLC 新闻铺天盖地。首先，VLC 有一个未公开的漏洞，然后更多关于 CVE-2019-13615 的细节出来了，首先被归类为远程代码执行漏洞，得分为 9.8 分(满分 10 分)。VLC 已经被下载了几十亿次，所以很多人声称有几十亿台电脑容易受到攻击。

这个耸人听闻的故事的唯一问题是，VLC 开发人员公开声称他们无法复制崩溃。随着越来越多的信息泄露出来，[一个更清晰的画面出现了](https://www.bleepingcomputer.com/news/security/keep-calm-carry-on-vlc-not-affected-by-critical-vulnerability/)。显然，被发现的漏洞实际上在`libebml`中，并且在一年前就被发现和修补了。重新发现这个问题的研究人员正在一台最近没有更新的 Linux 机器上工作。

我们很少看到漏洞的宣传和现实之间如此明显的差异。正如 VLC 开发人员在 Twitter 上解释的那样，安全社区中的许多人确实过早地将这个漏洞看得如此重要。管理 CVE 进程的组织 MITRE 需要承担很大一部分责任。他们似乎完全没有验证漏洞声明之前，分配一个荒谬的高评级 CVE 号码。

与你可能读到的相反；不，你不需要马上卸载 VLC；不，没有数十亿台突然易受攻击的计算机；不，目前发布的 VLC 不容易受到这种特殊的错误。然而，如果你有旧的库，你早就应该更新了。