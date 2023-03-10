# MicroSynth 将全模拟娱乐与小生意结合在一起

> 原文：<https://hackaday.com/2021/09/30/microsynth-mixes-all-analog-fun-with-a-little-business/>

虽然[【micro kits】](https://hackaday.io/project/181914-microsynth-part-biz-card-part-synth-all-analog)micro synth 是一个全模拟合成器，可以安装在名片大小的 PCB 上，而且他确实用它在商务会议上打破僵局，但这并不是这个项目背后的真正想法。相反，[MicroKits]热衷于让人们玩 synth，还有什么比自己构建 synth 更好的方式呢？

这个项目背后还有一个不可告人的动机:为一个更完整的合成器制作电路原型。因此，设计非常简单——没有微控制器，没有逻辑芯片，甚至没有 555。它甚至没有按钮；取而代之的是，一个八度音阶的键盘只是有交叉的轨迹，玩家的手指将其桥接，形成电阻触摸板。键盘接口电路也很聪明— [MicroKits]使用一对运算放大器将键盘上电阻的线性变化转换为接近指数的电压，以驱动合成器的压控振荡器(VCO)。下面的视频展示了它能做什么。

我们喜欢这样的项目，因为它们展示了严格使用模拟电路可以实现什么。请注意，我们在其他 synth 设计上没有任何问题，我们最近推出的这款基于 555 的配音警报器也非常棒。

 [https://www.youtube.com/embed/xIZMiCK1-oM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/xIZMiCK1-oM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[hack adayprize 2021](https://prize.supplyframe.com)主办单位:[![Digi-Key](img/e7d13a315fd6226594212ca8f8762832.png)](https://www.digikey.com/)[![Supplyframe](img/fdb8a432506edeeafacfef227b3d3b33.png)](https://supplyframe.com/)