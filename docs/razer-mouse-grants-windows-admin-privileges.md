# Razer Mouse 授予 Windows 管理员权限

> 原文：<https://hackaday.com/2021/08/26/razer-mouse-grants-windows-admin-privileges/>

俗话说，“所有联网的计算机都容易受到攻击，但一些联网的计算机比其他计算机更容易受到攻击”。虽然不是动物农场的确切措辞，但这句话还是有很多优点。当然，Linux 发行版存在一些病毒和问题，但是到目前为止，大多数攻击都是针对 Windows 的，因为每天使用它的人比其他任何操作系统都多。由[jonhat]发现的最新的 Windows 10 漏洞利用也简单得近乎滑稽，而[只不过是插上鼠标](https://twitter.com/j0nh4t/status/1429049506021138437)而已。

虽然稍微令人欣慰的是，攻击者需要对设备进行物理访问，而不是简单的网络访问，但这种攻击在其他方面有多简单是非常令人担忧的。显然，插入 Razer 鼠标会自动启动 Windows Update，为鼠标安装驱动程序。安装是以管理员权限运行的，用户只需按下 Shift 键并右键单击鼠标就可以打开 Power Shell。虽然[jonhat]最初试图让公司知道，但直到他在 Twitter 上公开这一漏洞，他们才做出回应，现在显然正在解决这个问题。

[其他人已经证实](https://www.bleepingcomputer.com/news/security/razer-bug-lets-you-become-a-windows-10-admin-by-plugging-in-a-mouse/)该漏洞确实有效，所以希望很快发布一个补丁来解决这个问题。与此同时，我们建议不要让陌生人将任何设备插入您的个人电脑，或者插入任何来源不明的设备。还要记住，有些攻击根本不需要物理或网络访问，就像这个[远程嗅探无线键盘](https://hackaday.com/2015/01/14/keystroke-sniffer-hides-as-a-wall-wart-is-scary/)的击键，安全性不太好，巧合的是也是由微软开发的。