# 应该为 Windows、Mac、IOS、Android 还是 Linux 构建？是啊！

> 原文：<https://hackaday.com/2020/10/01/should-you-build-for-windows-mac-ios-android-or-linux-yes/>

计算机语言的圣杯是编写一次代码，然后毫不费力地将它部署到任何地方。Java 喜欢把这个想法归功于自己，但是 UCSD P-Code 比它早得多，你可以说大型机甚至更早就有了类似 Fortran 单元号的 I/O 抽象。更现代的努力包括 Qt，GTK 和其他东西。自然，所有这些在某些方面都有不足。现在，谷歌带着 [Flutter](https://flutter.dev) 加入了这场争斗。

Flutter 并不新鲜，但在过去，它只处理 Android 和 iOS。现在它可以瞄准桌面平台，甚至可以产生 JavaScript。我们还没有充分地使用这个系统来说明它有多成功，但是如果你想要一些第一手的经验，你可以在你的浏览器中尝试一下。

Flutter 使用 [Dart](https://dart.dev) ，对 Mac 和 Windows 的支持被认为是 alpha 质量。如果你懂 C++或者 Python 之类的传统语言，你使用 Dart 就不会有任何问题。

如果你想了解某人用 Flutter 部署一些重要东西的经历，这里有一个全面的应用程序，有一个非常详细的报告。谷歌会成功吗？当然，它们足够大，理应如此。然而，任何尝试过跨平台部署的人都会告诉你，解决大问题要比解决小问题容易得多。你通常会死于跨平台项目中的一千次剪纸，而不是一次挥剑。

谷歌表示，他们希望 Flutter 也瞄准嵌入式设备。我们很确定他们指的是嵌入式，也就是拥有 UI 和互联网连接的相当强大的处理器。但是也许将来我们会看到其他的平台。毕竟，我们已经看到了许多目标相同的精简版 Java 虚拟机。我们甚至亲自探索了[跨平台编程、](https://hackaday.com/2020/03/04/write-once-run-everywhere-cross-platform-programming-done-right/)的复杂性。