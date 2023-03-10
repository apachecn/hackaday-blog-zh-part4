# 将华夫饼炉变成回流站

> 原文：<https://hackaday.com/2021/01/10/turning-a-waffle-iron-into-a-reflow-station/>

有很多方法可以建造自己的回流焊炉。大多数建筑都是从烤箱开始的——通常是烤面包机——有一小部分人选择改造烤盘。但是这可能是我们第一次看到华夫饼铁变成回流炉。

[![](img/a76abd89593d4970bd8a949e8212e8f2.png)](https://hackaday.com/wp-content/uploads/2021/01/waffle-reflow-thumb.jpeg) 当然，【文森特·德孔尼克】想出的东西本身并不是烤箱。但是他的“回流”确实完成了任务。它始于一个旧的华夫饼机和一些实验，看看需要多少修改来创建各种热回流曲线。事实证明，最初的烹饪表面有太多的热惯性，所以[文森特]用普通的铜片代替了它们。这有助于更快的温度转换，并在 SMD 板的上下加热元件之间创造了一些空间。

至于控制，[Vincent]最初使用了一个带有继电器和热电偶的 Arduino，但他最终构建了一个 2.0 版本，使用一个被黑掉的 Sonoff 作为控制器和开关。在 Sonoff 机箱内添加热电偶驱动板需要一些技巧，但他设法将所有东西都安全地塞进去了。网络接口在 Sonoff 上运行并控制回流过程。

我们认为这是一个伟大的建设，一个毫无疑问会看到我们在旧货店寻找便宜的华夫饼干转换。当然，我们已经看到了一些[令人惊叹的烤箱回流](https://hackaday.com/2020/07/16/touch-screen-reflow-oven-pulls-out-all-the-stops/)，但是 RefloWaffle 的简单性和可移植性对我们很有用。