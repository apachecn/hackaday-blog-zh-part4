# 聪明的气体混合器得到了自制激光管的正确混合

> 原文：<https://hackaday.com/2021/04/28/clever-gas-mixer-gets-just-the-right-blend-for-homebrew-laser-tubes/>

[卢卡斯]在 YouTube 上的 Cranktown City 最近很忙，但尽管目前出现，他的最新项目不是焊机。相反，他建造了一个非常聪明的气体混合器来填充他自制的二氧化碳激光管，它看起来只是一台焊接机。(视频，嵌在下面。)

我们一直在追踪[卢卡斯]从零开始建造激光切割机的旅程——真的是从零开始，因为[他建造了自己的激光管](https://hackaday.com/2021/03/31/scratch-built-co2-laser-tube-kicks-off-a-laser-cutter-build/)而不是依赖现成的东西。然而，获得正确的气体混合物来填充管道有点痛苦，因为他使用派对气球来收集二氧化碳、氦气和氮气，在每次添加后测量气球的直径，以确定每种气体的体积比。他试图将这一过程自动化，主要是围绕一种所谓的[气垫船](https://www.calculated.com/prd409/AirShim-1190-Inflatable-Pry-Bar-and-Leveling-Tool.html)，这基本上是一种由坚固材料制成的扁平充气袋，承包商使用气压来撬、楔、提升和垫。

[卢卡斯]第一个想法是利用水的位移和一些光电传感器来测量袋子中气体的体积，但这被证明是不切实际和不必要的。事实证明，当袋子里装着一个简单的微型开关时，它更容易被感知；每次灌装产生固定体积的气体，很容易计算出每种气体的分配量。Arduino 控制泵，这是一个回收的冰箱压缩机，监控限位开关和控制电磁阀，并计算气体分配的体积。

从下面的视频来看，混音器工作得非常好，它的简单给我们留下了深刻的印象。我们以前从未认真考虑过建造我们自己的激光管，但是看到[卢卡斯]在这方面的努力，这看起来很容易实现。我们期待着看到他的激光项目走到一起。

 [https://www.youtube.com/embed/Ax7xlcFS2QY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Ax7xlcFS2QY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

