# 打印不停止与这个 Prusa I3 MK3 模块

> 原文：<https://hackaday.com/2022/06/25/the-prints-dont-stop-with-this-prusa-i3-mk3-mod/>

3D 打印的一个问题是，当打印完成时，你需要回去把打印的东西从床上拉下来，重新设置它以进行下一次打印。如果您出于某种原因需要打印 600 个小零件，该怎么办？大多数人可能会说，买很多打印机，把它们排好队。不是[Pierre Trappe]，因为他决定[他的 Prusa i3 MK3S+将连续打印](https://github.com/Pierro55/Loop)。

该设置被称为循环，由几个部分组成。首先，有一个清扫构建板以清除打印件的臂，一个让打印件下降的滑块，以及一个让打印机坐在上面的支架，使其处于一个角度。下一步是修改 OctoPrint 以允许连续打印队列。切片器需要更换，因为[Pierre]提供了一些 g 代码来重置打印机和清除打印。

我们对这一次文档中对细节的关注印象特别深刻。有大量关于如何正确固定床的指南，因为你不能让它中途脱落，但你需要它在手臂扫过床时干净而容易地分离。校准第一层是必不可少的，他提供了方便的指示拨入。此外，温度和材料起着至关重要的作用，[Pierre]记录了他在开发 Loop 时使用的不同材料和温度。

虽然[连续带式打印机](https://hackaday.com/2022/02/03/conveyor-belt-printer-mod-is-nearly-all-printed/)可以说是打印 600 个小零件问题的“正确”答案，但它们有自己的包袱。能够在像 Prusa i3 这样可靠且支持良好的打印机上实现类似的功能是一个令人信服的选择。

 [https://www.youtube.com/embed/T4kzyH2tcBQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/T4kzyH2tcBQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

