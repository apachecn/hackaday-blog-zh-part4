# 本周失败:如何不造长丝挤出机

> 原文：<https://hackaday.com/2021/02/28/fail-of-the-week-how-not-to-build-a-filament-extruder/>

如果能自己造灯丝就太好了。从表面上看，这似乎很容易做到，但正如[托马斯·桑拉德勒]在学生时代发现的那样，[有许多细节会困扰你的设计。他的挤压机有点工作，但他不会建议重复他的努力。事实上，他希望你能学会什么是不应该做的，如果你自己尝试去做的话。](https://www.youtube.com/watch?v=QsxYMtiz5Fo)

平心而论，[托马斯]是一个低预算的学生，并试图节约。例如，他试着用钻头来驱动螺旋钻。为什么不呢？它看起来像钻头。但他发现这并不令人满意，并转向一对内置齿轮系的刮水器电机。

刮水器电机允许他得到一些 ABS 长丝，但机器有更多的问题。其他经验教训是保持水冷却箱关闭，这样水就不会溅到电子设备上，并且很难用 CCD 传感器观察灯丝。

控制器是一个简单的 Arduino。塑料到达模具之前有三个加热区。正如你所料，有一个 PID 控制器来调节机器。

[托马斯]说流速太高，所以放慢生产可能会有帮助。事后看来，一个更小的螺旋钻也在他要做的事情清单上。熔化区域需要像 3D 打印机的加热器一样加热，以防止热塑料流向管子较冷的部分并堵塞。

以他目前的经验和更大的预算，我们毫不怀疑他最终会有一台可行的挤出机。事实上，我们总是喜欢从别人的次优构建中学习。在互联网上向你展示失败的项目有点令人羞愧，但这确实是一项有价值的服务。

我们想要一台能够回收我们的废旧零件的挤压机。我们已经看到了一些[非常便宜的版本](https://hackaday.com/2013/11/01/low-cost-filament-extruder/)，但是我们真的不知道他们工作的有多好。

 [https://www.youtube.com/embed/QsxYMtiz5Fo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/QsxYMtiz5Fo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

