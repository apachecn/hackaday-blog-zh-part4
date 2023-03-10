# 将塞尔达经典带到浏览器中

> 原文：<https://hackaday.com/2022/05/04/bringing-zelda-classic-to-the-browser/>

找到一款不是网络浏览器的设备或应用似乎并不容易。如今，它要么连接到网络(看着你 ESP32)，要么只是一个伪装成其他东西的网络浏览器(la electron、PWAs 或 React Native)。因此，当然，我们有责任创造更多令人兴奋的东西来浏览。康纳·克拉克就是其中之一，他把塞尔达经典《T2》带到了浏览器中。

塞尔达经典 (ZC)不是官方*塞尔达*游戏。相反，它是一个旧引擎，旨在运行 OG *塞尔达传说*中的世界，并易于修改以支持数百种不同的游戏。迄今为止，一个大型社区提交了超过 600 个游戏。《ZC》是一款基于 Allegro 的只在 Windows 上运行的游戏，所以第一步是开发 Emscripten 来调整 C++代码以支持网络环境。Connor 没有完全从 Allegro 移植庞大的代码库，而是从 Allegro 4 跳到了 Allegro 5。Allegro 5 有 SDL 作为后端，并增加了对 Emscripten 的支持。

不幸的是，4 比 5 并不像改变依赖关系那么简单。API 完全重写，有一个方便的适配器称为 Allegro Legacy，可以帮助项目从一个过渡到另一个。在消灭了大量的臭虫之后，这是一个相对无痛的过程。在快速完成音乐和关卡数据工作后，[Connor]面临下一个挑战:多线程。将主循环从浏览器线程转移到 web worker 中的努力遇到了不得不屈服于循环、死锁和递归互斥的问题。最后，在修复了 SDL 和快板中的几个 bug 后，他添加了音乐和游戏手柄支持。

这是一个不可思议的旅程，有许多调试看似棘手的错误的技巧和诀窍。GitHub 上有[代码，或者如果你感兴趣的话](https://github.com/connorjclark/ZeldaClassic)[可以跳进去开始玩](https://hoten.cc/zc/play/)。为什么不看看这个基于[浏览器的 OpenSCAD](https://hackaday.com/2022/03/14/the-noble-effort-to-put-openscad-in-the-browser/) ？