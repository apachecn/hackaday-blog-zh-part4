# 麦克风听你的…监视器？

> 原文：<https://hackaday.com/2019/05/25/microphones-listen-to-your-monitor/>

洛克威尔的一首歌，“有人在看着我”可能是锡箔帽人群的颂歌。但是一份新的论文显示，有人听你说话可能同样令人害怕。研究人员使用普通的麦克风监听电脑显示器。该演示包括分析音频以确定虚拟键盘的输入，甚至是一种判断人们是否在 Google Hangout 会话期间上网的方法。

根据电子发射读取监视器并不是什么新鲜事——问问维姆·范·埃克或者阅读一下 T2 的《暴风雨》。令人担忧的是，我们的电脑周围经常有麦克风。网络摄像头，手机，最新的智能助手。甚至有些屏幕还内置了麦克风。根据这篇论文，你甚至可以从录音中提取数据。该论文有三个主要目标:提取显示文本，区分屏幕上的不同网站，提取用虚拟键盘输入的文本。

这项分析研究了 31 种不同的屏幕。有来自 6 个不同供应商的 12 种不同型号。他们确实使用了一种特殊的 VGA 电缆来分接垂直同步以帮助管理数据，但他们声称这只是一种辅助手段，而不是必不可少的。他们还使用了采样速率为 192 kHz 的高端声音设置。

测量不同显示模式发出的声音是凭经验的。作者认为这种机制是由于电流消耗的变化导致电源部件振动的细微变化。显示器的刷新率也是一个因素。

有了概念证明，团队继续使用 LG V20 手机并通过 Hangouts 呼叫。想象一下，如果电话另一端的人可以知道你在看 Hackaday，而不是关注电话。

需要学习不同类型的监视器以获得最佳精度。看起来阅读小文本也有问题。即使是网站检测也要靠训练。然而，也许锡帽人并没有完全错。

如果您想尝试读取射频辐射，[软件定义无线电是您的好朋友](https://hackaday.com/2017/11/26/a-tempest-in-a-dongle/)。不过，我们很想知道是否有人复制了本文中的声学方法。