# 为您的 Pi 项目轻松配置设备

> 原文：<https://hackaday.com/2020/11/18/easy-device-configuration-for-your-pi-projects/>

我们都熟悉新的大众市场物联网设备的典型配置序列。第一次打开它，它会显示一个临时 Wi-Fi 网络，连接到该网络并打开一个网页进行设备配置。如果能够将该功能集成到您自己的项目中，而不必自己编写，那岂不是很有用！幸运的是，现在多亏了[彼得·沃什]的树莓派应用守护程序项目，你可以做到了。

它的核心是一组 Perl 脚本，不管你的软件是什么，它们都可以运行，然后监控一个 GPIO。按下一个切换 GPIO 的按钮会停止应用程序并启动接入点和网络服务器。方便的是，所有的代码都可以在 GitHub 库中找到[，并且在我们放在断点下方的视频中有一个功能的预演。这并不是对每个人都有吸引力的东西，但是对于那些不得不把他们的工作传递给那些不能深入配置文件和打开编辑器的人的人来说，这应该是一个特别有用的补充。](https://github.com/ToolChainGang/AppDaemon)

[https://player.vimeo.com/video/479673811](https://player.vimeo.com/video/479673811)