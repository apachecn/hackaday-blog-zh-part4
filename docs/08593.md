# 宏键盘在甲板上

> 原文：<https://hackaday.com/2020/12/10/the-macro-keyboard-is-on-deck/>

从定制的 DIY 键盘到 MacBooks 上的极化触摸条，可重构宏键盘的概念已经被许多人反复提及。带 Wi-Fi 和 3D 打印机的廉价而强大的微控制器的不断崛起，使得滚动自己的宏键盘变得一年比一年容易。[Dustin Watts]已经加入了这个众所周知的俱乐部，并且[制作了一个漂亮的宏面板，叫做 FreeTouchDeck](https://hackaday.io/project/175827-freetouchdeck) 。

我们已经看到宏键盘[使用旋转编码器来循环按键](https://hackaday.com/2020/04/16/software-shortcut-keyboard-registers-many-macros/)的不同映射。FreeTouchDeck 采用了显示方式，并结合了触摸屏来提供不同的按钮。[Dustin]的灵感来自于[的一个类似项目，叫做 FreeDeck](https://hackaday.com/2020/07/09/open-source-stream-deck-does-it-without-touch-screens/) ，它提供了六个按钮，每个按钮都有一个小屏幕。FreeTouchDeck 由 ESP32 供电，驱动带有 XPT2046 触摸控制器的 ILI9488 触摸屏。这意味着 FreeTouchDeck 可以提供六个带子菜单的按钮和各种各样的铃铛和哨子。通过模拟蓝牙键盘实现与电脑的连接。通过添加启动 web 服务器的配置模式，FreeTouchDeck 允许在运行中轻松定制。

[Dustin]快速制作了一个 PCB，可以很容易地将 ESP32 和 TFT 焊接在一起，但试验板也可以很好地工作。在 GitHub 上可以找到 Gerbers。总而言之，一个漂亮的 3D 打印外壳以干净整洁的方式封装了整个系统。[代码、文档和机箱设计都在他的 GitHub](https://github.com/DustinWatts/FreeTouchDeck) 上。

 [https://www.youtube.com/embed/soIGV6BszcM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/soIGV6BszcM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[Dustin]将这封邮件发送给我们！