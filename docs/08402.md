# E-Ink 日历为所有人铺平了道路

> 原文：<https://hackaday.com/2020/11/19/e-ink-calendar-paves-a-path-for-all/>

马丁·法萨尼已经着手制作一个漂亮的低功耗 E-Ink 日历，他可以把它挂在墙上。但也许更重要的是，他所做的工作让未来的每个人都更容易拥有电子墨水显示器。许多电池供电的电子墨水项目连接到某个服务器，下载位图图像，显示新图像，然后进入深度睡眠模式。[马丁的]项目没有什么不同，但它使用了一个方便的微服务，为你做转换和渲染。

这款基于 ESP32/ESP32S2 的日历的固件在 GitHub 上开源，其版本基于 Arduino 框架和原生 ESP-IDF 框架。该固件的一个特别奇妙的部分是一个名为 CalEPD 的 C++组件，用于驱动电子纸显示器。CalEPD 扩展了 Adafruit_GFX 类，并在一个单独的 repo 中被分解为[，这使得它很容易在其他项目中使用。由于它支持几十种不同的电子纸显示器，这简化了用不同屏幕构建日历的过程。固件包括智能手机或平板电脑的蓝牙设置流程。这意味着您可以快速配置它的唤醒频率、查询内容和其他重要功能。](https://github.com/martinberlin/CalEPD)

演示视频中显示的硬件有一个 7.5 英寸的 Waveshare 屏幕，分辨率为 800 x 400，位于 3D 打印的外壳内。还有一个 5000 毫安的电池，ESP32 TinyPICO 为整个系统供电。TinyPICO 因其令人难以置信的深度睡眠功耗而入选。所有这些都可以放入一个只有 11 毫米厚的框架中，其中的 STL 文件是可用的。[Martin]继续致力于日历显示，最近增加了对 FocalTech 触摸面板控制器的支持。我们很期待他接下来的发展！

这不是我们看到的第一个电子墨水显示项目，但这是构建您自己的项目的一个很好的参考。如果你需要另一个好的起点，这个天气预报可能会给你一点你需要的灵感。

 [https://www.youtube.com/embed/5x-FETrisDw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/5x-FETrisDw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

