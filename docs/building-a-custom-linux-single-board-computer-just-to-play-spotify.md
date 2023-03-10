# 打造一台定制的 Linux 单板电脑，只为了玩 Spotify

> 原文：<https://hackaday.com/2021/09/22/building-a-custom-linux-single-board-computer-just-to-play-spotify/>

如果你想将现有的音响或放大器连接到 Spotify，市场上有相当多的选择。你甚至可以点一份树莓派就完事了。然而，【埃文·海利】走自己的路，从零开始打造自己的 Spotify 盒子。

![](img/fb4b2efb195f2292114d8d3ec8536eed.png)

【埃文】甚至还做了这个整洁的木制围栏，一路上还学得更多！

Spotify 盒子装在他自己创造的一个整洁的小木制外壳内，可以通过 [Spotify Connect](https://www.spotify.com/au/connect/) 将任何放大器变成遥控 Spotify 播放器。在你的智能手机上选择歌曲，它们将从 Spotify 盒子中播放，就这么简单。

该项目基于 Allwinner V3S，这是一个片上系统，具有 1.2GHz ARM-Cortex-A7 内核、64MB DDR2 RAM 和以太网收发器。还有一个内置的高质量音频编解码器，使它非常适合这个应用程序。它被扔在一个自己设计的四层 PCB 上，配有 Wi-Fi 和蓝牙收发器、RJ-45 和 RCA 插孔、一个按钮和一些 led。还有一个 SD 卡用来存储。

通过使用 Buildroot 进行定制的 Linux 安装，[Evan]能够在与网络通信的同时获得一个运行 [Spotifyd](https://github.com/Spotifyd/spotifyd) 的准系统。完成后，就像把 Spotify 盒子连接到放大器上，开始播放一些音乐一样简单。

在这个过程中，[Evan]学习了所有关于编译驱动程序和使用嵌入式 Linux 的知识，以及如何将一个裸 SoC 构建成一个全功能的单板计算机。当别人说他们“制造”了一个 Spotify 播放器时，他大概会清一清嗓子。

如果你喜欢复古的电脑，考虑将 Spotify [与你的经典 Mac 连接起来！](https://hackaday.com/2018/12/21/giving-an-old-mac-spotify/)

【感谢杰伊·卡尔森的提示！]