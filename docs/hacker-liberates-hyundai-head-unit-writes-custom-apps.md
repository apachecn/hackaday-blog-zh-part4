# 黑客解放现代总部，编写定制应用程序

> 原文：<https://hackaday.com/2022/07/18/hacker-liberates-hyundai-head-unit-writes-custom-apps/>

[greenluigi1]买了一辆现代 Ioniq 汽车，然后，令我们惊讶的是，[完全拆除了](https://programmingwithstyle.com/tags/d-audio2/)基于 Linux 的主机固件。我们的意思是，他[绕过了](https://programmingwithstyle.com/posts/howihackedmycar/)所有的固件更新认证机制，对固件更新进行了逆向工程，[创建了颠覆性的更新文件](https://programmingwithstyle.com/posts/howihackedmycarpart2/)，这让他在自己的设备上拥有了根外壳。然后，他对运行 dash 的应用框架进行逆向工程，[创建了自己的应用](https://programmingwithstyle.com/posts/howihackedmycarpart3/)。不仅仅是为了展示——在连接到 dash 可用的 API 并通过头文件访问后，他能够从他的应用程序监控汽车状态，甚至锁/解锁车门。最终，dash 完全被征服了——他甚至[写了一个教程](https://programmingwithstyle.com/posts/howihackedmycarguidescreatingcustomfirmware/)展示任何人如何为现代 Ionic D-Audio 2V dash 编写自己的应用程序。

在这一系列为我们整理的文章中，他向我们展示了整个黑客攻击过程——读起来真是一种享受。他涵盖了各种各样的内容:破解。zip 文件，在 USB-以太网加密狗上重新编程 efused MAC 地址，定位加密固件文件的密钥，小心地将后门放入 Linux 系统，在为主机交叉编译软件时对抗加密的 C++编译错误和标志组合，为专有的未记录框架制作插件；以及其他很多我们在家用消费类硬件时会遇到的逆向工程方面的问题。

这标志着黑客对我们生活中另一台我们不打算修改的计算机的胜利，以及一场精心记录的胜利——帮助我们每个人反击像这样的“不可修改”的小工具。读完这些教程后，你会学到一些新的技术。我们以前也报道过类似的总部黑客事件，例如，斯巴鲁和 T2【日产】，每一次都是一次值得关注的旅程。