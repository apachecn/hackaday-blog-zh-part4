# Rigol MSO5000 被黑，功能解锁

> 原文：<https://hackaday.com/2018/12/19/rigol-mso5000-hacked-features-unlocked/>

Rigol 的测试设备有被黑的历史。几年前，DS1022C 示波器被黑客攻击以增加带宽，最近 DS1054Z 被黑客攻击以解锁许可的功能。现在，轮到 MSO5000 了。

在 EEVBlog 论坛上，一个小组正在[研究另一个 Rigol，MSO5000](https://www.eevblog.com/forum/testgear/hacking-the-rigol-mso5000-series-oscilloscopes/) ，这是一个 70 MHz 的示波器，可以通过软件许可升级到 350 MHz。还内置了各种其他功能，包括双通道、25 MHz 任意波形发生器，但除非购买了许可证密钥，否则会被锁定。该小组已设法启用所有锁定选项，无需许可证密钥。

破解非常简单。在作用域上运行的 Linux 系统有一个默认的 root 密码，您猜对了，“root”。使用这些凭证通过 SSH 登录后，用户只需修改启动文件，将“-fullopt”标志添加到“appEntry”应用程序中。这将在完全解锁的状态下启动应用程序，从而可以访问所有功能。

MSO5000 的价格约为 1000 美元，仅带宽选项就增加了 3000 多美元。如果你愿意拿你的担保冒险，并且你有用 vi 编辑文件的技能，这个黑客免费提供了一个重要的升级。

如果你有一台 DS1022C，你会在这里找到我们对它的黑客攻击的报道，同样，DS1054Z 的用户也会在这里找到他们的报道。

标题图片: [EEVBlog](https://www.youtube.com/watch?v=P5faiEUXbGg) 。