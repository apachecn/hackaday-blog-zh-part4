# 在 ESP32 上模拟 IBM PC

> 原文：<https://hackaday.com/2021/07/28/emulating-the-ibm-pc-on-an-esp32/>

IBM PC 产生了基本架构，并发展成为我们今天所知的主要 Wintel 平台。曾经笨重，麻烦，耗电，现在你可以用一个廉价的商用微控制器在一个单板上模拟它。这要归功于[Fabrizio Di Vittorio]的工作，他在 Youtube 上分享了一个操作方法。

[完整的播放列表非常值得一看，](https://www.youtube.com/watch?v=3I1U2nEoxIQ&list=PLv49lyEwqDNMz9XGBy6wnBzBAYFVMdCki&index=24)展示了大量运行在该平台上的老派 PC 应用程序和游戏。有 QBASIC，FreeDOS，Windows 3.0，当然还有飞行模拟器。在 20 世纪 80 年代，后一种游戏实际上被认为是 PC 兼容性的事实标准，所以 ESP32 可以用[Fabrizio 的]代码运行它的事实表明他做得很好。

它非常完整，ESP32 可以处理从音频和视频到声音输出以及键盘和鼠标输入的一切。这证明了现代微控制器的能力，在 2021 年这是一个如此简单的壮举。

我们以前也见过 ESP32 模拟 8 位游戏系统。如果你记得[Fabrizio]的名字，很可能是来自他的优秀 FabGL 图书馆。休息后的视频。

 [https://www.youtube.com/embed/upgogkPwG6E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/upgogkPwG6E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/3I1U2nEoxIQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent&listType=playlist&list=PLv49lyEwqDNMz9XGBy6wnBzBAYFVMdCki](https://www.youtube.com/embed/3I1U2nEoxIQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent&listType=playlist&list=PLv49lyEwqDNMz9XGBy6wnBzBAYFVMdCki)

