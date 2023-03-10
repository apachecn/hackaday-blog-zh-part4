# 2021 年的编程伙伴

> 原文：<https://hackaday.com/2021/04/15/programming-pals-in-2021/>

[IMSAI Guy]发布了一个后续视频，详细介绍了他如何在现代编程 GAL22V10 芯片。我们注意到几天前[的步进电机项目](https://hackaday.com/2021/04/09/stepper-motors-quick-and-simple/)中缺少了这个，我们还没来得及问他，他就回答了。不，你不必从壁橱里翻出旧的英特尔 486 DX2-66，在易贝搜索工作的软盘驱动器。事实证明，答案比你想象的要简单。

![](img/8571b095d2b70746e3b12ee3e523f0a4.png)

Microchip 现在通过 2016 年收购 Atmel 拥有 WinCUPL，并从 Microchip 网站提供 WinCUPL 免费下载。这只能在 Windows 上运行，尽管一些用户报告说在 Linux 上 Wine 下运行是成功的。该工具将编译设计，但您仍然需要对芯片进行编程。如果你最近做过 EEPROM 编程，你很可能有一款 TL866A MiniPros，它可以处理 CPLDs、PALs 和 gal，也可以处理 EEPROM。[IMSAI Guy]将指导您完成编程过程，如果您以前编程过 EEPROMs，那么这个过程会很熟悉。

对于那些喜欢 Linux 或 Mac 环境的人来说，有一些替代方案。我们已经看到`GALasm`被用在几个项目上，比如【肯·雅普】的 [8085 Minimax](https://hackaday.io/project/164087-8085-minimax/log/160589-programmng-the-gal) 。`GALasm` 的 [GitHub 库声明商业使用是严格禁止的，所以请注意这是否适用于您的项目。至于控制 TL866A，GitLab](https://github.com/daveho/GALasm) 上有一个叫`minipro`的 [Linux 端口。如果你想试验这些可编程逻辑芯片，剩下的一个障碍是如何真正得到它们——许多现在已经过时了。但是看起来你还是可以从各种渠道买到 Lattice 和 Microchip (Atmel)的。快乐编程。](https://gitlab.com/DavidGriffith/minipro/)

 [https://www.youtube.com/embed/fo_WlA-kVRc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/fo_WlA-kVRc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

