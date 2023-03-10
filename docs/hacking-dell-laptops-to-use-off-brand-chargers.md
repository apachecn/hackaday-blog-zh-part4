# 黑客攻击戴尔笔记本电脑使用非品牌充电器

> 原文：<https://hackaday.com/2020/05/27/hacking-dell-laptops-to-use-off-brand-chargers/>

戴尔和许多其他制造商已经开始在其笔记本电脑充电电路中实施智能功能。如果用户希望使用非品牌零件，或者当他们的原装充电器出现故障时，这就让他们倒霉了。【中微子】正处于这样的位置，[决定绕开这个问题。](https://blog.project-insanity.org/2020/05/25/hardware-fix-for-dell-ac-power-adapter-could-not-be-determined/)

笔记本电脑通过第三个 pin 来验证所连接的充电器的身份。这与充电器中嵌入的单线 IC 通信，当笔记本电脑查询时，该 IC 报告充电器的身份。当[中微子]的充电器损坏时，人们试图使用一个非品牌充电器，第三个引脚连接到原来的故障单元。这诱骗笔记本电脑充电成功。

作为一个更持久的解决办法，[中微子]从原来的充电器中获取了单线 IC，而是将其连接到笔记本电脑内部，直接连接到充电端口。因此，当通电时，笔记本电脑总是认为连接了戴尔充电器。存在一些风险，因为如果用户插入比原来更低功率的充电器，可能会发生过载事件，但这只是黑客固有的风险。

对于一个在后 DRM 时代太普遍的恼人问题来说，这是一个很好的解决方法。笔记本充电器也经常是失败的主要原因；我们以前见过像用开心果修理保险箱这样有创意的修复方法！

[感谢 Levi 的提示]