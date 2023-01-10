# 将区块链引入网络监控

> 原文：<https://hackaday.com/2020/01/22/bringing-the-blockchain-to-network-monitoring/>

如果你需要确保你的电脑没有被篡改，你可以看看日志文件。如果事情看起来可疑，那就是进一步调查的理由。如果您运行一个大型的计算机网络，您可能想要查看所有的日志，但是您不会想要逐个查看每台计算机。设置中央服务器来分析日志暴露了另一个攻击面:传输中的日志。您如何确保攻击者不会同时拦截和清理您的日志文件报告？

这个问题以及几乎所有其他问题的答案都是区块链！也可能不是，但在 2019 年黑客日超级会议的这个简短的介绍中，杰夫·伍德的 Shanni Prutchi 和其他六名大学生打算找到答案。虽然 Shanni 和我们一样对区块链的大部分技术“不屑一顾”,但你必须承认一件事:递归散列你的日志数据以确保它们不被篡改听起来并不是一个坏主意。

 [https://www.youtube.com/embed/HmONXgmSqYA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/HmONXgmSqYA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



该演讲涵盖了学生如何使用 Linux 基金会的 [Hyperledger Fabric](https://www.hyperledger.org/projects/fabric) 区块链理工大学，将其与集装箱化日志记录系统和基于 [splunk](https://www.splunk.com/) 的集中式报告和显示系统相结合，构建安全报告和自动检测系统。学生，像黑客一样，在时间和金钱上都有紧张的预算，所以听到什么没起作用以及什么起作用是很有趣的。由于时间限制，从零开始编写他们自己的区块链是不可能的，而且使用一个更大的框架需要太长的时间。由于内存限制，无法在 Raspberry Pi Zeros 上运行 Docker 容器。

最后，他们选定了一个测试平台，用一些二手的 Linux 机器和 Hyperledger Fabric 来保护数据，看起来他们对所有相关工具都了如指掌。未来的方向包括拓宽日志报告的范围，将 Windows 机器包括进来，并改进报告自动化。更多细节请看他们的谈话！