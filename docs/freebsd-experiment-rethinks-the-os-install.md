# FreeBSD 实验反思操作系统安装

> 原文：<https://hackaday.com/2021/08/10/freebsd-experiment-rethinks-the-os-install/>

虽然介质可能已经从软盘发展到 DVD 和 USB 闪存驱动器，但是自 20 世纪 80 年代以来，在台式计算机上安装操作系统的整个过程还是大同小异。从广义上来说，你可以说现在大多数操作系统安装程序需要更多的点击而不是打字，但总的来说，并没有太多真正的改变。当然，这并不意味着没有改进的余地。

在 FreeBSD 2021 年 4 月至 6 月的状态报告中详细列出的一长串项目中，有一个由[Yang Zhong] 开发的实验性安装程序的[简要更新。为了让 FreeBSD 的安装更加用户友好，新的安装程序抛弃了传统的终端界面，完全采用了现代的以网络为中心的设计模式。一旦用户启动到实时操作系统，他们只需在任何时候将浏览器指向环回地址，就可以访问安装程序的 GUI。](https://www.freebsd.org/status/report-2021-04-2021-06/#_experimental_installer)

光是这一点并不特别具有突破性。毕竟，谷歌已经在 Chrome OS 中实现了一个带有 web 框架的完整操作系统，所以让安装程序成为一个 web 应用真的很难吗？但让[杨]的安装程序如此有趣的是，它的网络界面不仅限于本地机器，网络上的任何浏览器都可以访问。

[![](img/5608e0a8ede2f30f03b5ccd320b94763.png)](https://hackaday.com/wp-content/uploads/2021/08/bsdweb_detail.png) 这意味着你可以将 FreeBSD 的安装盘放入网络上的无头机器，并使用笔记本电脑甚至智能手机上的浏览器来访问安装程序。老人们会指出，精明的用户总是能够通过 SSH 从另一台计算机访问文本安装程序，但即使是最坚定的勒德分子也不得不承认，只要在你手边的任何设备上打开浏览器，并将其指向目标机器的 IP 地址，这是一个很大的可用性改进。

虽然该软件看起来足够完整，可以完成基本的安装，但我们应该提醒读者，现在还为时尚早。目前还没有适当的身份验证，所以一旦您启动到实时环境，网络上的任何人都可以格式化您的驱动器并开始安装过程。

GUI 的某些部分也没有完全发挥作用，偶尔会弹出杨的说明来解释什么有用，什么没用。例如，手动网络配置面板目前只适用于 WiFi 接口，因为这是他个人必须测试的全部内容。相当现代的安装工，的确。

有些人会说，Linux 和 BSD 等替代操作系统吸引人的部分原因是它们可以在较旧的硬件上愉快地运行，所以我们可以想象，安装程序使用占用大量内存的网络浏览器来展示其界面的想法不会受到很多用户的欢迎。在我们的测试中，实验安装程序 ISO 甚至不会启动，除非它检测到至少 4 GB 的内存。但这无疑是一个有趣的实验，而且随着它的成熟，还需要继续关注。

感谢迈克尔的提示。]