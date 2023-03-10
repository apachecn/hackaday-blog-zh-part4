# 本周安全:易受攻击的箱子、政府反应和新工具

> 原文：<https://hackaday.com/2022/04/08/this-week-in-security-vulnerable-boxes-government-responses-and-new-tools/>

独眼巨人眨眼僵尸网络被认为是来自俄罗斯的高级持续威胁(APT)的作品，似乎仅限于 Watchguard 和华硕设备。正常的三信和四信机构早在 2 月份就公布了他们的发现，并敦促每个有潜在易受攻击设备的人进行必要的验证和消毒。大约一个月后，在 3 月份，超过一半的僵尸网络仍然在线并运行，因此执法部门采取了严厉的措施来破坏网络。在对恶意软件本身进行逆向工程，并让法官签署该计划后，联邦调查局远程侵入了 13 台作为命令和控制节点的 Watchguard 设备。他们对这些节点进行了消毒，并关闭了易受攻击的端口，有效地将很大一部分僵尸网络离线。

促成僵尸网络的 WatchGuard 设备中的漏洞是 CVE-2022-23176，这是一个“暴露的管理访问”允许非特权用户管理访问系统的问题。这种模糊的描述听起来像是偶然包含在产品中的调试接口，或者是权限逻辑中的缺陷。无论如何，[该问题在 2021 年 5 月的更新中得到修复，但没有完全披露](https://arstechnica.com/information-technology/2022/04/watchguard-failed-to-disclose-critical-flaw-exploited-by-russian-hackers/)。攻击者显然逆向工程的修复，并使用它来感染和形成僵尸网络。联邦调查局在 2021 年 11 月通知 WatchGuard，他们大约有 1%的设备已经被入侵。直到今年 2 月，才公布了补救措施，并获得了该漏洞的 CVE。

这绝对是不理想的行为。更多的细节和 CVE 应该在 5 月份的修复中出现。正如我们之前所观察到的，晦涩实际上并不会阻止老练的参与者找出漏洞，但它确实会让用户和安全专业人员更难完成他们的工作。

## Zyxel 补丁可用

关于如何更好地处理类似的缺陷，请参见 Zyxel 对 CVE-2022-0342 的回应。这是访问控制逻辑中的一个缺陷，允许未经验证的管理员访问易受攻击的设备。Zyxel 针对该漏洞发布了 CVE，并透露了足够多的细节，让用户知道他们是否容易受到攻击。如果您正在运行补丁之前的固件，web 界面很容易被接管。这种缺陷不是孤立的事件，因为 Sophos 和趋势科技最近也修补并宣布了类似的问题。

## 拿下九头蛇

本周，德国当局形成了国际矛的尖端，端掉了 Tor 网络上的市场 Hydra 背后的物理服务器。你能想象到的所有东西都是在九头蛇上买卖的，为了了解市场和 sting 的范围，请注意在这次行动中有 543 个比特币被抢走。目前还没有逮捕任何人，但由于九头蛇也提供洗钱服务，抓获这么多的基础设施可能会揭露许多非法活动。目前还不知道这个 Tor 隐藏服务是如何被追踪到它的物理主机的，但它可能是政府运行 Tor 节点和网络定时分析的某种组合，以追踪基础设施。

## 春天 4 壳沉降物

Spring4Shell 在野外被利用，成千上万次触发[漏洞的尝试被类似 CheckPoint](https://blog.checkpoint.com/2022/04/05/16-of-organizations-worldwide-impacted-by-spring4shell-zero-day-vulnerability-exploitation-attempts-since-outbreak/) 的组织观察到。目前还不知道这些尝试中有多少成功了，但肯定会有一些。虽然[这个漏洞不像 Log4Shell](https://arstechnica.com/information-technology/2022/04/explaining-spring4shell-the-internet-security-disaster-that-wasnt/) 那么严重，但至少有一个僵尸网络已经开始利用这个漏洞传播。

[微软对该漏洞的报道很棒](https://www.microsoft.com/security/blog/2022/04/04/springshell-rce-vulnerability-guidance-for-protecting-against-and-detecting-cve-2022-22965/)，用一个有用的命令行程序来检查易受攻击的 Tomcat 安装:`$ curl host:port/path?class.module.classLoader.URLs%5B0%5D=0`HTTP 400 响应意味着你可能易受攻击。

## 面向云的数据包捕获——以及其他任何地方

情况是这样的。您正在 Docker 上运行的远程服务上工作，但有些地方工作不正常。要真正理解问题，您需要查看原始数据包数据。不幸的是，这是一个非常复杂的服务，它是在多个主机上运行的多个 Docker 映像。你如何捕获和组织你需要的包数据？现在有了一个工具，PacketStreamer 。[它是完全开源的](https://github.com/deepfence/PacketStreamer)，使用 BPF 内核框架来过滤和捕获数据包。从那里，您的捕获节点将捕获的数据转发到中央服务，中央服务将捕获的数据重组到一个排序的日志中。根据需要进行调查、分析和评审。

## 比特和字节

还记得[污管](https://hackaday.com/2022/03/11/this-week-in-security-ddos-techniques-dirty-pipe-and-lapsus-continued/)吗？这个 bug 弹出的一个有趣的地方是在 Android 上，如果你想根你的手机，这[是很棒的。该补丁已经登陆上游的安卓系统，三星也已经将更新推送到手机上。值得注意的是，像素 6 仍然没有定位。没错，如果你在谷歌的硬件上运行谷歌的代码，你仍然容易受到攻击——或者仍然能够根你的设备。一线希望之类的。](https://arstechnica.com/gadgets/2022/04/it-looks-like-pixel-6-users-have-to-wait-another-month-for-a-dirty-pipe-fix/)

骗子们发现了在伤口上撒盐的终极方法。你被诈骗了，损失了一些钱。当你的政府向你伸出援手，告诉你可能有机会找回你被盗的钱时，你会很高兴。只要填写适当的文件，支付处理费，财产回收办公室就会开始处理你的案件。当然，第一次骗到你的那个骗子只会大笑，扔掉伪造的文件，然后第二次拿走你的钱。

取决于你问的是谁，智能合约要么是货币、互联网和一切的未来；或者“程序员编写的不可改变的程序，他们傲慢地断言他们不会犯错误”([谢谢西蒙！](https://nitter.mstdn.social/webmink/status/1473279635169464329))。如果智能合同要经受时间的考验，我们需要能够调试和审计这些合同。从[thezero] 有一个很好的入门教程[，涵盖了将契约字节码反编译成可读代码的基础。额外的好处是，您可以模拟区块链来单步调试反编译的契约代码。俏皮！](https://www.shielder.com/blog/2022/04/a-sneak-peek-into-smart-contracts-reversing-and-emulation/)