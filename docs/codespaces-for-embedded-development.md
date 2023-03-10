# 嵌入式开发的代码空间

> 原文：<https://hackaday.com/2020/09/07/codespaces-for-embedded-development/>

我们可以同情本杰明·卡韦。他有许多开发板，为每个开发板维护许多工具链变得很痛苦。我们也遭受了升级一个工具以某种模糊的方式破坏另一个工具的痛苦。他的解决方案？使用 [Github Codespaces](https://www.youtube.com/watch?v=-enIM4x-KPA&feature=emb_logo) ，beta 测试人员可以提前获得。

这个想法是，您可以将一个特定于容器的容器剥离给一个 GitHub 存储库，该存储库拥有处理一个项目所需的所有适当的版本和依赖项。

如果你注册了测试版，你会在等待名单上，但是看着[本杰明]一步一步地走下去是很有趣的。这项服务在测试期间是免费的，你可以得到两个代码空间。据推测，您最终将能够为更多的功能付费。

这个想法很好，但我们还得看看实施情况。预配置的容器可能会从一台机器移动到另一台机器，或者甚至移动到更深的存储位置，以便以后重新配制。从浏览器的角度来看，将二进制图像刷新到设备看起来很痛苦。我们已经看到它做得很好，例如，在线 Arduino IDE，但它确实需要一些可安装的软件助手来完成。

我们很好奇这将支持多少不同的平台。然而，你可以使用 [Docker](https://hackaday.com/2016/09/01/how-to-use-docker-to-cross-compile-for-raspberry-pi-and-more/) 或者像 VirtualBox 这样的成熟虚拟机来推出你自己的版本，避免使用云。当然，这是更多的工作，但你掌握自己的命运。添加类似[的平台。IO](https://hackaday.com/2017/04/07/platformio-and-visual-studio-take-over-the-world/) 和您选择的开发工具，您可以避免在您的主计算机中有这么多相互竞争的开发工具。

 [https://www.youtube.com/embed/-enIM4x-KPA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/-enIM4x-KPA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

