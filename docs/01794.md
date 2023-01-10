# 电磁 7 段显示屏让您的眼睛和耳朵倍感舒适

> 原文：<https://hackaday.com/2019/01/12/electromagnetic-7-segment-display-easy-on-the-eyes-and-the-ears/>

我们喜欢电磁显示器:采用数字读数的现代外观，结合理论上你**可以*自己创造的低技术线圈机制，加上一点随机的噼啪声，还有什么不喜欢的呢？显然，[Nicolas Kruse]分享了我们对这些显示器的喜爱，因为他超越了理论，[从零开始创造了 7 段磁驱动显示器](http://www.nonan.net/nkruse/electromagnetic_7-segment_display)。*

 *正如你现在所期待的那样，这个显示器是 3D 打印的。每个部分包含一个小钕磁铁，每个线圈 1 毫米铁芯通量集中。线圈由 1.6 A 峰值电流驱动，使段在不到 10 毫秒的时间内翻转。[Nicolas]为显示器底座、段和卷轴提供 STL 文件，以便您可以打印自己的显示器。他还发布了驱动器的原理图和代码，该驱动器使用 ATtiny44 通过 N 沟道和 P 沟道 MOSFETs 驱动线圈。最初设计用于驱动无源 4×7 矩阵显示器，驱动器无法在不影响相邻段的情况下翻转一段。然而，对于单个显示器，驱动程序工作正常。我们希望他能尽快解决矩阵问题，因为我们真的很想看到用这些显示器制作的时钟。

休息之后，您可以看到(和听到)一段简短的视频。噼啪声没有让人失望！

 [https://www.youtube.com/embed/j9YwPZ9qRGc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/j9YwPZ9qRGc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



我们以前在这些页面上展示过使用商业翻转显示器的项目，以及那些使用 T2 回收翻转点阵的项目。*