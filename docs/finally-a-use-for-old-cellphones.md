# 最后，旧手机的一个用途

> 原文：<https://hackaday.com/2021/12/04/finally-a-use-for-old-cellphones/>

经过长达三年的寻找，我终于找到了一部旧手机的完美用途。有了它，一个紧迫问题的答案:[我们为什么不窃听手机](https://hackaday.com/2018/10/18/ask-hackaday-why-arent-we-hacking-cellphones/)？

第一，应用。Octo4a 项目让你可以使用一部旧的 Android 手机作为 3D 打印机服务器、网络界面，甚至延时相机来制作那些精美的电影，在这些电影中，印刷品似乎在你的眼前凭空生长。这是旧手机的完美应用，利用了内存、WiFi、图形功能，如果你想本地控制打印，甚至可以使用触摸屏。

连接到手机是我在手机项目开发中经常遇到的主要障碍，因为我想到了机器人应用。但是 Octo4a 不费吹灰之力就解决了这个问题。大多数 3D 打印机都设计为在 USB 上运行，因此将其连接到手机就像购买 USB OTG 电缆一样简单。随着 USB 端口的接管，为手机长时间供电变成了一个小问题，可以通过 Y 形电缆或一点焊料来解决。不管怎样，让操作系统不要进入睡眠状态，问题就解决了！

但这就是为什么这个*不是*的解决方案，它指出了手机黑客更深层次的问题，许多人在三年前的评论中指出了这个问题。 [Octoprint](https://octoprint.org/) 是用 Python 写的，因此很容易编写扩展和破解，如果你喜欢的话。当我第一次看到 Octo4a 时，我想“哦，太好了，一个工作的 Android Python 端口”。然后我就去钻研代码了。

Octo4a 是用 Kotlin 写的，用的是 Gradle 框架。这是 Octoprint 的完整移植，不仅仅是移植到不同的平台，而是移植到不同的编程语言和几乎完全不同的编程范式。我向[feelfreelinux]致敬，但我猜想，那些精通 Kotlin 和 Python 来帮助移植 Octoprint 中的上游变化的人的社区比 Python 程序员的社区要小得多。Octo4a 是一个伟大的项目，但在它的基础上进行开发并不容易。

所以，所有在我之前的评论中写道是 Android 软件生态系统阻止了手机的重复使用的人，这里有一个例外来证明你的规则！一个专注的、有才华的、多语言的开发者社区可以实现它，但是障碍太大了，很少有人会去面对它。

无论如何，感谢[Feelfree Filip]的出色工作！我会把这个放在我的老 S4 上。

This article is part of the Hackaday.com newsletter, delivered every seven days for each of the last 200+ weeks. It also includes our favorite articles from the last seven days that you can see on [the web version of the newsletter](https://mailchi.mp/hackaday.com/hackaday-newsletter-649368). Want this type of article to hit your inbox every Friday morning? [You should sign up](http://eepurl.com/gTMxQf)!