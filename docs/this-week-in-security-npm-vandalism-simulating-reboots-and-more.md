# 本周安全:NPM 破坏，模拟重启，等等

> 原文：<https://hackaday.com/2022/01/14/this-week-in-security-npm-vandalism-simulating-reboots-and-more/>

我们已经报道了不少关于恶意软件潜入 NPM 和其他 JavaScript 库的故事。这个有点不一样。这次，[一个 JS 程序员破坏了他自己的包](https://www.bleepingcomputer.com/news/security/dev-corrupts-npm-libs-colors-and-faker-breaking-thousands-of-apps/)。它甚至不是恶意软件，也许我们应该称之为抗议软件？这两个软件包，`colors`和`faker`都很受欢迎，每周下载量接近 2300 万。他们的作者[马拉克]给他们每个人都添加了一个突破性的更新。这些库现在打印一个`LIBERTY LIBERTY LIBERTY`的标题，然后要么是随机字符，要么是非常糟糕的 ASCII 艺术。已经确认这不是外部攻击者，而是[马拉克]故意破坏他自己的项目。为什么？

这个故事似乎要追溯到 2020 年末，当时【马拉克】[在一场火灾中损失惨重，不得不在推特](http://web.archive.org/web/20220105101202/https://twitter.com/marak/status/1320465599319990272)上讨钱。编辑:感谢评论者[Jack Dansen]指出了一个遗漏的重要细节。马拉克被指控犯有鲁莽危害罪，并被怀疑可能有恐怖主义野心，因为在他被烧毁的公寓中发现了[制造炸弹的材料。两个星期后，](https://nypost.com/2020/09/16/resident-of-nyc-home-with-suspected-bomb-making-materials-charged/)[他在推特上说开源开发者的工作赚了数十亿美元，理由是 FAANG 泄密。FAANG 是指美国五大科技公司:脸书、苹果、亚马逊、网飞和谷歌。同一天，他在 Github 上为`faker.js`开了一期，抛出了最后通牒:“把这当成一个机会，给我一份六位数的年度合同，或者叉开这个项目，让别人来做。”](http://web.archive.org/web/20210609195556/https://twitter.com/marak/status/1325612104808886274) 

![Respectfully, I am no longer going to support Fortune 500s ( and other smaller sized companies ) with my free work. There isn't much else to say. Take this as an opportunity to send me a six figure yearly contract or fork the project and have someone else work on it.](img/0256431b5ba5432b86fd082169b4f50a.png)

如果你发现自己对[马拉克]感到遗憾，还有一条路可走。自 2018 年 2 月以来，他没有向`colors.js`提交代码。另一个开发者[DABH]从那时起就一直在做维护工作，直到破坏事件发生。总之，这是一个烂摊子。关于 NPM 的两个项目都已经恢复到它们的正常版本，并且很可能会转向项目的官方分支。

## 模拟重启

普遍的看法是，虽然有多个由 NSO 集团等公司生产的 iOS 恶意软件套件，但该恶意软件实际上无法击败苹果的安全启动，所以手机重启就足以“卸载”它。一旦你听到这个问题就很明显了:你信任一个被入侵的设备[实际上执行一次干净的重启](https://blog.zecops.com/research/persistence-without-persistence-meet-the-ultimate-persistence-bug-noreboot/)。ZecOps 的研究人员已经展示了他们称之为 NoReboot 的中断重启过程的能力。他们的代码挂钩到关闭功能，而不是杀死用户界面。一旦再次按下电源按钮，就会显示引导动画，最后一个方便的系统命令会重新引导用户空间。观看下面嵌入的演示。

没问题吧？只需使用硬件强制重启功能。调高音量，调低音量，然后按住电源按钮，直到看到 Apple 标志。你拿着它多长时间？直到徽标出现——没错，在真正的强制重启发生之前假装强制重启是微不足道的。好的，所以要知道你得到了真正的重启，你只需要拔掉电池……[哦](https://youtu.be/5qtLijnz1tc?t=72)。

 [https://www.youtube.com/embed/g_8JVUVLxTk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/g_8JVUVLxTk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[经由记录。](https://therecord.media/threat-actors-can-simulate-iphone-reboots-and-keep-ios-malware-on-a-device/)

## 微软黑了 MacOS

MacOS 有一个称为透明、同意和控制(TCC)的功能，可以处理单个应用程序的权限。例如，这个系统阻止计算器应用程序访问系统的网络摄像头。这些设置存储在主目录中的数据库中，有严格的控制防止应用程序直接修改它。微软宣布了 Powerdir 漏洞(T1 ),它结合了一些奇怪的东西来克服保护。这个漏洞很简单:创建一个假的 TCC 数据库，然后更改用户的主目录，使被欺骗的数据库现在成为活动的数据库。比这稍微复杂一点，因为一个随机的应用程序真的不应该能够重新映射主目录。

他们发现了两种技术来实现重新映射。首先是目录服务二进制文件，`dsexport`和`dsimport`。虽然直接更改主目录需要 root 访问权限，但这种导出/导入操作可以作为无权限用户完成。第二种技术是向`configd`二进制文件提供一个恶意捆绑包，进行代码注入攻击。看到微软继续针对 MacOS 做安全研究很有意思。他们的动机可能不那么高尚，但它确实有助于让我们所有的设备更加安全。

## QNAP 和 UPnP

这些年来，我们已经讨论了相当多的 NAS 漏洞，我也多次指出，将这样的设备暴露在互联网上是不明智的。建议的解释之一是 UPnP，今天我们有一些官方确认，这确实是问题的一部分。在一份新的公告中，QNAP 官方建议[关闭 QNAP 设备](https://www.qnap.com/en/security-news/2022/take-immediate-actions-to-secure-qnap-nas)中的 UPnP。这似乎早就应该被推荐了，或者更好的是，这些设备默认禁用 UPnP。我会更进一步，建议在你的路由器上也关闭这个功能，除非你知道你确实需要它。

## 如果你收到了一个 u 盘…

看在上帝的份上，不要插上电源！似乎有几家公司没有收到这份备忘录，因为 FIN7 已经成功利用这种方法发起了一场勒索活动。诀窍在于，他们会附上一封看上去很正式的信，也许还有一张礼品卡，引诱收件人插入 USB 驱动器来领取他们的忠诚度奖励。来自同一个集团[的 2020 年活动模仿了百思买](https://www.bleepingcomputer.com/news/security/fbi-hackers-sending-malicious-usb-drives-and-teddy-bears-via-usps/)，其中这一个声称来自亚马逊或 HHS。

您可能已经意识到这些闪存驱动器不仅仅是闪存存储。事实上，它们似乎是 BadUSB 设备——注册为 HID 设备并向计算机发送按键的小芯片。一旦接入，它们就会打开 Powershell 并运行恶意脚本，从而为攻击者提供远程访问权限。如果你收到这些，或类似的攻击，打电话给联邦调查局或当地的对等机构。来自公司和个人的报告导致了这样的警告。

## 值得注意的更新

今年[的第一轮 Android 更新已经出来了](https://source.android.com/security/bulletin/2022-01-01)，有一个突出的问题，影响了大量配备高通骁龙的设备。 [CVE-2021-30285](https://www.qualcomm.com/company/product-security/bulletins/january-2022-bulletin#_cve-2021-30285) 是高通闭源软件中的一个严重评级漏洞。这被称为“内核中不正确的输入验证”，但似乎是高通系统管理程序中的内存管理问题。它在 CVSS 震级上被评为 9.3 级，但目前没有其他细节。

VMWare 的虚拟化产品已经针对 CVE-2021-22045 打了[补丁，这是其虚拟光盘设备代码中的一个堆溢出漏洞。利用该漏洞可能导致虚拟机逃逸，并在虚拟机管理程序上运行任意代码，这对于虚拟机操作员来说是最糟糕的情况。该缺陷的等级为 7.7，谢天谢地，机器上肯定有一个 CD 映像，所以解决方法很简单——只需移除 CD 驱动器或映像。](https://www.vmware.com/security/advisories/VMSA-2022-0001.html)