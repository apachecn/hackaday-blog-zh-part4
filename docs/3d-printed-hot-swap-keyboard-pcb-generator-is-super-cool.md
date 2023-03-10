# 3D 打印，热插拔键盘 PCB 发电机是超级酷

> 原文：<https://hackaday.com/2021/07/12/3d-printed-hot-swap-keyboard-pcb-generator-is-super-cool/>

大约一个月前，[50an6xy06r6n]分享了他们的热插拔 3D 印刷电路板，用于机械键盘 subreddit 的键盘设计。它更像是一个原型工具，而不是一个永久的固定装置，尽管没有什么可以阻止你永久地使用它。[嗯，现在更好了，开源引导](https://www.reddit.com/r/functionalprint/comments/o8qy4v/3dprintable_hotswap_pcb_generator_now_opensource/)。

[![](img/ac83bef35fb119697327923ee10e9276.png)](https://hackaday.com/wp-content/uploads/2021/07/pcb_back.jpg)【50 an 6 xy 06 r 6n】想出这个来更快地测试分离式 ergo 布局，而不必焊接任何东西——开关引脚与行导线和折叠二极管引脚接触。事实上，准备所有的二极管可能是最耗时的事情。

设计可以从布局数据生成，或者你可以直接从一个 [KLE](http://www.keyboard-layout-editor.com/) JSON 文件转换。我们喜欢这个键盘试验板发生器看起来如此干净，我们希望我们已经想到了它！

[【50 an 6 xy 06 r 6n】的 PCB 生成器](https://github.com/50an6xy06r6n/hotswap_pcb_generator)目前支持 Cherry MX/clones 和 Kailh Choc 开关足迹。如果你想要阿尔卑斯山，就必须有人送一些阿尔卑斯山来实现。

[![](img/b09f1803a4ddafce2aa3d16e305c24ab.png)](https://hackaday.com/wp-content/uploads/2021/07/hot-swap-pcb-bv.jpg)

只要所有的接触点都是好的，你应该可以无限期地使用它作为最终的 PCB。[我们当然已经看到了我们的 3D 打印导丝](https://hackaday.com/2021/03/02/3d-printed-macro-pad-ditches-the-pcb-with-slick-wiring-guides/)。真的，你可以打印整个东西，[包括开关](https://hackaday.com/2020/07/09/3d-printing-a-macro-pad-switches-and-all/)。