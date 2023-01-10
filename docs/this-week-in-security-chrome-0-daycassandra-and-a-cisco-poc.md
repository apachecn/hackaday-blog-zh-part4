# 本周安全:Chrome 0-day、Cassandra 和 Cisco PoC

> 原文：<https://hackaday.com/2022/02/18/this-week-in-security-chrome-0-daycassandra-and-a-cisco-poc/>

运行 Chrome 还是基于 Chrome 的浏览器？[检查版本 98.0.4758.102](https://threatpost.com/google-chrome-zero-day-under-attack/178428/) ，如果您没有运行该版本或更高版本，请进行更新。快速提示，使用`chrome://restart`触发 Chrome 的立即重启，就像更新后的重启一样。这非常有用，尤其是在 Linux 上安装了更新之后，使用`apt`、`dnf`等等。

CVE-2022-0609 是刚刚修补的大漏洞，谷歌已经承认它正在被利用。这是一个释放后使用的错误，意味着应用程序将内存的一部分标记为返回给操作系统，但随后访问现在无效的内存地址。释放内存和错误地重用内存之间的时间间隔使得恶意代码可以声称该内存是自己的，并编写一些意想不到的内容。

谷歌已经吸取了过早公开太多细节的教训，这个 CVE 和相关的错误不容易在 Chromium 项目的源代码中找到，Chromium 代码测试套件中似乎也没有发布漏洞。

## 阿帕奇卡桑德拉

![Cassandra Logo](img/26ae9c7b71895e35aea896fa9511431e.png) Cassandra 是一个基于 NoSQL 范式的流行分布式数据库。[它容易受到 CVE-2021-44521](https://jfrog.com/blog/cve-2021-44521-exploiting-apache-cassandra-user-defined-functions-for-remote-code-execution/) 的攻击，这是一个潜在的令人讨厌的 RCE 排名 8.4 的 CVSS。这里的可取之处是，它是一个易受攻击的非默认配置，需要将三个特定的配置标志从默认设置更改为易受攻击。另一方面，这些标志都与 Cassandra 的用户定义函数(UDF)相关，这是该项目的一个杀手级特性。这三个标志是:`enable_user_defined_functions`和`enable_scripted_user_defined_functions`设置为真，`enable_user_defined_functions_threads`设置为假。

让我们稍微分析一下，了解一下这里发生了什么。首先，`enable_user_defined_functions`是不言自明的，因为它启用了 UDF。这允许用户提供在服务器上运行的 Java 函数，进行数据操作。第二个标志启用脚本函数，在这个上下文中意味着 JavaScript。请注意，众所周知，允许这些用户定义的 JavaScript 函数是不安全的，但这可以通过在沙箱中运行它们来缓解，这是自动发生的。最后一个标志`enable_user_defined_functions_threads`默认设置为 true，并强制这些 UDF 在单独的线程上运行。最重要的是，这些线程在没有特殊权限的安全管理器下运行。

将 boolean 设置为 false 意味着每个函数都在主程序线程中运行。不明显的是，这意味着安全管理器设置也是从主程序继承的。其中一个设置只是允许禁用安全管理器。从那里开始，最简单的逃避就是调用`this.engine`，它有执行非沙盒代码的函数，包括一个 Java `.exec()`调用。

## NAS 中断

Pwn2Own 上一次非常聪明的攻击出了差错，而[我们足够幸运地得到了关于它的报道](https://www.iot-inspector.com/blog/advisory-western-digital-my-cloud-pro-series-pr4100-rce/)。它是西部数据 My Cloud Pro，该漏洞是一个命令注入，由包含在 shell 命令中的 HTTP 响应产生。该设备每五分钟进行一次 HTTP 呼叫，检查互联网连接。最终使用`analyticlog`二进制文件记录响应，当然只是在系统调用中包含部分响应。如果您不熟悉这类漏洞，在 Unix 系统上，可以使用反勾`` ` ``字符将命令作为参数的一部分。例如，在文件名中包含`date`的输出非常有用，但是在这种情况下，这是一个安全噩梦。

这个故事的转折是 Pwn2Own 的攻击失败了。这是一个简单的漏洞，只是一个针对 HTTP 域的中间人攻击，在响应中发送一个恶意命令。问题是，攻击是通过返回攻击者控制的 IP 地址来实现的，他们忘记了为 Pwn2Own 网络布局更改这个地址。时间不允许在规定的时间内修复 IP 地址和进行连接检查。

## 适用于思科的概念验证

上周我们讨论了思科的几个小型企业 VPN 网关中的漏洞，现在[一个概念验证已经发布](https://github.com/pedrib/PoC/blob/master/advisories/Pwn2Own/Austin_2021/flashback_connects/flashback_connects.md)。这是传入 HTTP 数据包上的一对简单的缓冲区溢出。第一种情况发生在将 HTTP 头和主体合并到一个 16k 的缓冲区时。因为标题和正文的最大容量都可以达到 16k，并且不做进一步的大小检查，所以这可以很容易地溢出数据包缓冲区，但不会导致崩溃或利用漏洞，因为第二个 16k 缓冲区就在内存中紧随其后。确实发生了什么，这是后来被复制到另一个 16k 缓冲区，但这个没有意外溢出保护。这是一个天真的空终止数据，所以整个双缓冲区的数据被复制，破坏了堆栈并导致可利用的损坏。

## 比特和字节

理智战胜了密苏里“黑客”事件。我们给你带来了一个研究人员/记者的故事，他说[在一个国家网站](https://hackaday.com/2021/10/15/this-week-in-security-the-apache-fix-miss-github-malicious-actions-and-shooting-the-messenger/)中发现了嵌入的社会安全号码。在负责任地披露了这一发现后，州长脱离了剧本，并以法律行动威胁研究人员。本周，负责此案的州检察官发布了一份声明，声明的一部分被嵌入此处。

> 审查案卷后，调查的核心问题已通过非法律手段得到解决。因此，利用大量资源和纳税人的钱来进行轻罪刑事指控是不符合科尔县公民的最佳利益的。

(编者注:那是*差点*道歉，对吧？)

谷歌[提高了对某些可利用的 0 天漏洞的奖励](https://security.googleblog.com/2022/02/roses-are-red-violets-are-blue-giving.html),这些漏洞被提交给他们的漏洞奖励计划，特别是那些涉及 Linux 内核、Kubernetes 和其他几个项目的漏洞。一个漏洞的最高支付现在高达 91，337 美元，并且有资格获得奖励的规则已经放宽。如果这是你的拿手好戏，现在是时候去抓虫子了。

最后，[克日什托夫·zając]发布了一系列 WordPress 插件问题，这些问题是通过他的自定义模糊框架发现的。代码看起来并没有公开，但它详细记录了他是如何通过这种方式找到 100 多份简历的。这对于寻找新的寻找 bug 的方法是很大的启发。