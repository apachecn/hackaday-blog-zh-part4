# 本周安全:Java 的精神签名，AWS 逃逸，和一个讨厌的 Windows Bug

> 原文：<https://hackaday.com/2022/04/22/this-week-in-security-javas-psychic-signatures-aws-escape-and-a-nasty-windows-bug/>

Java 版本 15、16、17、18(可能还有一些更老的版本)有一个大问题， [ECDSA 签名验证完全被破](https://neilmadden.blog/2022/04/19/psychic-signatures-in-java/)。这个故事是一个很好的例子，说明了意想不到的后果的危险，开发自己的密码的陷阱，以及为什么要为重要的代码建立一个测试套件。在 Java 15 中，ECDSA 验证代码被重写，将代码从 C++转移到 Java 本地实现。新代码遗漏了一个重要的检查，即初始化和验证值都是非零的。

对 ECDSA 的[复习可能会有所帮助。椭圆曲线数字签名算法是一种非对称加密方案，其中公钥-私钥对用于加密或签名消息。ECDSA 不使用大数的因式分解作为单向函数，而是使用一个在特殊椭圆曲线内部反弹的向量。一个签名由两个值组成，随机起始点`r`和证明`s`。ECDSA 规范的一部分是这些值不能为零，因为验证函数包括与这些值相乘。被零除乘有短路算法的倾向，这个也不例外。`r=0`和`s=0`的签名总是有效的，不需要私钥。](https://blog.cloudflare.com/a-relatively-easy-to-understand-primer-on-elliptic-curve-cryptography/)

Java 代码没有对签名中的零进行健全性检查，因此任何使用 ECDSA 签名的 Java 程序都可以被微不足道的假凭证(全是零)击败。这个缺陷最糟糕的部分是它是一个已知的问题，包含在[发布的测试用例中，比如 Wycheproof](https://github.com/google/wycheproof) 。这不是一个我熟悉的项目，但它现在肯定在我的加密雷达上。

[NIST 发布了各种加密算法的测试向量](https://csrc.nist.gov/projects/cryptographic-algorithm-validation-program/block-ciphers)——发布明文、密钥和密文集，用于验证您的代码是否正确实现了给定的方案。这些的问题是它们不是敌对的；NIST 向量正确地使用算法。Wycheproof 的测试都是无效使用，旨在发现像这样的边缘案例 bug。如果你涉及一个加密实现，一定要在测试套件中使用公开的测试向量，但是要包括 Wycheproof 或者类似的东西。

这个缺陷是在周二公布的，但最初是在大约五个月前的 11 月份发现的。正如在 Twitter 上敏锐观察到的那样，对于 Oracle 来说，在 Java 代码中添加一个`if`语句需要很长时间。已经有了一个扫描器来帮助你审计你的 Java 程序暴露出的问题。官方修复已在四月份的关键更新集中发布。

## log4 外壳二阶后果

我们不经常考虑像 Log4shell 这样的大 bug 的二级后果，但事实是，每个 bugfix 也是一个可能的新漏洞，当被修复的 bug 广泛而严重时，更有可能出现后续的 bug。在这种情况下，这个统计彩票的不幸赢家是亚马逊。AWS 在他们的 Java 基础设施中添加了一个热补丁系统，这个系统容易受到容器逃逸的攻击。

hotpatch 服务扫描容器内运行的任何`java`应用程序，并在需要时尝试修补这些进程。这个过程的一部分包括在底层主机上运行容器的`java`二进制文件——没有适当的容器化，并以 root 用户身份运行。用恶意的东西替换容器的`java`二进制文件，触发热补丁，然后在主机运行有效负载时接管主机，这是非常简单的事情。亚马逊已经更新了他们的代码，但根据你使用的服务，可能需要采取一些手动步骤。

## Windows RPC

一直追溯到 Windows 7 的 Windows 版本在如何处理远程过程调用方面有一个明显的安全问题。令人惊讶的是，这个漏洞不是通过 RPC 端口(135)访问的，而是通过 SMB (445)访问的，尽管仍然可以在端口 135 发现漏洞。CVE-2022-26809 是预授权远程代码执行(RCE)，CVSS 评分为 9.8。akamai[发布了一份补丁](https://www.akamai.com/blog/security/critical-remote-code-execution-vulnerabilities-windows-rpc-runtime)的分析，看起来整数溢出可能会导致堆缓冲区溢出。

## 被盗的 OAuth 令牌

在一个不断发展的故事中，GitHub 发现[多个私有存储库已经被使用偷来的 OAuth 令牌](https://github.blog/2022-04-15-security-alert-stolen-oauth-user-tokens/)签出。代币似乎是从赫罗库和特拉维斯-CI 那里泄露的。这两个组织都在使其令牌失效，并警告受影响的用户。Travis CI[发表了一篇帖子](https://blog.travis-ci.com/2022-04-17-securitybulletin)，暗示令牌是通过中间人攻击获得的，但没有透露多少具体细节。

## 守望先锋在野外攻击

CVE-2022-26318 在 3 月份公布并修复了非常有用的“一个漏洞，该漏洞可能允许未经验证的用户在 Firebox 上执行任意代码”正如我们所知，一个模糊的漏洞描述不足以阻止一个坚定的攻击者对一个缺陷进行逆向工程；到三月底，在野外观察到攻击。【迪伦·平杜尔】在[来自](https://blog.assetnote.io/2022/04/13/watchguard-firebox-rce/)的这篇文章中拯救了我们，这篇文章概述了漏洞的历史，并对漏洞进行了分析。整个过程是好的，但是简单来说，一个格式错误的 XML 文档触发了太多对`strcat()`的调用，导致缓冲区溢出到堆中。

## 比特和字节

联想发布了大量笔记本电脑型号的固件更新，因为研究人员发现了联想 UEFI 固件的漏洞。这些问题似乎都是由于无意中包含在产品固件中的制造和调试代码造成的。危险在于，一个足够先进的恶意软件将不再仅仅局限于加密你的数据，它可以在固件中安装一个模块，从而导致非常顽固的感染。

一个 [VMware 漏洞](https://www.vmware.com/security/advisories/VMSA-2022-0011.html)，CVE-2022-22954，正在被大肆利用。它被描述为“服务器端模板注入远程代码执行”。易受攻击的组件 VMware Identity Manager 是其他 VMware 产品的组件，因此您可能会在不知不觉中运行它。这是一个 CVSS 9.8，似乎是可利用的预认证。

最后， [Apache Struts 2.x 有一个反复出现的漏洞](https://cwiki.apache.org/confluence/display/WW/S2-062) : CVE-2020-17530 又变成了 CVE-2021-31805，因为最初的修复被证明是不够的。这个缺陷允许 OGNL 代码被评估两次，这可能导致 RCE。在本月发布的 2.5.30 版本中，该错误再次得到修复。希望这个修复可以捕获所有的极限情况。