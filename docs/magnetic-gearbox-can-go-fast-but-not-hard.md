# 磁力变速箱能走得快但不硬

> 原文：<https://hackaday.com/2022/09/02/magnetic-gearbox-can-go-fast-but-not-hard/>

3D 打印齿轮箱非常适合实验设计，但由于打印表面的粗糙度和不准确性，它们可能会磨损很快，而且噪音很大。作为一种可能的替代方案，[Resetman]正在试验[磁性 3D 打印变速箱](https://www.youtube.com/watch?v=DAWVetrtD9U)，它们在旋转的车轮之间没有物理接触的情况下工作，并且还可以以一些有趣的方式“调整”不同的传动比。

自然地，两个间隔很近的带有磁铁的轮子会相互作用，比率由每个轮子上的磁铁数量决定。一个不太明显的实现是二阶径向磁通同轴磁齿轮箱。它的工作原理类似于普通的行星齿轮箱，有一个包含磁铁的内外轮，以及一个称为通量调节器的中间环，其中包含等间距的铁磁性钢金属。在[Resetman]的演示中，通量调制器只是一个 3D 打印的环形螺钉。

最明显的缺点当然是严重限制扭矩传递。如果通量调节器缓慢加速，可以很容易地将太阳轮加速到 12，000 RPM，但速度的任何突然变化都会导致它失去同步。当然，您可以将这视为特定用例的扭矩限制特性。通过一点测试，他确定了 1:4 比率下的扭矩极限为 0.05 牛·米。这可以通过一些优化来增加，例如重新排列磁体以形成 Halbach 阵列，以及减小部件之间的气隙。

磁力齿轮箱并不是什么新鲜事，我们之前已经展示过另一个[演示器](https://hackaday.com/2020/04/13/simple-demo-shows-the-potential-of-magnetic-gears/)，甚至就这个主题做了一次[“问吧”。你会用这些做什么？下面让我们了解一下。](https://hackaday.com/2016/08/15/ask-hackaday-what-are-magnetic-gears-good-for/)

 [https://www.youtube.com/embed/DAWVetrtD9U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/DAWVetrtD9U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

