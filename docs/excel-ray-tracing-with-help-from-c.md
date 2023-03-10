# 在 C 语言帮助下的 Excel 光线追踪

> 原文：<https://hackaday.com/2021/09/28/excel-ray-tracing-with-help-from-c/>

[solly]喜欢使用 Microsoft Excel 进行光线追踪已经不是什么新闻了。然而，他最近更新了他的设置，使用 C XLL 中的函数——实际上是一个 DLL——来加速 Excel 的渲染。即使您不喜欢光线跟踪，创建自定义高性能 Excel 函数的技术可能会在其他地方对您有所帮助。

我们已经看到了[s0lly]在之前的努力[，你当然可以看到新技术加快了速度，产生了更好的结果，这并不特别令人惊讶。除了速度更快之外，新的例程产生了更多的细节。](https://hackaday.com/2019/08/29/experiments-in-3d-graphics-via-excel/)

如果你想试一试的话，微软的文档很清楚。你可以在你的 C 代码中做的事情之一是利用像线程这样的东西来获得更好的性能，这在他的例子中显示了。

当然，你可以争辩说你不需要 Excel，但是那有什么意思呢？此外，您还需要处理所有的数据输入和输出，这本身就是一种痛苦。

如果你需要一个关于光线追踪的简单解释，我们已经介绍过了。我们自己也不会滥用[电子表格](https://hackaday.com/2020/11/13/dsp-spreadsheet-the-goertzel-algorithm-is-fouriers-simpler-cousin/)。

 [https://www.youtube.com/embed/XAJS-pbcWYA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/XAJS-pbcWYA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

