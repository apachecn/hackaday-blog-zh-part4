# 黑进机器人吸尘器来写一个替代应用

> 原文：<https://hackaday.com/2021/09/16/hacking-a-robot-vacuum-to-write-a-replacement-app/>

虽然联网设备在家里非常有用，而且能够在半个地球之外监控你的洗碗机也很酷，但重要的是要注意隐私和安全问题。例如，购买的 Cecotec Conga 1490 机器人真空吸尘器(Rastersoft)带有一个 Android 应用程序，安装后要求几乎完全访问用户的手机。对这种侵犯隐私的行为不满意，更不用说潜在的安全隐患，[Rastersoft]开始试图对机器人的通信进行逆向工程([翻译为](https://translate.google.com/translate?sl=es&tl=en&u=https://blog.rastersoft.com/?p%3D2324))，以找出它在上网时到底在做什么。他通过配置一个 Raspberry Pi 作为接入点，让 vacuum 连接到它，并记录所有流过的数据。

结果，机器人给制造商打了电话，报告了它的序列号和一些配置设置。然后，服务器将控制权传递给移动应用程序，但不是没有通过远程服务器路由所有后续命令。这不仅令人毛骨悚然，还意味着如果制造商关闭服务器，应用程序将完全停止工作。[Rastersoft]因此有了编写定制软件来控制机器人的想法。他首先重新配置 Pi 的网络设置，以欺骗 vacuum 认为它正在连接到其制造商的服务器，然后编写一些 Python 代码来模拟服务器的响应。他现在控制着所有来回流动的数据。

经过大量的实验和数据分析，[Rastersoft]成功破译了应用程序发送的命令，使他能够在休息后编写一个完整的替代应用程序，包括控制吸尘器的所有标准动作，还包括手动控制吸尘器移动的新功能。所有代码都可以在 GitHub 上找到，对于那些也想破解他们的康加舞的人来说。

我们认为这是一个软件入侵你所拥有的未来设备的很好的例子，同时也减轻了默认软件给你的安全和隐私带来的许多危险。事实上，你从手机发送到你的真空世界的命令，可能被其他人存储和读取，首先是相当荒谬的。毕竟，我们已经看到机器人吸尘器是如何监视你的。

 [https://www.youtube.com/embed/T_ZY2NQ6UWo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/T_ZY2NQ6UWo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

