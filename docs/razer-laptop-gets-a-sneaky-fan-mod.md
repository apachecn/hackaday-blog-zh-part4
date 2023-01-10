# 雷蛇笔记本电脑得到一个鬼鬼祟祟的球迷模式

> 原文：<https://hackaday.com/2019/11/05/razer-laptop-gets-a-sneaky-fan-mod/>

有些人喜欢风扇噪音，用它来帮助入睡或只是在房间里创造一些氛围。其他人讨厌它，像[迪米特里斯]，会在可能的地方采取严厉措施消灭它。当他的 Razer Blade 笔记本电脑不停地转动时，[该去工作了](https://onedrive.live.com/?authkey=%21AN1DtWk3Y9VQOtU&cid=1871385C8AE58CDF&id=1871385C8AE58CDF%21163&parId=1871385C8AE58CDF%21145&o=OneUp)。

Razer 笔记本电脑使用一个输出可变占空比信号的控制器来控制风扇速度。不幸的是，即使笔记本电脑很冷，风扇也不会完全关闭，导致令人沮丧的过度噪音。[Dimitris]实现了一个 ATtiny85 拦截这个信号，让他完全控制风扇。实施了两种模式，一种是在占空比最小时关闭风扇，另一种是尽可能将风扇保持在最低速度。

虽然修改高性能笔记本电脑的关键冷却系统是一件有风险的事情，但为了一些和平和安静，这是一个体面的代价。我们也看到了与这种模式完全相反的东西—[比如配备了额外冷却系统的 Xbox 360](https://hackaday.com/2015/11/19/adding-a-fan-where-microsoft-should-have/)。