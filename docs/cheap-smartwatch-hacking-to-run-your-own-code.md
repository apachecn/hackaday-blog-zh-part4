# 廉价智能手表黑客，运行自己的代码

> 原文：<https://hackaday.com/2020/05/02/cheap-smartwatch-hacking-to-run-your-own-code/>

[Aaron Christophel]最近很忙，他买了一块 P8 智能手表，这种手表你们很多人肯定都见过。他们几乎不花钱，也几乎什么都不做。平心而论，借助 Nordic 的芯片(NRF52832)，它们确实可以使用蓝牙 LE 连接到您的手机，并且它们可以完成几项简单的任务。但它们运行应用程序的方式不同于安卓或苹果手表。[Aaron]想要运行自己的应用程序，所以他的 YouTube 频道有很多关于黑掉 P8 和其他具有类似芯片的手表的信息。在下面的一个视频中，他展示了他是如何为设备编写对 Arduino 编程的支持的。我们真正感到兴奋的是下面的第二个视频，他展示了他的 Android 应用程序，可以通过蓝牙[刷新设备。这意味着你有可能在不打开设备的情况下入侵这些设备。](https://www.youtube.com/watch?v=gUVEz-pxhgg&t=303s)

通常运行这些手表的应用程序被称为 Da Fit，因此[Aaron]将他的实用程序称为 [DaFlasher](https://play.google.com/store/apps/details?id=com.atcnetz.paatc.patc) 。这都是早期的东西，所以我们希望一些哄骗让一切工作，但它有很大的希望。

该设备内部是一个内置蓝牙堆栈的 ARM 处理器。显然，许多廉价的智能手表和健身追踪器都有相同的电路板。我们用一款使用 Da Fit 的手表进行了尝试，我们从未在 DaFlasher 屏幕上看到它的 MAC，但它与视频中出现的 P8 有很大不同。不过，该程序确实在附近发现了许多其他 BLE 设备。

在你的手表上运行你自己的代码会让你得到很多极客的信任。但不如[打造自己的手表](https://hackaday.com/2019/01/01/a-smartwatch-you-can-easily-build-yourself/)来得多。从我们看到的情况来看，[围栏](https://hackaday.com/2018/10/26/a-multifunction-esp8266-smartwatch/)是最难的部分。

 [https://www.youtube.com/embed/c9KMUe6GVLw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/c9KMUe6GVLw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/gUVEz-pxhgg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/gUVEz-pxhgg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

