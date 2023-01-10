# 从头开始制作自己的支持 BLE 的 IOS 应用程序

> 原文：<https://hackaday.com/2021/12/04/make-your-own-ble-enabled-ios-app-from-scratch/>

即使是那些对苹果产品持最怀疑态度的读者也会喜欢这个来自[Akio]的支持[蓝牙低能耗(BLE)的 iOS 应用教程](https://www.instructables.com/IOS-App-for-Adafruit-Feather-NRF52832/)。

如今一切都是“连接”的，智能手机应用程序当然是我们生活中无处不在的一部分。我们已经看到了很多例子[将你的蓝牙项目连接到 Android 设备](https://hackaday.com/2013/02/15/beginners-androidarduino-example-shows-the-power-of-app-inventor/)，但是相对来说，连接到 iOS 设备的教程就比较少了。这主要与[安卓更大的市场份额](https://hackaday.com/2020/09/09/google-turns-android-up-to-11-with-latest-update/)以及安卓更加开源友好的商业模式有关。然而，如果你将物联网开发作为业余爱好或职业，那么你可能会发现自己与苹果设备的互动比你愿意承认的更多。

(Akio 的)应用程序实际上是用从 Adafruit nRF52832 羽毛板上读取的数据实时更新图表。然后，他会带你了解使用苹果的故事板界面创建用户界面(UI)的所有基础知识，这是一种[简单的拖放模式](https://hackaday.com/2018/09/21/myopenlab-talks-to-arduino-pi-and-more/)，类似于你可能在许多其他环境中使用的东西。[Akio]向读者展示了如何添加允许用户与应用程序交互的按钮，向用户显示数据的标签，并带你了解苹果使用 IBAction 和 IBOutlets 将 UI 元素连接到代码的奇怪方法。他的教程的重点是向读者展示如何将图表添加到他们的 iOS 应用程序中，这似乎比你想象的要多花几个步骤。

[Akio]在详述所有相关功能方面做得非常好，这样读者就有希望理解每段代码在做什么。我们真的很喜欢他为一些更棘手的编程步骤添加单独的视频教程。他也欣然承认，有些人可能会选择完全用代码开发他们的 UI，而不是故事板，但他认为故事板对初学者仍然很重要，当 UI 相当简单时，故事板真的很方便。

当然，在真正的开源方式中，[Akio] [在他的 GitHub 库](https://github.com/shaqattack13/iOS-BLE)上提供了他的所有代码，所以你可以克隆回购协议并自己运行代码，还可以使用他在制作应用程序时使用的一些资源。我们很想看到两件事。希望[Akio 的]教程能让连接 iOS 设备看起来[比以前](https://hackaday.com/2018/08/03/beginning-ble-experiments-and-making-everything-better/)轻松得多。